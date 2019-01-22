# masternode-miner

![Latest Version][ico-version]
![Software License][ico-license]
![Style CI][ico-styleci]

> **THIS SOFTWARE IS OBSOLETE AND SHOULD NOT BE USED!**
>
> For an official masternode guide, [click here][link-masternode-setup-guide].

The deprecated masternode miner for the Arionum cryptocurrency.

## Install

#### Requirements

1. 8 GB RAM
2. 100GB+ DISK SPACE (SSD)
3. 4 CPU Cores
4. 100,010 ARO

#### Important Information

- The cost of a masternode is 100,000 ARO (plus a 10 ARO creation fee)
- The funds are locked for a minimum of 3 Months
- To release the funds, the miner must be paused for 1 month
- Block winners are chosen in order, therefore all masternodes will receive a reward
- The IP must remain accessible for the duration of the masternode

## Usage

1. Create a new wallet using the [command-line wallet][link-arionum-cli]
1. Send 100,010 ARO to a newly created masternode address
1. The node must be accessible on IP + port 80 (e.g. http://1.1.2.2)
1. Edit the `config.inc.php`, set `masternode` to `true` and the `masternode_public_key` to the wallet's public key
1. Download the [`masternode-miner`](./masternode-miner) to a secure location on the same server
1. Create a keypair `.env` file in the format shown below
1. Create a cron task to run `masternode-miner` every minute
1. Using the command-line wallet, run the command: `arionum masternode:create 'ip'`
1. After 360 blocks, the masternode will start mining

**Create a Cron task**

```cron
* * * * * /etc/arionum-mn/miner >/dev/null
```

**Environment file format**

- Public key
- Private key
- Node address (e.g. `https://10.0.1.1`)

## License

The MIT License (MIT).

[ico-version]: https://img.shields.io/badge/status-deprecated-red.svg?style=flat-square
[ico-license]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square
[ico-styleci]: https://styleci.io/repos/143841461/shield

[link-arionum-cli]: https://github.com/pxgamer/arionum-cli
[link-masternode-setup-guide]: https://forum.arionum.com/viewtopic.php?f=13&t=367
