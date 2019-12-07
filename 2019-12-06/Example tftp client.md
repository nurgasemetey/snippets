### Example tftp client







```java 
import org.apache.commons.net.tftp.TFTP;
import org.apache.commons.net.tftp.TFTPClient;

import java.io.FileInputStream;
import java.io.IOException;
import java.net.SocketException;
import java.net.UnknownHostException;

public class TestClient {


    public static void main(String arg[])
    {
        TFTPClient tftp =new TFTPClient();
        FileInputStream input = null;

        // Try to open local file for reading
        try
        {
            input = new FileInputStream("/home/nurgasemetey/Desktop/siyah.bmp");
        }
        catch (IOException e)
        {
            tftp.close();
            System.err.println("Error: could not open local file for reading.");
            System.err.println(e.getMessage());
            System.exit(1);
        }
        try
        {
            tftp.open();
        }
        catch (SocketException e)
        {
            System.err.println("Error: could not open local UDP socket.");
            System.err.println(e.getMessage());
            System.exit(1);
        }
        try
        {
            tftp.sendFile("IMAGE04.BMP", TFTP.BINARY_MODE, input, "192.168.1.120");
        }
        catch (UnknownHostException e)
        {
            System.err.println("Error: could not resolve hostname.");
            System.err.println(e.getMessage());
            System.exit(1);
        }
        catch (IOException e)
        {
            System.err.println("Error: I/O exception occurred while sending file.");
            System.err.println(e.getMessage());
            System.exit(1);
        }
        finally
        {
            // Close local socket and input file
        }
    }
}

```
