# unifi-video-mqtt

This project is forked from https://github.com/mzac/unifi-video-mqtt

# Introduction
This image can run on your Unifi Video server and push MQTT messages to a broker when motion is detected.

This can be useful for systems like Homeassistant that are lacking motion detection integration with Unifi Video.


# Run it

```
docker run -ti --rm -v /your/path/to/unifi/logs/motion.log:/var/log/unifi-video/motion.log anderskvist/unifi-video-mqtt:latest
```

# Environment variables

`UNIFI_MOTION_LOG` - default is `/var/log/unifi-video/motion.log` (you probably don't need to change this as you need to add your logfile as a volume somewhere)
`MQTT_TOPIC_BASE` - default is `camera/motion/`
`MQTT_SERVER` - default is `192.168.1.1`
`MQTT_PORT` - default is `1883` (it's unlikely you need to change this)

`MQTT_USER` - not set by default, only required if you have auth on your MQTT
`MQTT_PORT` - not set by default, only required if you have auth on your MQTT
`MQTT_ID` - not set by default, only required if you wich to use a different MQTT ID for this client
