# CPUPower Utility Installation Guide for Ubuntu

This guide provides instructions on how to install and use the `cpupower` utility on Ubuntu systems. The `cpupower` utility is used to manage CPU frequency settings, including setting the CPU governor to `performance` mode.

## Prerequisites

- Ubuntu operating system
- Access to a terminal
- Sudo privileges

## Installation

### Step 1: Identify Your Kernel Version

To find your current kernel version, open your terminal and run:

```bash
uname -r
```

This command will output your current kernel version, which looks something like `5.4.0-42-generic`.

### Step 2: Install Matching Linux Tools
Install the linux-tools package that matches your kernel version:

```bash
sudo apt install linux-tools-$(uname -r)
```

This command automatically selects and installs the correct version of linux-tools for your kernel.

### Step 3: Verify Installation
After the installation, verify that cpupower is installed successfully:

```bash
sudo cpupower frequency-set --governor performance
```

### Usage

The cpupower utility can be used to manage CPU frequency settings. For example, to set the CPU governor to performance mode, use:

```bash
sudo cpupower frequency-set --governor performance
```

This sets the CPU to run at maximum performance.
