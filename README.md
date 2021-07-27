# example-oathkeeper
Example about oathkeeper, using with nginx

# Steps to run on MacOS:
* Update self-signed ssl keys:

`
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout nginx/ssl/nginx.key -out nginx/ssl/nginx.crt
`

* Start docker compose:

`
docker-compose up -d
`

* Open `https://127.0.0.1/`, it'll redirect and open `https://127.0.0.1/auth/login?flow=<flow-id>`


# Notes
* Because using self-signed certs, if you're using Chrome, please type `thisisunsafe` to bypass checking from Chrome
