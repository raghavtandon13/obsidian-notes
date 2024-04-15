1   server{
  1   server_name 3.27.146.211;
  2
  3       location /api {
  4         proxy_pass http://localhost:5000;
  5         proxy_http_version 1.1;
  6         proxy_set_header Upgrade $http_upgrade;
  7         proxy_set_header Connection 'upgrade';
  8         proxy_set_header Host $host;
  9         proxy_cache_bypass $http_upgrade;
 10     }
 11
 12       location / {
 13         proxy_pass http://localhost:3000;
 14         proxy_http_version 1.1;
 15         proxy_set_header Upgrade $http_upgrade;
 16         proxy_set_header Connection 'upgrade';
 17         proxy_set_header Host $host;
 18         proxy_cache_bypass $http_upgrade;
 19     }
 20 }
 21
~                                                                                                                           ~                                                                                                                           ~                                                                                                                           ~                                                                                                                           ~                                      