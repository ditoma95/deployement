---
marp: false
theme : uncover
---
### PROCESSUS DE D'EPLOYEMENT DE L'APPLICATION LARAVEL

---

### Sur le terminal

##### Install le apache 2

```bash
sudo apt-get install apache2
```

##### Coller tout votre projet ici :

```bash
cd /var/www/html/s
```

---

##### Donner les droits sur le projet coller

```bash
sudo chmod -R 777 nom_projet/
```

---

### Configuration de : hosts

```bash
cd /etc/
cat hosts

--il s'agit de fixer l'IP, le nom de notre Application

192.168.228.223	www.gtfod.com s
```

## Option apache2

```bash
service apache2 [start | stop | restart | status]
```

---

### Configuration du .conf

```bash
cd /etc/apache2/sites-available/

sudo cp 000-default.conf gtfod_appli.conf

sudo nano gtfod_app.conf
```

---

##### Modifier simplement gtfod.com

```bash
ServerAdmin webmaster@localhost
DocumentRoot /var/www/html
ServerName gtfod.com
ServerAdmin webmaster@gtfod.com
DocumentRoot /var/www/html/admin/public

<Directory /var/www/html/admin>
AllowOverride All
</Directory>

ErrorLog ${APACHE_LOG_DIR}/error.log
CustomLog ${APACHE_LOG_DIR}/access.log combined
```

---

### Voila donc le resulat
