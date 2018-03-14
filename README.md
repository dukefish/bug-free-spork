raspberry pi zero w connect bluetooth
sudo wpa_cli reconfigure. Use sudo reboot if you can't see connected IP in ifconfig wlan0

Install Pulse Audio: sudo apt-get install pulseaudio pulseaudio-module-bluetooth

Configuration: sudo nano /etc/bluetooth/main.conf

Add Enable=Source,Sink,Media,Socket after [General]
Configuration: sudo nano /etc/pulse/daemon.conf

exit-idle-time = 10800
sudo pulseaudio --start

sudo bluetoothctl

scan on
pair XX:XX:XX:XX:XX:XX
connect XX:XX:XX:XX:XX:XX
sudo pacmd list-sinks sudo pacmd set-default-sink bluez_sink.XX_XX_XX_XX_XX_XX.a2dp_sink
