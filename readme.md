ssh root@ip_address

apt update 

apt upgrade

apt install nodejs npm -y

git clone 

npm i -g pm2

pm2 start index.js

pm2 startup systemd

pm2 list

pm2 monit

// nginx reversy proxy

sudo nano /etc/nginx/sites-available/default

```
. . .
    location / {
        proxy_pass http://localhost:4000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}
```

```
sudo nginx -t
```

```
sudo systemctl restart nginx
```