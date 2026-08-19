# Bidcoin Auchash Miner

This is a simple guide to start mining Bidcoin (BID) using the Auchash algorithm.

The miner is designed primarily for CPU mining.

## Windows

Download the latest miner release and extract it to a folder.

Create a file called `mine.bat` in the miner directory:

```bat
@echo off
miner.exe --algo auchash --pool pool.example.com:3333 --wallet bid1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx --threads 8

pause
```

Replace:

```text
bid1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

with your Bidcoin wallet address.

You can also change the number of CPU threads:

```bat
--threads 8
```

For example, to use 16 CPU threads:

```bat
--threads 16
```

Run `bidcoin-miner.exe` to start mining.

## Linux

Download the miner and make it executable:

```bash
chmod +x miner
```

Start mining:

```bash
./miner --algo auchash --pool pool.example.com:3333 --wallet bid1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx --threads 8
```

Replace the example wallet address with your own BID address.

You can adjust the number of CPU threads:

```bash
./miner --algo auchash --pool pool.example.com:3333 --wallet bid1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx --threads 16
```

## Solo Mining

If the miner supports solo mining, the command can look like:

```bash
./miner --algo auchash --daemon 127.0.0.1:port --wallet bid1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx --threads 8
```

Windows example:

```bat
miner.exe --algo auchash --daemon 127.0.0.1:port --wallet bid1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx --threads 8

pause
```

## Options

| Option           | Description                              |
| ---------------- | ---------------------------------------- |
| `--algo auchash` | Use the Auchash algorithm                |
| `--pool`         | Mining pool address and port             |
| `--wallet`       | Bidcoin wallet address                   |
| `--threads`      | Number of CPU threads                    |
| `--daemon`       | Connect directly to a local Bidcoin node |

## Recommended Starting Point

For the first test, start with approximately 50-75% of your available CPU threads.

Example:

```bash
./miner --algo auchash --pool pool.example.com:3333 --wallet bid1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx --threads 8
```

Then compare hashrate, CPU temperature and power consumption before increasing the thread count.

[b]Note:[/b] Pool address, command-line parameters and the wallet address format shown above are examples. Replace them with the actual parameters provided with the Bidcoin miner release.
