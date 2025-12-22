Deployment Steps

0. Clone Artifacts.CarService in /root/
1. Create dev and prod directories in /root/
2. Copy dev/docker-compose.yaml to dev and prod/docker-compose.yaml to prod
3. Clone fe/be in dev and in prod

4. Move default.conf to /etc/nginx/sites-available/default.conf

5. Install certbot standalone certificates for front end and api urls:

[frontend prod] sudo certbot certonly --standalone -d service.cars-done.com -d www.service.cars-done.com
[api prod] sudo certbot certonly --standalone -d api.service.cars-done.com -d www.api.service.cars-done.com

[frontend dev] sudo certbot certonly --standalone -d dev.service.cars-done.com -d www.dev.service.cars-done.com
[api dev] sudo certbot certonly --standalone -d dev.api.service.cars-done.com -d www.dev.api.service.cars-done.com

4. For dev, go in /root/dev and run docker compose up --build -d
5. For prod, go in /root/prod and run docker compose up --build -d

6. Start common nginx from /root/Artifacts.CarService/nginx with docker compose up --build -d