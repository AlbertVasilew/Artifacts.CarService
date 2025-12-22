Deployment Steps

1. Move default.conf to /etc/nginx/sites-available/default.conf
2. Clone backend and front end repos

3. Install certbot standalone certificates for front end and api urls:
[frontend] sudo certbot certonly --standalone -d service.cars-done.com -d www.service.cars-done.com
[api] sudo certbot certonly --standalone -d api.service.cars-done.com -d www.api.service.cars-done.com

4. Run docker compose up --build -d