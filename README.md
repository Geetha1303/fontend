# Frontend

The frontend is the service in RobotShop to serve the web content over Nginx.

To Install Nginx.

```
# apt update
# apt install nginx -y
# systemctl enable nginx 
# systemctl start nginx 
```

Let's download the HTDOCS content and deploy under the Nginx path.

```
# curl -s -L -o /tmp/frontend.zip "https://github.com/zelar-soft-roboshop/frontend/archive/main.zip"
```

Deploy in Nginx Default Location.

```
# rm -rf /var/www/html /etc/nginx/sites-enabled/default /etc/nginx/sites-available/default
# cd /var/www
# unzip /tmp/frontend.zip
# mv frontend-main/* .
# mv static html
# rm -rf frontend-main README.md
# mv roboshop.conf /etc/nginx/sites-enabled//roboshop.conf
```

Finally restart the service once to effect the changes.

```
# systemctl restart nginx 
```


Working App Screenshorts.

![image](https://user-images.githubusercontent.com/29029753/114181910-b7d40380-995f-11eb-8d9f-16e11c38e37d.png)

![image](https://user-images.githubusercontent.com/29029753/114181944-befb1180-995f-11eb-8918-78c2801b5469.png)

![image](https://user-images.githubusercontent.com/29029753/114181981-c5898900-995f-11eb-9206-1cf97431d44b.png)

![image](https://user-images.githubusercontent.com/29029753/114182013-cde1c400-995f-11eb-8847-1a736352682a.png)

![image](https://user-images.githubusercontent.com/29029753/114182026-d20de180-995f-11eb-9b82-04807d4bf8ea.png)


;;