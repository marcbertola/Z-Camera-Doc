## Resolution & Framerate

### Normal Dynamic Range

| Record Mode | 3840x2160 4K(Low Noise) | 4096x2160 C4K(Low Noise))| 1920x1080 16:9 HD | 3696x2772 4:3 Anamorphic | 3840x2160 16:9 4K/UHD | 4096x2160 17:9 C4K/DCI4K | 3312x2760 6:5  |
| :---        | :---:             | :--:                 | :---:             | :--:                     | :--:                  | :--:                     | :--:           |
| 23.98(NTSC) | 20,21,22,23,24 | 20,21,22,23,24 | 20,21,22,23,24,48,60,72,84,96,108,120,240 | 20,21,22,23,24,48,60 | 20,21,22,23,24,48,60,72,84,96,108,120 | 20,21,22,23,24,48,60,72,84,96,108,120 | 20,21,22,23,24,48,60 |
| 24(Cinema) | 20,21,22,23,24 | 20,21,22,23,24| 20,21,22,23,24,48,60,72,84,96,108,120,240 | 20,21,22,23,24,48,60 | 20,21,22,23,24,48,60,72,84,96,108,120 | 20,21,22,23,24,48,60,72,84,96,108,120 | 20,21,22,23,24,48,60 |
| 25(PAL) | 25 | 25 | 25,50,75,100,120,200,240 | 25,50 | 25,50,75,100,120 | 25,50,75,100,120 | 25,50 |
| 29.97(NTSC) | 30 | 30 | 30,60,120,240 | 30,45,60 | 30,45,60,75,90,105,120 | 30,45,60,75,90,105,120 | 30,45,60 |
| 50(PAL) | - | - | 25,50,75,100,120,200,240 | 25,50 | 25,50,100,120 | 25,50,100,120 | 25,50 |
| 59.94(NTSC) | - | - | 30,60,120,240 | 30,60 | 30,60,120 |  30,60,120 | 30,60 |

### Wide Dynamic Range

| Record Mode | 1920x1080 16:9 HD | 3696x2772 4:3 Anamorphic | 3840x2160 16:9 4K/UHD | 4096x2160 17:9 C4K/DCI4K | 3312x2760 6:5  |
| :---        | :---:             | :--:                     | :--:                  | :--:                     | :--:           |
| 23.98(NTSC) | 20,21,22,23,24,48 | 20,21,22,23,24,48 | 20,21,22,23,24,48 | 20,21,22,23,24,48 | 20,21,22,23,24,48 |
| 24(Cinema) | 20,21,22,23,24,48 | 20,21,22,23,24,48 | 20,21,22,23,24,48 | 20,21,22,23,24,48 | 20,21,22,23,24,48 |
| 25(PAL) | 25,50 | NA | 25,50 | 25,50 | NA |
| 29.97(NTSC) | 30,60 | NA | 30,60 | 30,60 | NA |
| 50(PAL) | 25,50 | NA | 25,50 | 25,50 | NA |
| 59.94(NTSC) | 30,60 | NA | 30,60 |  30,60 | NA |

## Video Encoder

| Frame Rate | H.264 | H.265 | ProRes 422 |
| :--- | :---: | :--: | :--:|
| FR <= 30 | Y | Y (10bit 420) | Check next section |
| 30 < FR <= 60 | N | Y (10bit 420) | Check next section |
| 60 < FR <= 120 | N | Y (10bit 420) | Check next section |
| 120 < FR | N | Y (8bit 420) | Check next section |

*Chroma sample is 4:2:0 for H.264/H.265; 4:2:2 for ProRes*

## ProRes

| Record Mode | 3840x2160 4K(Low Noise) | 4096x2160 C4K(Low Noise))| 1920x1080 16:9 HD | 3696x2772 4:3 Anamorphic |  3312x2760 6:5  | 3840x2160 16:9 4K/UHD | 4096x2160 17:9 C4K/DCI4K |
| :---        | :---:                   | :--:                     | :---:             | :--:                     | :--:                  | :--:                     | :--:           |
| ProRes 422 Proxy| fps <= 30               | fps <= 30                | fps <= 120        | fps <= 60                | fps <= 60      | fps <= 60             | fps <= 60                |
| ProRes 422 LT   | fps <= 30               | fps <= 30                | fps <= 120        | fps <= 60                | fps <= 60      | fps <= 60             | fps <= 60                |
| ProRes 422  | fps <= 30               | fps <= 30                | fps <= 120        | fps <= 48                | fps <= 48      | fps <= 60             | fps <= 48                |
| ProRes 422 HQ   | fps <= 30               | fps <= 30                | fps <= 100        | fps <= 30            |   fps <= 30      | fps <= 30             | fps <= 30                |

