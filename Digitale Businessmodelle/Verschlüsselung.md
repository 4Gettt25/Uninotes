### End zu End verschlüsselung
- Schlüsselgenerierung: Die beteiligten Parteien generieren ihre öffentlichen und privaten Schlüssel. Der öffentliche Schlüssel wird geteilt und ermöglicht es anderen, Daten zu verschlüsseln, die nur mit dem entsprechenden privaten Schlüssel entschlüsselt werden können.
- Verschlüsselung: Der Sender verschlüsselt die zu übertragenden Daten mithilfe des öffentlichen Schlüssels des Empfängers. Dadurch werden die Daten in eine undurchsichtige Form umgewandelt, die ohne den passenden privaten Schlüssel nicht lesbar ist.
- Übertragung: Die verschlüsselten Daten werden übertragen, beispielsweise über das Internet oder andere Kommunikationskanäle. Da die Daten verschlüsselt sind, können sie sicher durch unsichere Netzwerke transportiert werden.
- Entschlüsselung: Der Empfänger empfängt die verschlüsselten Daten und entschlüsselt sie mit seinem privaten Schlüssel. Dadurch werden die ursprünglichen Daten wiederhergestellt und sind für den Empfänger lesbar.

#### Wichtige Punkte der End-to-End-Verschlüsselung sind:
- Nur der Empfänger, der den privaten Schlüssel besitzt, kann die Daten entschlüsseln.
- Zwischenstellen, wie z.B. Server oder andere Netzwerkgeräte, haben keine Möglichkeit, die Daten zu entschlüsseln oder einzusehen.
- Selbst wenn das Übertragungsmedium kompromittiert wird, bleiben die Daten geschützt, da sie verschlüsselt sind.


### SSH
- **Verschlüsselte Kommunikation:** SSH verschlüsselt alle übertragenen Daten, einschließlich Benutzernamen, Passwörtern, Befehlen und Dateien. Dadurch wird sichergestellt, dass vertrauliche Informationen nicht von Angreifern abgefangen oder gelesen werden können.
- **Authentifizierung:** SSH verwendet verschiedene Methoden zur Benutzer-Authentifizierung, um sicherzustellen, dass nur autorisierte Benutzer auf das entfernte System zugreifen können. Die gängigsten Methoden sind die Passwort-Authentifizierung, die public-key-Authentifizierung und die Verwendung von Zwei-Faktor-Authentifizierung (2FA).
- **Port-Forwarding:** SSH ermöglicht das Weiterleiten von Netzwerkverbindungen über eine verschlüsselte SSH-Verbindung. Dadurch können entfernte Dienste, die normalerweise nicht direkt zugänglich sind, über die SSH-Verbindung genutzt werden, als wären sie lokal verfügbar.
- **Sichere Dateiübertragung:** Mit dem SSH-Protokoll können Dateien sicher zwischen dem lokalen und dem entfernten System übertragen werden. Dies wird oft mit dem Kommandozeilenprogramm "scp" (secure copy) oder grafischen SFTP-Clients (SSH File Transfer Protocol) realisiert.
- **Remote-Zugriff und Fernsteuerung:** SSH ermöglicht den Remote-Zugriff auf ein entferntes System über eine Befehlszeile oder die Ausführung von Befehlen auf dem entfernten System von einem lokalen System aus.[[Deep-Web Hosting]]