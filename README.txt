Deployment Steps

1. Create dev and prod directories
2. Copy dev/docker-compose.yaml to dev and prod/docker-compose.yaml to prod
3. Clone fe/be in dev and in prod

4. Move default.conf to /etc/nginx/sites-available/default.conf

5. Install certbot standalone certificates for front end and api urls:
[frontend] sudo certbot certonly --standalone -d service.cars-done.com -d www.service.cars-done.com
[api] sudo certbot certonly --standalone -d api.service.cars-done.com -d www.api.service.cars-done.com

4. For dev, go in /root/dev and run docker compose up --build -d
5. For prod, go in /root/prod and run docker compose up --build -d