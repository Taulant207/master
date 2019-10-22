## Modul 126 ngrok Tunnel

Peripheriegeräte im Netzwerkbetrieb einsetzen 1/3 TBZ-IT Modul 126 KEL AB126-W01 Modul 126 Localhost tunneln ngrok Version 1.4 Autoren KEL Peripheriegeräte im Netzwerkbetrieb einsetzen 2/3 TBZ-IT Modul 126 KEL AB126-W01 Demoprojekt fertig stellen: Dies ist ein guter Einstiegspunkt in ihre Werkstattarbeit. Beenden Sie ihr Demoprojekt mit der LED-Ansteuerung via Web. Der Zugriff sollte innerhalb des TBZ-Schul-Zimmers funktionieren! Zugriff von überall aus dem Internet Nun wollen wir ein „Tunnel“ (Reverse-Proxy) einbauen, damit wir z.B. per Natel unseren RasPi steuern können! Wir verwenden hier den NGROK-Service (sprich en-grok), der sogar bei Microsoft manchmal verwenden wird, um Webapps in einer VM zu testen, ohne gross die Applikation auf die DMZ auszurollen. https://ngrok.com/ Kopieren Sie ngrok Version 2.x für Linux(ARM) ins Verzeichnis ~/ngrok/ auf ihrem RasPi (Download à SFTP à ~/ngrok/*) und entzippen Sie das Archive gemäss Anleitung. Starten Sie den Dienst mit cd cd ./ngrok ./ngrok http 80 Der externe Zugriff erfolgt nun über die Adresse http://xyz....123.ngrok.io/index.html ... also auf die HTML-Indexdatei ihres RasPi-Apache2-Servers! Das fertig gestellte Demoprojekt kann nun auch «ferngesteuert» werden! Testen Sie nun auch den externen Zugriff via Smartphone (mit 3G/4G - Verbindung)! Hinweis: Via http://localhost:4040 können Sie den detaillierten Status auf dem RasPi-Browser anzeigen und den Verlauf checken! Auftrag: ePortfolio Erklären Sie in ihrem ePortfolio, wie der Aufbau der Verbindung von aussen zustande kommt, obwohl der RasPi hinter der TBZ-Firewall steht und in einem Subnetz verborgen ist! Verwenden Sie die korrekten Fachbegriffe und ein geeignetes Diagramm dazu! Weshalb müssen wir «http» und «80» beim Aufruf angeben? Ein guter Einstieg dafür ist: https://ngrok.com/docs Verwenden Sie dazu folgendes Diagramm: J Viel Glück und Spass am Entdecken...! J Peripheriegeräte im Netzwerkbetrieb einsetzen 3/3 TBZ-IT Modul 126 KEL AB126-W01 Hinweis: Gut aufgesetzte (Firmen-)Firewalls lassen den Tunnel (Reverse-Proxy) nicht zu und blockieren ihn. Auch an der TBZ musste ngrok.io als Dienst freigeschaltet werden:
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA0OTIyNzgxNSwyMjQ5NjIwLC0yMDg4Nz
Q2NjEyLDkxMjE0NTIxMCwtMTMxMDkyNTk4NSwtMTIxMDAwNDQx
NCwyNTc4MDY5MjhdfQ==
-->