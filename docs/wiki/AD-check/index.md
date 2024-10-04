# AD-check
## Allgemeines
Hiermit kann die Authentifikation an einem Active-Directory oder an einem LDAP-Server konfiguriert und getestet werden.

<br>![ClipCapIt-190121-193330.PNG](ClipCapIt-190121-193330.PNG)

###  Folgende Daten müssen für die Authentifikation eingestellt und bekannt sein 
* Ist die Active-Directory-ID bei einem Benutzer nicht gesetzt muss der **Login-Bezeichner von Letto als Benutzername am LDAP** existieren.
<br>![ClipCapIt-190121-192228.PNG](ClipCapIt-190121-192228.PNG)
* Sind Login-Bezeichner von Letto und Benutzername am LDAP unterschiedlich, so muss der **Benutzername von LDAP als Active-Directory-ID** beim Benutzer angegeben werden. Dies kann beim [Datenimport](../Datenimport/index.md) über den Button "AD-User" für alle Lehrer automatisch importiert werden oder in der [Benutzer](../Benutzer/index.md)einstellung eingestellt werden.
* IP-Adresse oder DNS-Name des LDAP/AD-Servers
* ldap URL, gegebenenfalls mit verwendetem Port
* Domain-Bezeichnung der lokalen Domain
* notwendige Parameter für die Konfiguration des LDAP-Strings

###  Prüfen der Einstellungen 
Durch den Button "Test Active-Directory" wird die Authentifikation des Benutzers "User" mit den angegebenen Konfigurationseinstellungen geprüft. Hierzu muss als "**User**" ein Benutzer angegeben werden, welcher am **LDAP/AD-Server** existiert. Es ist für diese Prüfung nicht notwendig, dass der Benutzer auch als Letto-User existiert.

Ob die Prüfung erfolgreich war wird rot und fett angegeben.

Unterhalb sieht werden die Logmeldungen zu dem Login angegeben, um die Fehlersuche zu erleichtern.

Aktuell werden **4 verschieden Varianten des Login-Vorgangs** (AD-Login, LDAP-Login(KS), LDAP-Login(old), LDAP-Login) durchprobiert. Die Login-Varianten AD-Login, LDAP-Login(KS) und LDAP-Login(old) werden in zukünftigen Versionen entfernt werden, da sie nur noch aus Kompatibilitätsgründen vorhanden sind. Für aktuelle und neue Installationen sollte die vierte Variante **LDAP-Login** einen korrekten Login liefern.
<br>![ClipCapIt-190121-194521.PNG](ClipCapIt-190121-194521.PNG)

###  Bekannte funktionierende Konfigurationen 