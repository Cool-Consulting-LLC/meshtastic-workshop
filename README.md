# Meshtastic Workshop resources

Please install the following before attending the workshop!

## Step 1: Chrome

Please install a Chrome-based browser; it's needed to access a serial connection to the device the workshop will provide.

## Step 2: Serial Drivers

Install the [CP210x serial drivers](https://meshtastic.org/docs/getting-started/serial-drivers/esp32/).

## Step 3: Clone this repo

Please clone this repo and then navigate to the folder you've cloned in your terminal before running Step 4.

## Step 4: Python tooling

There are two ways to configure the Python resources you'll need for the workshop. If you've never sued Python before, we recommend using UV to manage your Python installation and dependencies. If you've used Python before, skip to the pure Python directions.

## Python UV

### Step A

[Install UV](https://docs.astral.sh/uv/getting-started/installation/) per their guide for your operating system.

### Step B

Run the following commands in your terminal:

```
$ uv python install 3.13.1
$ uv sync --python 3.13.1
```

### Step C
Run the following commands in your termainl to verify installation worked:

```
$ uvx python3 --version
Python 3.13.1

$ uvx meshtastic --version
2.7.7

$ uvx platformio --version
PlatformIO Core, version 6.1.19

$ uvx esptool version
esptool v5.2.0
5.2.0
```

## Pure python setup

### Step A

First, ensure you have python installed on your system. [The guide on Real Python](https://realpython.com/installing-python/) is good if you've never installed python before (but we recommend using UV if you haven't!). Follow the directions for your operating system.

Please be sure you've installed Python v3.13.1.

### Step B

Once you have python installed, run the following commands.

```
$ python3 -m venv venv
$ source venv/bin/activate   # or venv\Scripts\activate on Windows
$ pip3 install -r requirements.txt
```

This creates a `venv` of all the required tooling for our workshop:

1. `protobuf` v4.25.8
1. [Meshtastic CLI](https://meshtastic.org/docs/software/python/cli/)
1. [PlatformIO Core](https://docs.platformio.org/en/latest/core/installation/index.html)
1. [`esptool`](https://pypi.org/project/esptool/)

Every time you start a new shell session, navigate to this folder and run the second command above to access these command line tools.

### Step C

By the end of this setup process, you should be able to verify the tooling by running:

```
$ python3 --version
Python 3.13.1

$ meshtastic --version
2.7.7

$ pio --version
PlatformIO Core, version 6.1.19

$ esptool version
esptool v5.1.0
5.1.0
```
