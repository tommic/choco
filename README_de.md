# Chocolatey und Git Setup

Dieses Projekt hilft dir, schnell eine Basisinstallation deiner bevorzugten Software mithilfe von Chocolatey und Git einzurichten.

## Chocolatey installieren

Als Erstes muss Chocolatey heruntergeladen und installiert werden. Das geht am besten mit folgendem (langen) Command:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.SecurityProtocolType]::Tls12; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

### Git installieren

Nun können und müssen wir unser erstes Tool mit Chocolatey installieren.  
**Git** ist ein verteiltes Versionskontrollsystem, das hauptsächlich zur Verwaltung von Quellcode verwendet wird. Es ermöglicht Entwicklern, Änderungen an ihrem Code zu verfolgen, an mehreren Features gleichzeitig zu arbeiten und die Zusammenarbeit im Team zu vereinfachen.  

Installiere Git mit folgendem Befehl:

```powershell
choco install git -y
```

> **Hinweis:** Nach der Installation einmal das Terminal schließen und neu öffnen, damit Windows erkennt, dass Git installiert wurde.

## Holen der Paketlisten

Navigiere zu deinem Benutzerverzeichnis und klone das Repository mit den Softwarepaketlisten:

```bash
cd ~
git clone https://github.com/tommic/choco_pack.git
```

Jetzt liegen alle Softwarepakete im Verzeichnis `choco_pack` in deinem Benutzerverzeichnis.

## Installieren der Paketlisten

Um die Paketliste zu installieren, führe den folgenden Befehl aus:

```bash
choco install basic.config -y
```

> Das `-y` sorgt dafür, dass du bei jedem Paket nicht einzeln bestätigen musst.


