# Podman Compose Setup For Installing Vaultwarden

This configuration creates database and SSL reverse proxy containers for Vaultwarden.

Detailed info: [Tom's IT Cafe article on https://tomsitcafe.com](https://tomsitcafe.com/2023/12/08/how-to-install-vaultwarden-password-manager-in-podman/)

## Prerequisite

- Podman
- Internet connection
- A domain name
- Cert and Key
- Coffee

## .env file example

```ini
MYSQL_ROOT_PASSWORD=<root pw>
MYSQL_PASSWORD=<user pw>
MYSQL_DATABASE=<db>
MYSQL_USER=<user>

DATABASE_URL=mysql://<user>:<user pw>@vw_database/<db>
```

## Usage

Place the certificate and key file in the `certs` folder of the project directory.

Start the services:

```bash
podman-compose up -d
```

## Author

Tamas Molnar - <tmolnar0831@gmail.com> - [https://tomsitcafe.com](https://tomsitcafe.com)
