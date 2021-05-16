
- set yours microphone
- edit /etc/pulse/default.pa
 
```sh
load-module module-echo-cancel aec_method=webrtc sink_properties=device.description="noiseless" aec_args="analog_gain_control=0 digital_gain_control=0"
set-default-source noiseless
```
> if use fedora 34 and back to pulseaudio
> ```sh
> sudo dnf swap --allowerasing pipewire-pulseaudio pulseaudio
> ```

- run 
```sh
pulseaudio -k
```
