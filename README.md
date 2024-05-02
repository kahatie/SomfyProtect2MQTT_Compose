# SomfyProtect2MQTT_Compose
docker compose i use for SomfyProtect2MQTT

--- EN ---

After installing the container you must create / edit config.yaml
to connect to the container as root:
```
docker exec -it --workdir / --user root <docker id/name> sh
```
then once logged we can copy the example config file:
```
copy /app/config/config.yaml /config/config.yaml
```
then edited it

finally set read-only rights to appuser :
```
chown appuser /config/config.yaml
chmod 400 /config/config.yaml

mkdir /config/somfyprotect2mqtt
chown appuser /config/somfyprotect2mqtt
chmod 766 /config/somfyprotect2mqtt

mkdir /config/echo
chown appuser /config/echo
chmod 766 /config/echo
```
copy https://github.com/Minims/SomfyProtect2MQTT/blob/master/config/echo/somfy.sh in /config/echo

then fix right
```
chmod 666 /config/echo/somfy.sh
```
--- FR ---

Après avoir installer le container il faut créé / édit config.yaml
pour ce connecter au container en root :
```
docker exec -it --workdir / --user root <docker id/name> sh
```
puis une fois logger on peut copier le fichier de config d'exemple:
```
copy /app/config/config.yaml.exemple /config/config.yaml
```
puis edité le

enfin fixer les droits en lecture seule pour appuser:
```
chown appuser /config/config.yaml
chmod 400 /config/config.yaml

mkdir /config/somfyprotect2mqtt
chown appuser /config/somfyprotect2mqtt
chmod 766 /config/somfyprotect2mqtt

mkdir /config/echo
chown appuser /config/echo
chmod 766 /config/echo
```
copy https://github.com/Minims/SomfyProtect2MQTT/blob/master/config/echo/somfy.sh dans /config/echo

enfin fixer les droit:
```
chmod 666 /config/echo/somfy.sh
```
