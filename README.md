# Estimote packet specs

We believe in **runnable code** more than we do in PDF specs, so we bring our specs to you in form of example Node.js scripts that demonstrate **how to do all the parsing**. Combined with rich in-line documentation, this should allow you to write your own parsers (in technology of your own choice, and for platforms you want to use) in no time. Or, just port our code! :wink:

Simply read the `*.js` files to learn how the Estimote packets are constructed and how to parse them.

But, the best part is, you can also run them!

You'll need to:

- install [Node.js][njs]; on macOS, you can use [homebrew][hom] and `brew install node`
- meet the ["noble" prerequisites][nob] ("noble" is a Node.js library that we use here to do the BLE scanning)
- clone this repo and run `npm install` in this directory—this will install noble
- run `node estimote-telemetry.js` (or other)

[njs]: https://nodejs.org/en/
[hom]: http://brew.sh/
[nob]: https://github.com/sandeepmistry/noble#prerequisites

[noble-hs]: https://github.com/sandeepmistry/noble/issues/679#issuecomment-353909458

Naturally, you'll also need some Estimote hardware broadcasting the actual packets. :satellite:

### List of Estimote packets

- **Estimote Telemetry**, used to transmit sensor and health data from the beacons. Available in most Estimote Proximity and Location Beacons. Notable exception: Proximity Beacons from 2013, with hardware revision D3.x.

- **Estimote Nearable**, a packet used to identify nearby objects ("nearables"). Estimote Stickers broadcast this packet. You can stick a Sticker onto any regular object, transforming it into a "nearable" that apps can detect.

### Questions?

For any questions, post on [Estimote Forums][ef], or email us at <contact@estimote.com>.

[ef]: https://forums.estimote.com/
