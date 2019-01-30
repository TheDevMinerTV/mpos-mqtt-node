# mpos-mqtt-node

This repo contains a backend MQTT client for MPOS-mining pools.
This project can be run as any user of a MPOS-powered mining pool.

## Configuration

The configuration file `config.json` is a JSON file. It contains all the information regarding userid, apitoken or mqtt settings.
If you leave MQTT username and token empty, it will try to login without credentials.

```json
{
    "pool": {
        "address": "https://emc2.suprnova.cc",
        "apikey": "ffa842602cvg0a097245784dd0d1869d8b2342015a75aefed1fe80aed7ed5c17",
        "userid": "423"
    },
    "mqtt": {
        "broker": "mqtt://localhost",
        "servertype": "mosquitto",
        "username": "",
        "token": "",
        "feeds": {
            "network": "emc2.network",
            "pool": "emc2.pool",
            "topusers": "emc2.topusers",
            "user": "emc2.user",
            "workers": "emc2.workers",
            "info": "emc2.info"
        }
    }
}
```

    NOTE: If servertype equals adafruit, it will automatically put a `USERNAME/feeds/` before all feed adresses.

## Some MPOS-powered mining pools

| Pool                   | Coin                                            |
| -----------------------|-------------------------------------------------|
| `<coin>.suprnova.cc*`  | Einsteinium, genx, ZCASH, DASH, LiteCoin, etc.  |
| `weminebtq.com`        | BitQuark                                        |
| `goldennoncepool.com`  | Bitcoin                                         |
| `magi.trasmamod.com`   | Magi Coin                                       |
| `<coin>.thecoin.pw*`   | Acoin, Asiccoin, Casinocoin, CHNcoin, etc.      |

    * Look on the website of the aforementioned pool (for suprnova.cc, thecoin.pw)
