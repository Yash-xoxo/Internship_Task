## On Host (Linux Desktop)
### 1. Allow PulseAudio access from the container:
Run this to allow local Docker containers to connect:

bash

```pactl load-module module-native-protocol-tcp auth-anonymous=1```

### 2. Expose PulseAudio socket to Docker container
#### Run your container with:
```
docker run -it \
  --env PULSE_SERVER=unix:/tmp/pulse-socket \
  -v ~/.config/pulse/cookie:/root/.config/pulse/cookie \
  -v /run/user/1000/pulse/native:/tmp/pulse-socket \
  -v /dev/snd:/dev/snd \
  --device /dev/snd \
  your-image-name
```
