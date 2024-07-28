<p align="center">
  <a href="./README.md">
	English
	</a>
	|
	<a href="./README_PR.md">
	فارسی
	</a>

</p>

## What's This?

We've got some cool templates for Marzban's homepage that you can use. Here's the list:

- **Transfer**

This template will send your visitors directly to another webpage you specify.

- **Random**

With this one, visitors will see a random image, making it look like your domain hosts a random image site.

- **IFrame**

This template shows a webpage you specify within your domain's homepage, allowing visitors to interact with it right there.

- **Fake**

This one just shows visitors an ugly GIF. :/



**For more templates, give the project a star ⭐. My Telegram Chanel:** [@ErfJabs](https://t.me/erfjabs)

## Installation

Before you start, run this command on your server:

```
apt install wget
```

Then add these lines to your configuration:

```
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'HOME_PAGE_TEMPLATE="home/index.html"' | sudo tee -a /opt/marzban/.env
```

Now, pick the template you want and follow these steps.


### Transfer Template

1. Download the file:

```
sudo wget -N -P /var/lib/marzban/templates/home/ https://raw.githubusercontent.com/erfjab/WebTemplates/main/templates/transfer/index.html
```

2. Open the file:

```
nano /var/lib/marzban/templates/home/index.html
```

3. Enter the URL you want to transfer to in the following field:

```
<meta http-equiv="refresh" content="0; URL='https://example.com'" />
```

4. Save with `Ctrl+S` and exit with `Ctrl+X`.

5. Restart Marzban to load your template:

``` 
marzban restart
```


### Random Template

1. Download the file:

```
sudo wget -N -P /var/lib/marzban/templates/home/ https://raw.githubusercontent.com/erfjab/WebTemplates/main/templates/random/index.html
```

2. Restart Marzban to load your template:

``` 
marzban restart
```


### IFrame Template

1. Download the file:

```
sudo wget -N -P /var/lib/marzban/templates/home/ https://raw.githubusercontent.com/erfjab/WebTemplates/main/templates/iframe/index.html
```

2. Open the file:

```
nano /var/lib/marzban/templates/home/index.html
```

3. Find a simple page and put its name in the title section:

```
<title>example</title>
```

4. Enter the page's URL in this field:

```
<iframe src="https://example.com" sandbox="allow-scripts allow-same-origin allow-forms"></iframe>
```

5. To make it look nicer, you can add the site’s favicon URL here:

```
<link rel="icon" href="https://example.png">
```

6. Save with `Ctrl+S` and exit with `Ctrl+X`.

7. Restart Marzban to load your template:

``` 
marzban restart
```


### Fake Template

1. Download the file:

```
sudo wget -N -P /var/lib/marzban/templates/home/ https://raw.githubusercontent.com/erfjab/WebTemplates/main/templates/fake/index.html
```

2. Restart Marzban to load your template:

``` 
marzban restart
```
