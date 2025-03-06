# ADS-B Dataset for SDR Applications

An ADS-B dataset created through utilizing a HackRF One Software Defined Radio and a publicly available Mode-S decoder known as Dump1090_sdrplus, a forked version of the main Dump1090 with a focus on Software Defined Radio useablility (see the full project at https://github.com/itemir/dump1090_sdrplus).

## Setup

This setup process follows the installation and setup process on the Dump1090_sdrplus GitHub page.

In Linux or a Linux shell program, clone the Dump1090_sdrplus repository as follows:

```
git clone git@github.com:itemir/dump1090_sdrplus.git
cd dump1090_sdrplus
make
```

After the Dump1090_sdrplus repository has been cloned entered, type the following command:

```
sudo apt-get install librtlsdr0 librtlsdr-dev libhackrf-dev libairspy-dev libsoxr-dev
```

For this dataset, we will not be utilizing the SDRPlay capabilities of the Dump1090_sdrplus package. To disable this setting, use the following command:

```
make NoSDRplay=1
```

This repository can be run using the following commands, where the first command runs the decoder as normal, the second command runs the decoder in a menu that recursively adjusts the decoded ADS-B data being observed, and the third command adds a CSV output log to the interactive decoder.

```
./dump1090

./dump1090 --interactive

./dump1090 --interactive --csv-log
```
