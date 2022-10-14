# ese5190Lab2_SDKGuide 
(Reference to https://datasheets.raspberrypi.com/pico/getting-started-with-pico.pdf Section 9)

(Reference to YuChen Wang: https://github.com/YuchenWang0303/Documentation-of-M1-MacBook-to-use-QT-PY-2040-)

## Laptop Info:
	MacBook Pro (14-inch, 2021)
	System: MacOS Monterey Version 12.6
	Chip: Apple M1 Pro

## Software List
1. HomeBrew
2. cmake
3. ArmMbed/homebrew-formulae
4. arm-none-eabi-gcc
	

## Step 1 Using X86 Terminal on M1 Pro chip
1. Duplicate a new Terminal from the Application Folder.
2. Name the new Terminal as "Terminal_X86". 
3. Right click to open its “Get Info” pane and check the box for “Open using Rosetta.”

<img width="1029" alt="WechatIMG5" src="https://user-images.githubusercontent.com/114244957/195737554-85f9d637-69af-4841-999d-3059788928f3.png">

In this way, we can run the command in Intel architecture.

## Step 2 Install Homebrew and required packages
1. Change the shell from zch to bash
2. Copy and paste the following command and hit Enter

```
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

3. After a while, you will see a line: "Installation Successful!" This means Homebrew is installed on our system.
4. Put in the following commands each by each to install the necessary package for this lab (cmake, ArmMbed/homebrew-formulae, and arm-none-eabi-gcc)

```
$ brew install cmake
$ brew tap ArmMbed/homebrew-formulae
$ brew install arm-none-eabi-gcc
```

5. Type ```brew list``` to check that all packages are installed.

![WX20221013-210131](https://user-images.githubusercontent.com/114244957/195738671-80cc8ec9-4f6f-4da6-beb4-de81fe4af9dd.png)

## Step 3 Get the SDK and examples (Setup Guide Section 2.1 & 2.3)
1. Create a pico dictionary to put the examples
```
$ cd ~/
$ mkdir pico
$ cd pico
```
2. Clone the ```pico-sdk``` and ```pico-examples``` git repositories
```
$ git clone -b master https://github.com/raspberrypi/pico-sdk.git
$ cd pico-sdk
$ git submodule update --init
$ cd ..
$ git clone -b master https://github.com/raspberrypi/pico-examples.git
```
3. In the future, we can use the following commands to upate SDK and sunmodules
```
$ cd pico-sdk
$ git pull
$ git submodule update
```

## Step 4 Compile and Print "Hello World!"

























