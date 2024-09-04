**Ansible-Playbook für die Installation eines Home Assistant-Servers local auf einen Ubuntu 24.04 Server**

Eine sehr Anfänger freundliche Anleitung :

Vorraussetzung: 
- Umgang mit den Terminal ( sudo ) und Nano 
- Ubuntu 24.04 Server
- Ansible ( falls nicht vorhanden - install mit : apt install ansible -y )
- erstelle eine Datei : nano inst_home.yml 
- kopiere den Code von inst_home.yml in die erstellte Datei und speichern
- Ausführen des Ansible Playbook: ansible-playbook inst_home.yml

![Bildschirmfoto vom 2024-09-04 23-01-54](https://github.com/user-attachments/assets/6b34dbd7-f739-47c0-89e2-442d525a7d4a)


- nach dem ausführen des Playbooks sollte der Home Assistant Server über eure IP Adresse des Server erreichbar sein. Zum bspl bei war es dann 192.168.178.74:8123 

![Bildschirmfoto vom 2024-09-04 23-14-27](https://github.com/user-attachments/assets/f86bd3b2-d9fb-4361-b73a-3a6f32e64100)



Beschreibung des Playbooks. 

Dieses Playbook führt die Installation von Home Assistant auf Ubuntu 24.04 durch. Es werden die erforderlichen Pakete installiert, ein virtuelles Umgebung erstellt, Home Assistant installiert und der Dienst gestartet. Am Ende werden die Login-Daten für Home Assistant angezeigt. 
Bitte beachten Sie, dass Sie möglicherweise zusätzliche Konfigurationsschritte vornehmen müssen, je nach den spezifischen Anforderungen Ihres Home Assistant-Setups.


Schritte der Installation im Playbook :

    Update APT Cache: Aktualisiert den APT-Paketindex, um sicherzustellen, dass die neuesten Paketinformationen verwendet werden.
    Installiere erforderliche Pakete: Installiert Python und andere Abhängigkeiten, die Home Assistant benötigt.
    Erstelle einen Benutzer: Erstellt einen dedizierten Benutzer homeassistant für die Ausführung von Home Assistant.
    Erstelle das Verzeichnis für Home Assistant: Erstellt das Verzeichnis /srv/homeassistant für die Installation und das virtuelle Python-Environment.
    Erstelle eine virtuelle Python-Umgebung: Richtet eine Python-Umgebung ein, um Home Assistant darin zu installieren.
    Aktualisiere pip: Stellt sicher, dass die neueste Version von pip verwendet wird.
    Installiere Home Assistant: Installiert Home Assistant im virtuellen Environment.
    Systemd-Dienst einrichten: Erstellt eine systemd-Dienstdatei, sodass Home Assistant automatisch gestartet wird.
    Start und Aktivierung des Dienstes: Startet den Home Assistant-Dienst und aktiviert ihn für den automatischen Start bei jedem Systemneustart.



Für das Ganjos Automation projekt: 
Anpassen der Konfig Datei Anleitung ( Terminal )
- ll /home/homeassistant/.homeassistant/configuration.yaml
   - in diesen ordner -  rest kommt morgen g8n
