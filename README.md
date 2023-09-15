# OBS Stats Overlay
Simple OBS websocket stats overlay without external libraries.

Written for the specific purpose of monitoring the output and performance of a number of OBS instances on a local network, using OBS as a multiviewer for those instances. In my use case the streams are received via RTMP, but they could be NDI, SRT or anything else that OBS supports.

* Includes support for OBS Multi-RTMP plugin (https://github.com/sorayuki/obs-multi-rtmp/).
* Typically used in combination with OBS Waveform plugin to provide a peak meter (https://github.com/phandasm/waveform/).

I'm not a developer, merely a hacker, so this code does not aspire to be efficient or beautiful, just functional and self-contained.

# Usage

* Add the obs-statsoverlay.html file into OBS using the Browser Source. To use it from a local disk you MUST specify the path using file:/// and not browse for the file.
* Set the Browser Source resolution to match your OBS canvas resolution.
* By default connects to 127.0.0.1 as a test. Specify the OBS host on the network by appending ?host=x.x.x.x to the URL.
* An optional name overlay can be specified by further appending &name=yourname to the URL.
* By default updates every 5 seconds. Value can be adjusted by editing the ```updateInterval``` variable in the script.

Example:
```
file:///C:/Users/User1/Documents/obs-statsoverlay.html?host=192.168.0.11&name=Instance 1
```


# Example image

With streaming, multi-RTMP streaming and recording in progress, and with the Waveform plugin added.

![overlay-example](https://github.com/rob-fi/obs-statsoverlay/assets/1683665/e531d723-8bef-4e15-b70a-2d38b456c490)
