# xiaomi-air-purifier-to-mqtt

## Usage in docker compose

```yaml
version: '3.2'
services:
  xiaomi-air-humidifier-to-mqtt:
    container_name: xah
    image: rzarajczyk/xiaomi-air-humidifier-to-mqtt:latest
    volumes:
      - ./config/xiaomi-air-humidifier-to-mqtt.yaml:/app/config.yaml
    restart: unless-stopped
```

## Configuration

```yaml
mqtt:
  broker: <hostname>
  port: <port>
  username: <username>
  password: <passqord>

xiaomi-air-humidifier:
  id: xiaomi-air-humidifier   # how will the device be identified in MQTT  
  ip: <device IP>
  token: <device token>
  fetch-interval-seconds: 5  # how often should the Monitor be pulled


```