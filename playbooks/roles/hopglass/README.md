# Rolle: hopglass

Erstellt von **Thomas Arend** am *2019-07-20*

# Achtung, dies ist ein **Muster!**

*(Bitte eine Beschreibung einfügen! Weil: Gute Doku hilft!)*

# Kurzbeschreibung

Mit dieser Rolle wird ...

## Voraussetzungen

Die Rolle setzt voraus, dass

- Erstens
- Zweitens
- ...

## Unterverzeichnisse

Die Rolle verwendet folgende Unterverzeichnisse

- tasks:        contains the main list of tasks to be executed by the role.
- handlers:     contains handlers, which may be used by this role or even anywhere outside this role.
- defaults:     default variables for the role.
- vars:         other variables for the role.
- files:        contains files which can be deployed via this role.
- templates:    contains templates which can be deployed via this role.
- meta:         defines some meta data for this role.

### tasks

Die Rolle hopglass führt Tasks aus, die wie folgt gruppiert sind:

- Installation
- Konfiguration
- Neustart der Dienste, des Rechners

**Näheres** zu den *tasks* findest du **im README.md** im Verzeichnis *tasks*.

### handlers

Die Fehlerbehandlung wird durch Handler in *handlers* übernommen. 

**Näheres** zu den *handlers* findest du **im README.md** im Verzeichnis *handlers*.

### defaults / vars

Die Rolle hopglass nutzt folgende Variablen in *defaults* und / oder *vars*:

Die Rolle hopglass nutzt folgende Variablen in vars:

**Näheres** zu den *defaults* und *variablen* findest du **im README.md** im Verzeichnis *defaults* / *handlers*.

### templates

Templates im *j2* werden durch Ansible anhand der Varibalen und des Programmcodes in den Templates modifiziert und als Dateien auf das Zielsystem kopiert.

Die Rolle hopglass nutzt folgende Templates in *templates*:

- A.j2
- B.j2
- ...

**Näheres** zu den *defaults* und *variablen* findest du **im README.md** im Verzeichnis *defaults* / *handlers*.

### files

Die Rolle hopglass nutzt folgende Dateien in *files*:

Dateien werden 1:1 in der Regel 1:1 auf den Zielserver kopiert.

**Näheres** zu den *Dateien* findest du **im README.md** im Verzeichnis *files*.

### meta

Die Rolle hopglass nutzt folgende Meta-Daten:

**Näheres** zu den *Meta-Daten* findest du **im README.md** im Verzeichnis *meta*.

