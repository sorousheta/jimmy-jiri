# jimmy-jiri

Here's a comprehensive README.md file generated from the content of the provided link. This file includes the full content of the link in Markdown format.

```markdown
# نصب و فعال سازی کلیه نرم افزارهای شرکت Atlassian بر روی داکر

## مقدمه

نرم‌افزارهای شرکت Atlassian با یکپارچگی کامل، امکانات بی‌نظیری را در اختیار کاربران قرار می‌دهند و می‌توانند کل فرایندهای یک شرکت را مدیریت کنند. این نرم‌افزارها چرخه CI/CD را در بالاترین سطح و کیفیت ممکن به وجود می‌آورند.

## نصب داکر و داکر کامپوز

### نصب Docker
```sh
curl -sS https://get.docker.com/ | sh
```

### نصب Docker-compose
```sh
curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
```

برای اطمینان از نصب درست:
```sh
docker --version
docker-compose --version
```

## شروع نصب نرم‌افزارها

ابتدا مخزن گیت را کلون کنید:
```sh
git clone https://github.com/beigi-reza/atlassian-software.git
```
وارد شاخه ایجاد شده شوید و شبکه Docker را ایجاد کنید:
```sh
cd atlassian-software
docker network create --driver bridge --subnet=150.50.50.0/24 my-net
```

## نصب و راه‌اندازی نرم‌افزارها

### Jira
```sh
docker-compose -f jira-compose.yml up -d
```
در مرورگر، به آدرس `http://<IP>:8080/` بروید.

### Jira Service Management
```sh
docker-compose -f servicemanagement-compose up -d
```
در مرورگر، به آدرس `http://<IP>:8080/` بروید.

### Confluence
```sh
docker-compose -f confluence-compose.yml up -d
```
در مرورگر، به آدرس `http://<IP>:8090/` بروید.

### Bitbucket
```sh
docker-compose -f bitbucket-compose.yml up -d
```
در مرورگر، به آدرس `http://<IP>:7990/` بروید.

### Bamboo
```sh
docker-compose -f bamboo-compose.yml up -d
```
در مرورگر، به آدرس `http://<IP>:8085/` بروید.

### Fisheye & Crucible
```sh
docker-compose -f fisheye-compose.yml up -d
```
در مرورگر، به آدرس `http://<IP>:8088/` بروید.

## فعال‌سازی کلیه نرم‌افزارها

برای فعال‌سازی نرم‌افزارها، مراحل زیر را دنبال کنید:
1. اطلاعات مورد نیاز را در صفحات فعال‌سازی وارد کنید.
2. از فرمان‌های زیر برای دریافت لایسنس استفاده کنید:
    - Jira
    ```sh
    docker exec jira java -jar /atlassian-agent.jar -d -m r.beigy@gmail.com -o reza-beigi -p jira -s <ServerID>
    ```
    - Jira Service Management
    ```sh
    docker exec jira java -jar /atlassian-agent.jar -d -m r.beigy@gmail.com -o reza-beigi -p jsm -s <ServerID>
    ```
    - Confluence
    ```sh
    docker exec jira java -jar /atlassian-agent.jar -d -m r.beigy@gmail.com -o reza-beigi -p conf -s <ServerID>
    ```
    - Bitbucket
    ```sh
    docker exec jira java -jar /atlassian-agent.jar -d -m r.beigy@gmail.com -o reza-beigi -p bitbucket -s <ServerID>
    ```
    - Bamboo
    ```sh
    docker exec jira java -jar /atlassian-agent.jar -d -m r.beigy@gmail.com -o reza-beigi -p bamboo -s <ServerID>
    ```
    - Fisheye
    ```sh
    docker exec jira java -jar /atlassian-agent.jar -d -m r.beigy@gmail.com -o reza-beigi -p fisheye -s <ServerID>
    ```
    - Crucible
    ```sh
    docker exec jira java -jar /atlassian-agent.jar -d -m r.beigy@gmail.com -o reza-beigi -p crucible -s <ServerID>
    ```
    - Jira Core
    ```sh
    docker exec jira java -jar /atlassian-agent.jar -d -m r.beigy@gmail.com -o reza-beigi -p js -s <ServerID>
    ```

## نصب و فعال‌سازی پلاگین‌ها

برای نصب و فعال‌سازی پلاگین‌ها:
1. پلاگین را از سایت [marketplace.atlassian.com](https://marketplace.atlassian.com) دانلود کنید.
2. فرمان زیر را اجرا کنید:
```sh
docker exec jira java -jar /atlassian-agent.jar -p <...> -m r.beigy@gmail.com -o reza-beigi -s <ServerID>
```

امیدوارم این آموزش مفید بوده باشد و بتوانید از نرم‌افزارهای قدرتمند شرکت Atlassian نهایت استفاده را ببرید.

[لینک اصلی](https://virgool.io/@r.beigy/نصب-و-فعال-سازی-کلیه-نرم-افزارهای-شرکت-atlassian-oclfipois9qk)
```

شما می‌توانید این فایل را ذخیره کرده و در محیط مورد نظر خود استفاده کنید.
