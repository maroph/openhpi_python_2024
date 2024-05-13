# Über diese Site
Vom 2. Oktober 2024 bis 29. Oktober 2024 läuft der
[openHPI](https://open.hpi.de/) Kurs
[Python – schnell und intensiv Programmieren lernen](https://open.hpi.de/courses/python2024).

Auf dieser Site habe ich meine Beispiellösungen zu den
Aufgaben abgelegt.

Die Lösungen sind im Verzeichnis 
[sources](https://github.com/maroph/openhpi_python_2024/tree/main/sources)
abgelegt. Alle Lösungen sind lokal (also ohne die 
openHPI CodeOcean Umgebung) ablauffähig.

__Hinweis__: es sind nur mögliche Lösungen. Es gibt
meistens mehrere (auch elegantere) Möglichkeiten, die
Aufgaben zu lösen.

__Die Aufgaben habe ich mit Python 3.11 erstellt und
auf einem Windows 10 und einem Debian 12.1 System
getestet.__  

Die verwendete Python Version kann man mit dem Programm 
[version.py](https://raw.githubusercontent.com/maroph/openhpi_python_2024/main/sources/version.py) 
ausgeben.

```
Debian:
$ python3 version.py
3.11.2 (main, Mar 13 2023, 12:18:29) [GCC 12.2.0]
sys.version_info(major=3, minor=11, micro=2, releaselevel='final', serial=0)
major        : 3
minor        : 11
micro        : 2
releaselevel : final
serial       : 0
```

```
Windows 11:
> python.exe version.py
3.11.7 (tags/v3.11.7:fa7a6f2, Dec  4 2023, 19:24:49) [MSC v.1937 64 bit (AMD64)]
sys.version_info(major=3, minor=11, micro=7, releaselevel='final', serial=0)
major        : 3
minor        : 11
micro        : 7
releaselevel : final
serial       : 0
```

## Struktur der Site
Der gesamte Inhalt dieser Site (HTML und Python Source
Code) ist abgelegt in meinem GitHub Repository
[maroph/openhpi_python_2024](https://github.com/maroph/openhpi_python_2024/):

* docs
  Markdown Sourcen dieser Site
* sources  
  Python Source Code der Aufgaben aus Woche 1 bis 4
* LICENSE  
  Lizenz des Repositories (CC-BY 4.0)
* README.md  
  Readme Datei des Repositories
* mkdocs.yml  
  [MkDocs](https://www.mkdocs.org/) Konfigurationsdatei

Die Webseiten aus den Markdown Dateien erzeuge ich mit dem
[MkDocs](https://www.mkdocs.org/) Static Site Generator. Die erzeugten Webseiten
werden im Verzeichnis _site_ abgelegt.

## Mein Python Virtual Environment
Zur Erzeugung der Webseiten verwende ich die folgenden Python
Module

* [mkdocs-material](https://pypi.org/project/mkdocs-material/)  
  Das Modul [mkdocs](https://pypi.org/project/mkdocs/) wird dabei mitinstalliert.
* [mkdocs-git-revision-date-localized-plugin](https://pypi.org/project/mkdocs-git-revision-date-localized-plugin/)

Für die benötigten Python Module verwende ich das folgende Virtual Environment:

    python3 -m venv venv
    source venv/bin/activate
    python -m pip install --upgrade pip
    python -m pip install --upgrade setuptools
    python -m pip install --upgrade wheel
    python -m pip install --upgrade mkdocs-material
    python -m pip install --upgrade mkdocs-git-revision-date-localized-plugin

Sollte das Modul pip und/oder venv nicht installiert sein,
muss man das entsprechende Package installieren.

Auf einem Debian System geht das mit dem folgenden
Kommando

    sudo apt install python3-pip
    sudo apt install python3-venv

Hinweis: einige Beispiele im Verzeichnis _sources/extras_
verwenden das Modul [requests](https://pypi.org/project/requests/): 

    python -m pip install --upgrade requests

---

* Das [Python favicon](https://www.favicon.cc/?action=icon&file_id=831343) im Verzeichnis 
assets ist von der Site [favicon.cc](https://www.favicon.cc/)
* Die [Python Logo](../assets/python-logo-only2.png) Datei ist eine verkleinerte Version der Datei 
[python-logo-only.png](https://s3.dualstack.us-east-2.amazonaws.com/pythondotorg-assets/media/community/logos/python-logo-only.png).
