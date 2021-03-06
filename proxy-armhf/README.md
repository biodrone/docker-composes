# Proxy ARMHF

Use this for Raspberry Pi 3/4 or any other armhf platform.

# Proxying Containers

Any container that you wish to be proxied just needs the VIRTUAL_HOST environment variable adding to it. LetsEncrypt requires the LETSENCRYPT_HOST variable and you can provide the LETSENCRYPT_EMAIL variable (optional) to receive emails about certificate expiry.
```
VIRTUAL_HOST=sub.domain.com
LETSENCRYPT_HOST=sub.domain.com
LETSENCRYPT_EMAIL=test@test.com
```

By default, whatever port is exposed by your container will be proxied. If you are exposing multiple ports, you can use the below to specify which one to proxy.
```
VIRTUAL_PORT=9443
```

# Usage

```
docker-compose build
docker-compose up -d
```

For more in depth usage details, see https://github.com/jwilder/nginx-proxy
