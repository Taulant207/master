# Localhost tunneln mit ngrok

## Inhaltsverzeichnis
1. [Autoren, Versionierung des Dokumentes](#autoren)
2. [Funktion des Services](#funktion)
	2.1. [Zusatz](#zusatz)
3. [Benötigte Hard- und Software](#ware)
	3.1. [Hardware](#hardware)
	3.2. [Software](#software)
4. [Installationsanleitung](#anleitung)
5. [Qualitaetssicherungprozess](#quali)
6. [Quellen](#quellen)


## Autoren, Versionierung des Dokumentes <a name="autoren"></a>
**Version:** 1.0
**Autoren:** Taulant Saliu, Trojan Veseli


## Funktion des Services <a name="funktion"></a>
**Was ist ein Web Tunnel und wozu brauchen wir ngrok?**

Mit einem Web Tunnel kann man einen (Reverse-Proxy) einbauen, um dann somit zum Beispiel auf den RasPi Zugriff zu erhalten. Dies kann man sich so vorstellen, wie wenn ein Inhaftierter durch einen Tunnel aus dem Knast versucht zu fliehen.<br> Beispiel [El Chapo](https://www.spiegel.de/panorama/justiz/joaquin-guzman-el-chapo-floh-durch-diesen-tunnel-a-1043339.html)

"ngrok" ist in ein Service, welches eine Verbindung zum ngrok-Clouddienst herstellt. Es akzeptiert öffentlichen Datenverkehr und leitet diese durch den ngrok-Prozess an die angegebene lokale Adresse weiter. - *In unserem El Chapo Beispiel wären es die Werkzeuge und Personen, die ihn dabei geholfen hatten.*


### Zusatz<a name="zusatz"></a>
Der Service "*ngrok*" wird von guten Firewalls blockiert und ist somit nicht zugänglich.

**Fazit:** 

*Man kann nicht aus jedem Gefängnis auf gleicher Art und Weise ausbrechen.*

## Benötigte Hard- und Software <a name="ware"></a>

### Hardware<a name="hardware"></a>
- Aufgesetzter RasPi
- Handy (3G, 4G)

### Software<a name="software"></a>
- Linux für Raspberry (Raspbian...)
- [ngrok (Linux ARM 64)]([https://ngrok.com/download](https://ngrok.com/download))


## Installationsanleitung <a name="anleitung"></a>
**1**. Über oben genannten Link ngrok für Linux installieren.
**2**. ngrok Datei ins Verzeichnis ~/ngrok/ auf dem RasPi kopieren.
**3**. ngrok über folgende Commands auf RasPi starten:<br> &nbsp;&nbsp;&nbsp;&nbsp;`cd`
&nbsp; &nbsp;&nbsp;`cd ./ngrok`
&nbsp;&nbsp;&nbsp;&nbsp;`./ngrok http 80`
**4**. Nun kann man über ~ http://"IpAdresse".ngrok.io/file.html ~ auf den &nbsp;&nbsp;&nbsp;&nbsp;RasPi zugreifen.



## Qualitätssicherungsprozess <a name="quali"></a>
Der Service kann nun getestet werden, indem man ein File erstellt und mit dem folgenden Link darauf zugreifen kann.
http://"**IpAdresse**".ngrok.io/**file.html**
**IpAdresse**: Adresse des RasPi's
**file.html**: Selbst erstellte Website, auf die man zugreifen möchte.

Wenn man auf dem Smartphone Zugriff auf die Website hat, so hat man die Bestätigung, dass es funktioniert hat.

## Quellen<a name="quellen"></a>
[ngrok offizielle Seite](https://ngrok.com/)
[Spiegel Beitrag über El Chapo](https://www.spiegel.de/panorama/justiz/joaquin-guzman-el-chapo-floh-durch-diesen-tunnel-a-1043339.html)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTM5OTQyNDAzMCw5MjAxMjM2NTAsMTA2OT
Y0OTgyNCwyMTE5NTk5NzY0LDIwMDY2MDMyNjksMTA3ODE5ODg5
OSwxNTM1ODM2MDYyLDk4MjA1MDE2MCwtMjA1MDQyNTI1NiwxOT
E1NTc5NjkwLDcyODQzOTc1MSwxNzA1MTc2NDE2LC0xMjEyNjE4
MzA4LC0xOTM4Nzc5MTUwLC0xMDM3ODUzNjgzLC04MDQ4NjIxOT
csMTk1MDUwODc5OCwzNzUxNjI1NzIsMzk2MTg0MjA1LDIyNDk2
MjBdfQ==
-->