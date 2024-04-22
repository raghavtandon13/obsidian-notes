# current nginx conf
```nginx
server {
    server_name 3.27.146.211;

    location /api {
        proxy_pass http://localhost:5000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }

     location / {
         proxy_pass http://localhost:3000;
         proxy_http_version 1.1;
         proxy_set_header Upgrade $http_upgrade;
         proxy_set_header Connection 'upgrade';
         proxy_set_header Host $host;
         proxy_cache_bypass $http_upgrade;
     }
}

```
# new with vercel and server_name
```nginx
server {
    server_name credmantra.com;

    location /api {
        proxy_pass http://localhost:5000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }

    location / {
        proxy_pass https://cred-front.vercel.app;
        proxy_redirect off;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }
}
```
# conf with subdomain settings and direct ip access restriction
```nginx
server {
    listen 80 default_server;
    server_name _;

    return 444;
}

server {
    listen 80;
    server_name credmantra.com;

    location /api {
        proxy_pass http://localhost:5000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }

    location / {
        proxy_pass https://cred-front.vercel.app;
        proxy_redirect off;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }
}

server {
    listen 80;
    server_name admin.credmantra.com;
    
    location / { 
	    proxy_pass https://next-cred.vercel.app;
	    proxy_redirect off;
	    proxy_set_header X-Real-IP $remote_addr;
	    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
	}
}
```

>[!Reload nginx]
>sudo systemctl reload nginx

# Notes
- admin.credmantra.com not working 
- DNS issue might be fixed if a_record for admin subdomain is added to hostinger
```nginx

server {                                                                                             listen 80 default_server;                                                                        server_name _;                                                                                                                                                                                    return 444;                                                                                  }                                                                                                server {                                                                                             listen 80;                                                                                       server_name www.credmantra.com;                                                                                                                                                                   return 301 $scheme://credmantra.com$request_uri;                                             }                                                                                                server {                                                                                             listen 80;                                                                                       server_name credmantra.com;                                                                                                                                                                       location /api {                                                                                      proxy_pass http://localhost:5000;                                                                proxy_http_version 1.1;                                                                          proxy_set_header Upgrade $http_upgrade;                                                          proxy_set_header Connection 'upgrade';                                                           proxy_set_header Host $host;                                                                     proxy_cache_bypass $http_upgrade;                                                            }                                                                                                location / {                                                                                         proxy_pass http://localhost:3000;                                                                proxy_http_version 1.1;                                                                          proxy_set_header Upgrade $http_upgrade;                                                          proxy_set_header Connection 'upgrade';                                                           proxy_set_header Host $host;                                                                     proxy_cache_bypass $http_upgrade;                                                            }                                                                                            }                                                                                                ~                                                                                                ~     
```