###  Example of inversify test


[InversifyJS/inversify.test.ts at master · inversify/InversifyJS](https://github.com/inversify/InversifyJS/blob/master/test/inversify.test.ts "InversifyJS/inversify.test.ts at master · inversify/InversifyJS")


 

```typescript
 interface Ninja {
            fight(): string;
            sneak(): string;
        }

        interface Katana {
            hit(): string;
        }

        interface Shuriken {
            throw(): string;
        }

        @injectable()
        class Katana implements Katana {
            public hit() {
                return "cut!";
            }
        }

        @injectable()
        class Shuriken implements Shuriken {
            public throw() {
                return "hit!";
            }
        }

        @injectable()
        class Ninja implements Ninja {

            private _katana: Katana;
            private _shuriken: Shuriken;

            public constructor(
                @inject("Katana") katana: Katana,
                @inject("Shuriken") shuriken: Shuriken
            ) {
                this._katana = katana;
                this._shuriken = shuriken;
            }

            public fight() {return this._katana.hit(); }
            public sneak() { return this._shuriken.throw(); }

        }

        const container = new Container();
        container.bind<Ninja>("Ninja").to(Ninja);
        container.bind<Katana>("Katana").to(Katana);
        container.bind<Shuriken>("Shuriken").to(Shuriken);

        const ninja = container.get<Ninja>("Ninja");

        expect(ninja.fight()).eql("cut!");
        expect(ninja.sneak()).eql("hit!");
```
