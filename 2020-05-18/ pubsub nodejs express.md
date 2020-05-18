###  pubsub nodejs express


[pedrorvelloso/donation-tracker-server](https://github.com/pedrorvelloso/donation-tracker-server "pedrorvelloso/donation-tracker-server")


 

```
import { Server } from "http";
import PubSub from "pubsub-js";
import io, { Socket } from "socket.io";

class ServerSocket {
    public socketIo: io.Server;
    constructor(server: Server) {
        this.socketIo = io.listen(server);
        this.connect();
    }

    private connect(): void {
        this.socketIo.of("/socket").on("connection", (socket: Socket) => {
            PubSub.subscribe("donation", (msg: string, data: any) => {
                socket.emit("donation", data);
            });
        });
    }
}

export default ServerSocket;


import PubSub from "pubsub-js";
import client from "socket.io-client";

import Donation, { DonationModel } from "../models/Donation";

class StreamlabsSocket {
    public client: SocketIOClient.Socket;

    constructor() {
        this.client = client(
            `${process.env.STREAMLABS_SOCKET_URL}?token=${
                process.env.STREAMLABS_SOCKET_TOKEN
            }`,
        );

        this.donationTracker();
    }

    private donationTracker(): void {
        this.client.on("event", (eventData: any) => {
            if (
                !eventData.for ||
                (eventData.for === "streamlabs" &&
                    eventData.type === "donation")
            ) {
                PubSub.publish("donation", eventData.message);
                const donationStreamlabs = eventData.message[0];
                donationStreamlabs.formattedAmount =
                    donationStreamlabs.formatted_amount;

                const {
                    amount,
                    from,
                    message,
                    formattedAmount,
                }: DonationModel = donationStreamlabs;

                const donation = new Donation({
                    amount,
                    formattedAmount,
                    from,
                    message,
                });
                donation.save();
            }
        });
    }
}

export default StreamlabsSocket;
```
