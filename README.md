# Anleitung für Versionierung eines Projektes
1. Initialisierung des Projektes mit Git
- Installiere Git entweder über einen Paketmanager, wie z.B. choco/brew/apt
- Initialisiere das Verzeichnis als git-Repository mit "git init"
2. Einrichtung von Git:
- Identifiziere dech eindeutig, indem du die beiden Befehle git config --global user.name "username" und git config --global user.email "email@gmail.com"
- Das ist wichtig, damit deine Commit deinem Usernamen und deiner Email-Addresse zuordnen kann.
3. Verwaltung von Änderungen in Git
- Erstelle eine neue Datei mit "touch README.md" und füge diese zum Staging-Area mit "git add. " hinzu.
- Möchtest du diesen Stand commiten, also eine neue Version erstellen, dann führe ein "git commit- m "beschreibung"
- Mit "git Status" überprüfen wir, welche Files bisher zur Staging-Area hinzugefügt worden sind.
4. Verbindung zu einem Remote-Repository
- du hast bereits einen Github-Account angelegt.
- du musst eine Verbindung zwishcen deinem lokalen Rechner und deinem Github-Account erstellen, führ dazu folgende Schritte durch.
- Generiere dir einen SSH-Key mit dem Befehl "ssh-keygen -t ed25519 -C "E-Mail". Du wirst nach dem Pfath gefragt, wo der SHH-Key gespeichert werden soll. 
- Gibt hier den Stand ein. Setzte kein Passwort. Mit cat musst dir den Public key des geneierten ablesen und kopieren.
- Den kopierten Schlüssel fügst du unter Github Settings --> SHH Keys ein. 
- Der Entwickler erstellt eine Repository auf Github (Profil --> neues Repo erstellen..). Er kann sich diese Repository 
- Dazu verwendet er den BEfehl "git remote add origin..." und kann dann nach einem "git push -u origin" seine lokale Änderung 
- Die anderen Entwickler können sich auch den updstream auf das Repo setzen, wenn sie als Collaboration seinem Repository in Github auf Settings geht und dann unter Collaborators --> Add die Entwickler mit ihren Github-Namen hinzufügt. 
5. Synchronisieren von Änderungen
- zum Pushen führe folgenden BEfehl aus. "git push -u origin master" einmal, dannach reich ein "git push"
- zum Pullen führe folgenden Befehl aus "git pull (--rebose, dann holen wir uns akturelle Änderungen vom Master-Branch in unseren aktuellen Stand/Branch)
- Achtung! Wenn zwei Entwickler gleichzeitig an dem Repository arbeiten, dann versuche immer wieder die Änderung mit zu integrieren --> immer wieder ein git pull --rebose durchführen. 
6. Branching und Features Entwicklung: 