*fps >= 100, the maxinum output of HDMI is 1080p60*

*4k 48<fps<=60, ProRes 422, the maxinum output of HDMI is 1080p60*

### H.265/H.264 bitrate
| Resolution | FR | High(Mbps) | Medium(Mbps) | Low(Mbps) |
|:-- | :--: | :--: | :--: |:--:|
| 4K | FR <=30 | 200 | 130 | 60 |
| 4K | 30 < FR <= 60 | 230 | 150 | 100 |
| 4K | 60 < FR | 300 | 200 | 160 |
| 1080P | FR <=30 | 30 | 20 | 10 |
| 1080P | 30 < FR <= 60 | 60 | 30 | 15 |
| 1080P | 60 < FR | 200 | 130 | 60 |

## HDMI Resolution
| Capture FR | HDMI (Max.) |
|:-- | :--: |
| FR <= 60 | 4K@60fps 10bit 4:2:2 |
| 60 < FR | 1080@60fps 8bit 4:2:0 |

## Audio Encoder
| File Format | AAC | PCM | None |
|:-- |:--:|:--:|:--:|
| MOV | Y | Y | Y |
| MP4 | Y | N | Y |

If you don't want to record the audio, you can choose None.

## Battery Life
Based on a fully charged NP-F970.

| Resolution | VFR | Duration |
| :-----|:----- | :-----|
| 4KP30 | OFF | 330min |
| 4KP30 | 120 | 200min |

## Control the camera
### HTTP based control
see [HTTP Protocol](http.md)
#### Ethernet
The Ethernet work in these 3 modes:

- Router, you can plug the E2 into your router, E2 get IP from your router.
- Direct, the E2 work as DHCP server, it assign IP to the client. IP is 10.98.32.1
- Static, use the cfg file in storage card(/MISC/cfg) to setup the static IP.

    eth.ipaddr=192.168.8.8

    eth.netmask=255.255.255.0

    eth.gateway=192.168.8.1

#### USB
The USB port can work as RNDIS, it work with a DHCP server which assign IP to your computer.

Windows/Mac/Linux has buildin driver for RNDIS device. Once you install the driver, you can access the camera with IP 172.18.18.1.

#### WiFi
The WiFi in E2 work as a Access Point, connect your computer/smart phone to E2 to get the IP and access the camera. IP is 10.98.33.1.

#### Find out the IP of camera
- If you can use the menu of the camera, you can find the IP in the 'Connect' menu.
- If your computer is in the same network of E2, you can use [Multicast DNS](https://en.m.wikipedia.org/wiki/Multicast_DNS)(e.g. [Bonjour](https://en.m.wikipedia.org/wiki/Bonjour_(software)#Bonjour_Browser)) to find out the IP.

### LANC
It's compatible with [SONY's LANC](http://www.boehmel.de/lanc.htm).

### Serial port
TTL & RS232 level are supported

## Overlay
### Exposure
#### Zebra
We support two Zebra settings:
- over exposure
- under exposure 

#### False Color
![False Color](false_color.jpg)

We provide this feature both on iOS app and camera.

*Suggestion: Make the skin tone/mid-gray to be green(around 0.4), you can get a better result with zlog:)*

### Peak
We provide this feature both on iOS app and camera.

## Multiple camera sync
E2 can do the pixel-synced recording. Cameras work in a chained connection. One master camera and multiple slave cameras. The master will generate the sync signal to all of the slave camera.

Master camera <-> Slave camera 1 <-> Slave camera 2 <-> Slave camera3 <-> ...

### Hardware
1. Sync connector, it contains input and output ports. Contact our sales to buy it.
2. CAT6 or better Ethernet cables.

### Steps

There is a switcher in the battery socket with a lable M/I/S. M: Master, I: single camera, S: Slave.

1. Set switcher to I, power on the camera. Set up the Movie Format and VFR for every camera. All of the cameras should use the same movie format and VFR.
2. Long press power button to power off the camera, set switcher to M or S.
3. Connect the camera in chain, make sure the output port is linked to the input port.
4. Power up the cameras.
5. Before recording, please make sure the free space of the cameras are similar.
6. You can set up the shutter speed to the same value to get a better performance.
7. Press the RECORD button on the Master camera to start multi-camera recording.

On the GUI, you can find out the role under the menu:

    Connect -> Multi Camera
