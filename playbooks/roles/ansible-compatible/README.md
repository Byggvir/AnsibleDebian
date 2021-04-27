# Rolle: ansible-compatible/

Erstellt von **Thomas Arend** am *2019-07-20*

# Kurzbeschreibung

Mit dieser Rolle wird wir ein frisch installieres Debian ansible komptibel gemacht.

## Voraussetzungen

- auf dem Ziel-Host ist mindestens ein minimales Debian eingerichtet.
- der Ziel-Host wurde mit einem User eingerichtet, dessen Username mit dem lokaten Usernamen identisch ist oder 
- ansible_user für den Ziel-Host definiert,
- das root-Passwort für den Zielhost ist bekannt
- das Password des Remote User ist bekannt.


## Ergebnis

- auf dem Ziel-Host ist die minimal erforderliche Software für ansible installiert.
- der ssh-key des Remote user ist auf dem Ziel-Host in $HOME/.ssh/authorized_users abgelegt 
- der user auf dem Zielhost ist in der Gruppe *sudo*.
- der Nutzer kann sich mit ssh auf dem Zielhost anmelden,
- der Nutzer erhält mit sudo ohne Passwort root-Rechte

## Unterverzeichnisse

Die Rolle verwendet folgende Unterverzeichnisse

- tasks:        Tasks zum ansible-komptiblem Einrichten des minimalsystems
- handlers:     keine
- defaults:     default variables for the role.
- vars:         zusätzlichen Nutzer
- files:        public ssh-keys der User
- templates:    keine
- meta:         keine

### tasks

Die Rolle *ansible-compatible* führt Tasks aus, die wie folgt gruppiert sind:

- Installation zusätzlicher Software
- Konfiguration, anpassen apt und der CD
- Einrichten der Nutzer
- Hinzufügen zur Gruppe sudo
- anpassen der /etc/sudoers, so dass kein Password abgefragt wird.

**Näheres** zu den *tasks* findest du **im README.md** im Verzeichnis *tasks*.

### handlers

Die Fehlerbehandlung wird durch Handler in *handlers* übernommen. 

**Näheres** zu den *handlers* findest du **im README.md** im Verzeichnis *handlers*.

### defaults / vars

Die Rolle *ansible-compatible* nutzt folgende Variablen in *defaults* und / oder *vars*:

Die Rolle *ansible-compatible* nutzt folgende Variablen in vars:

**Näheres** zu den *defaults* und *variablen* findest du **im README.md** im Verzeichnis *defaults* / *handlers*.

### templates

Templates im *j2* werden durch Ansible anhand der Varibalen und des Programmcodes in den Templates modifiziert und als Dateien auf das Zielsystem kopiert.

Die Rolle *ansible-compatible* nutzt folgende Templates in *templates*:

- *keine*

**Näheres** zu den *defaults* und *variablen* findest du **im README.md** im Verzeichnis *defaults* / *handlers*.

### files

Die Rolle *ansible-compatible* nutzt folgende Dateien in *files*:

Public ssh-keys der Nutzer. Der Name der Datei muss mit dem Username identisch sein und endet auf _pub.

**Näheres** zu den *Dateien* findest du **im README.md** im Verzeichnis *files*.

### meta

Die Rolle *ansible-compatible* nutzt folgende Meta-Daten:

**Näheres** zu den *Meta-Daten* findest du **im README.md** im Verzeichnis *meta*.

