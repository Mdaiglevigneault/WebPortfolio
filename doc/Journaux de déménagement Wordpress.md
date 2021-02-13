## #1 - Configurer le nom de domaine
![Configuration DNS](./images/Demenagement_DNS.PNG)

## #1 - Crée le site sur le serveur
- [X] Création du répertoire /var/www/dvmax.xyz.
```
mkdir dvmax.xyz
```
- [X] Création du vhost "dvmax.xyz".
```
sudo  cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/dvmax.xyz.conf
```
- [X] Configurer le vhost
- [X] Activer le vhost
```
sudo  a2ensite dvmax.xyz.conf
sudo  systemctl reload apache2
```
## #1 - Déplacer le répertoire WordPress
- [X] Déplacement intégral de l'ancien répertoire dans le nouveau.
```
mv ./dvmax.zonedns.education/* ./dvmax.xyz/
```