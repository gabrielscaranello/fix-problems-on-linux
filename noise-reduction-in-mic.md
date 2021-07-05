
- set yours microphone
- edit /etc/pulse/default.pa


> If you are using fedora 34 and want to switch back to using pulseaudio instead of pipewire 
> ```sh
> sudo dnf swap --allowerasing pipewire-pulseaudio pulseaudio
> ```
 
```sh
load-module module-echo-cancel aec_method=webrtc sink_properties=device.description="noiseless" aec_args="analog_gain_control=0 digital_gain_control=0"
set-default-source noiseless
```


- run 
```sh
pulseaudio -k
```
