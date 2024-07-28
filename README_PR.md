اینجا ما تعدادی تمپلیت برای صفحه هوم مرزبان داریم که می‌توانید از آنها استفاده کنید. لیست تمپلیت‌ها شامل موارد زیر است:

- انتقال
  
با این تمپلیت بازدیدکنندگان دامنه‌ی شما مستقیم به یک صفحه‌ی وبسایت دیگه که شما مشخص میکنید انتقال داده میشود.

- رندوم
  
با این تمپلیت بازدیدکنندگان دامنه‌ی شما عکس رندوم مشاهده میکنند که خیال کنند یک وبسایت تصویر هست.

- آی فریم
  
با این تمپلیت بازدیدکنندگان دامنه‌ی شما در صفحه‌ی Home شما با آدرس دامنه‌ی شما یک صفحه‌ی وبسایت که مشخص کردید نمایش داده میشود و میتوانند باهاش کار کنند.

- فیک
  
با این تمپلیت بازدیدکنندگان دامنه‌ی شما یه گیف زشت مشاهده میکنند. :/


برای تمپلیت‌های بیشتر می‌توانید به پروژه ستاره بدهید. ⭐ چنل تلگرام من : [@ErfJabs](https://t.me/erfjabs)


## نصب

قبل از شروع نصب، دستور زیر را در سرور خود وارد کنید:

```
apt install wget
```

سپس این دستورات را وارد کنید:

```
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'HOME_PAGE_TEMPLATE="home/index.html"' | sudo tee -a /opt/marzban/.env
```

حالا تمپلیتی که می‌خواهید را انتخاب کنید و طبق تنظیمات مربوطه پیش بروید.


### تمپلیت انتقال

1. فایل را دانلود کنید:

```
sudo wget -N -P /var/lib/marzban/templates/home/ https://raw.githubusercontent.com/erfjab/WebTemplates/main/templates/transfer/index.html
```

2. وارد فایل شوید:

```
nano /var/lib/marzban/templates/home/index.html
```

3. صفحه‌ای که می‌خواهید انتقال داده شود را در فیلد زیر وارد کنید:

```
<meta http-equiv="refresh" content="0; URL='https://example.com'" />
```

4. با فشردن `Ctrl+S` ذخیره و با `Ctrl+X` از فایل خارج شوید.

5. مرزبان را ریستارت کنید تا تمپلیت شما لود شود:

``` 
marzban restart
```


### تمپلیت رندوم

1. فایل را دانلود کنید:

```
sudo wget -N -P /var/lib/marzban/templates/home/ https://raw.githubusercontent.com/erfjab/WebTemplates/main/templates/random/index.html
```

2. مرزبان را ریستارت کنید تا تمپلیت شما لود شود:

``` 
marzban restart
```


### تمپلیت آی فریم

1. فایل را دانلود کنید:

```
sudo wget -N -P /var/lib/marzban/templates/home/ https://raw.githubusercontent.com/erfjab/WebTemplates/main/templates/iframe/index.html
```

2. وارد فایل شوید:

```
nano /var/lib/marzban/templates/home/index.html
```

3. یک صفحه‌ی ساده پیدا کنید و نامش را در قسمت عنوان وارد کنید:

```
<title>example</title>
```

4. آدرس صفحه مورد نظر را در فیلد زیر وارد کنید:

```
<iframe src="https://example.com" sandbox="allow-scripts allow-same-origin allow-forms"></iframe>
```

5. برای اینکه ظاهری بهتر داشته باشد، می‌توانید آدرس آیکون آن سایت را در این قسمت وارد کنید:

```
<link rel="icon" href="https://example.png">
```

6. با فشردن `Ctrl+S` ذخیره و با `Ctrl+X` از فایل خارج شوید.

7. مرزبان را ریستارت کنید تا تمپلیت شما لود شود:

``` 
marzban restart
```


### تمپلیت فیک

1. فایل را دانلود کنید:

```
sudo wget -N -P /var/lib/marzban/templates/home/ https://raw.githubusercontent.com/erfjab/WebTemplates/main/templates/fake/index.html
```

2. مرزبان را ریستارت کنید تا تمپلیت شما لود شود:

``` 
marzban restart
```
