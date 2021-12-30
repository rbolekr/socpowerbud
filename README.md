<h1 align="center">osx-cpufreq</h1>

<p align="center">
    Get the current average CPU frequency (all cores or efficiency cores only) on MacOS.
</p>
<p align="center">
            <a href="https://github.com/BitesPotatoBacks/osx-cpufreq/releases"><img alt="Supported Architectures" src="https://img.shields.io/badge/architectures-Apple_Silicon,_Intel-default.svg"/></a><a href="https://github.com/BitesPotatoBacks/osx-cpufreq/releases"><img alt="Releases" src="https://img.shields.io/github/release/BitesPotatoBacks/osx-cpufreq.svg"/></a> <a href="https://github.com/BitesPotatoBacks/osx-cpufreq/stargazers"><img alt="Stars" src="https://img.shields.io/github/stars/BitesPotatoBacks/osx-cpufreq.svg"/></a>
    <br>
</p>

## Usage
Download the precompiled binary from the [releases](https://github.com/BitesPotatoBacks/osx-cpufreq/releases) and run it in the terminal like so:
```
./osx-cpufreq
```

The default output is formatted in hertz (Hz). Available command line options are:
```
    -k         : output in kilohertz (kHz)
    -m         : output in megahertz (mHz)
    -g         : output in gigahertz (gHz)
    -e         : get E-Cluster frequency (arm64 only)
    -v         : print version number
    -h         : help
```
If you would like to add the binary to your `usr/local/bin/`, you may run the following:
```
sudo cp ./osx-cpufreq /usr/local/bin
```

## Example

Here is an example running `./osx-cpufreq -m` in a for loop.

Output on an M1 Mac Mini:
```
829 mHz
2064 mHz
2064 mHz
1702 mHz
1333 mHz
```
Output on an Intel Macbook Pro:
```
3001 mHz
3015 mHz
3001 mHz
3008 mHz
3003 mHz
```

## Bugs and Issues
If you can't diagnose the problem yourself, feel free to open an Issue. I'll try to figure out what's going on as soon as possible.

## Credits
[https://github.com/lemire/iosbitmapdecoding/blob/master/bitmapdecoding/bitmapdecoding.cpp](https://github.com/lemire/iosbitmapdecoding/blob/master/bitmapdecoding/bitmapdecoding.cpp)

[https://github.com/somdipdey/osx-temp-freq/blob/master/smc.c](https://github.com/somdipdey/osx-temp-freq/blob/master/smc.c)
