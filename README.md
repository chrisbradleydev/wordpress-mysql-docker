# wordpress-mysql-docker

## Setup instructions

Create a directory and clone the repository to that directory.

```sh
mkdir yourdomain.com
cd yourdomain.com
git clone https://github.com/chrisbradleydev/wordpress-mysql-docker.git .
```

Replace all instances of `updateme.com` with `yourdomain.com`.

```sh
LC_CTYPE=C && LANG=C && find . -type f -not -name '*.md' -print0 | xargs -0 sed -i '' -e 's/updateme.com/yourdomain.com/g'
```

Download and unzip Wordpress.

```sh
wget https://wordpress.org/wordpress-6.2.2.zip
unzip https://wordpress.org/wordpress-6.2.2.zip
```

Copy and update env file.

```sh
cp .env.example .env
```

Run with Docker Compose.

```sh
sudo docker compose up -d
```
