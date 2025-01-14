# conky.conf

My personal fork of [kematzys Config](https://github.com/kematzy/conky) for [Conky](https://github.com/brndnmtthws/conky).

This configuration is for **Kali Linux 2021.2** tested on a single-screen setup of a **2.560 x 1.440** monitor.

### Added Features

I really liked kematzys Design and wanted to use Conky to show information which are useful while Pentesting.
So I added these main features:

1. Dynamic network interfaces: Show interfaces which are enabled. Actually monitored: eth0. wlan0, usb0 and tun0 (inspired by [Matthias A. Lee](https://matthiaslee.com/dynamically-changing-conky-network-interface/))
2. Show open Ports (netstat). Port status is color coded: ESTABLISHED = green, LISTEN = yellow, Everything else = red
3. Show state of the entropy-pool

This is the end result:

![Kali2021.2 Conky](Kali2021.2/Conky-Kali2021.2-1440-sceen.png)

## Installation:
1. Install conky-all:
```sudo apt-get install conky-all``` 
2. Copy conky.conf and openPorts.sh to ```/home/kali/.config/conky/```
3. Start conky:
```conky``` 

### Optional: Autostart
4. Copy conky.desktop to ```/home/kali/.config/autostart/```

## Alternative CPU display:

My design have limited space for the CPU display, but if you have the space this alternative design may suit you better:

![Conky alternative CPU display](Kali2021.2/Conky-Kali2021.2-CPUs-alternative.png)

To implement this design, just copy the code below:

```lua
${font :size=11}${color1}CPUs ${color6}${hr 2}${color}
${voffset -15}
${font Montserrat Light:size=8}${color1}01:${color}${font} ${font :size=10}${goto 40}${cpu cpu1 }% ${goto 80}${color4}${cpubar cpu1  4,50}${color} ${goto 160}${font Montserrat Light:size=8}${color1}02:${color}${font} ${goto 190}${font :size=10}${cpu cpu2 }% ${goto 230}${color4}${cpubar cpu2  4,50}${color}
${font Montserrat Light:size=8}${color1}03:${color}${font} ${font :size=10}${goto 40}${cpu cpu3 }% ${goto 80}${color4}${cpubar cpu3  4,50}${color} ${goto 160}${font Montserrat Light:size=8}${color1}04:${color}${font} ${goto 190}${font :size=10}${cpu cpu4 }% ${goto 230}${color4}${cpubar cpu4  4,50}${color}
${font Montserrat Light:size=8}${color1}05:${color}${font} ${font :size=10}${goto 40}${cpu cpu5 }% ${goto 80}${color4}${cpubar cpu5  4,50}${color} ${goto 160}${font Montserrat Light:size=8}${color1}06:${color}${font} ${goto 190}${font :size=10}${cpu cpu6 }% ${goto 230}${color4}${cpubar cpu6  4,50}${color}
${font Montserrat Light:size=8}${color1}07:${color}${font} ${font :size=10}${goto 40}${cpu cpu7 }% ${goto 80}${color4}${cpubar cpu7  4,50}${color} ${goto 160}${font Montserrat Light:size=8}${color1}08:${color}${font} ${goto 190}${font :size=10}${cpu cpu8 }% ${goto 230}${color4}${cpubar cpu8  4,50}${color}
${font Montserrat Light:size=8}${color1}09:${color}${font} ${font :size=10}${goto 40}${cpu cpu9 }% ${goto 80}${color4}${cpubar cpu9  4,50}${color} ${goto 160}${font Montserrat Light:size=8}${color1}10:${color}${font} ${goto 190}${font :size=10}${cpu cpu10}% ${goto 230}${color4}${cpubar cpu10 4,50}${color}
${font Montserrat Light:size=8}${color1}11:${color}${font} ${font :size=10}${goto 40}${cpu cpu11}% ${goto 80}${color4}${cpubar cpu11 4,50}${color} ${goto 160}${font Montserrat Light:size=8}${color1}12:${color}${font} ${goto 190}${font :size=10}${cpu cpu12}% ${goto 230}${color4}${cpubar cpu12 4,50}${color}
${voffset -12}
```


### CONKY MAN PAGE

A quick and dirty conversion of Conky's `man` page is enclosed for reference of Conky's various settings and features.

[Conky Man Page](/Conky-Man-Page.md)


## LICENCE

MIT or Do Whatever You Want 

IF it breaks on your system, then just work it out yourself. No warranty expressed or implied and no support provided.

Have a great life.

