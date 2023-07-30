# Anleitung zu Git Branches und Pull Requests auf GitHub

Git ist ein Versionskontrollsystem, das die Verwaltung von Codeänderungen und die Zusammenarbeit in Entwicklungsprojekten erleichtert. In dieser Anleitung werde ich Ihnen Schritt für Schritt erklären, wie Sie mit Git Branches arbeiten und Pull Requests auf GitHub erstellen. Dies ermöglicht es Ihnen, Codeänderungen sicher zu testen, bevor sie in den Hauptcode eingeführt werden. Ich werde auch auf typische Anwendungsfehler und deren Lösungen eingehen.

## Schritt 1: Branch erstellen

1. Wechseln Sie in das Verzeichnis des geklonten Repositorys:
   ```bash
   cd <Repository-Name>
   ```
2. Überprüfen Sie den aktuellen Branch mit dem Befehl `git branch`:
   ```bash
   git branch
   ```
3. Erstellen Sie einen neuen Branch mit dem Befehl `git checkout -b`:
   ```bash
   git checkout -b <Branch-Name>
   ```
   Ersetzen Sie `<Branch-Name>` durch den Namen des neuen Branches, den Sie erstellen möchten.

## Schritt 2: Codeänderungen durchführen und committen

1. Öffnen Sie den Code-Editor Ihrer Wahl und führen Sie die gewünschten Änderungen im Code durch.
2. Speichern Sie die Änderungen und schließen Sie den Editor.
3. Führen Sie den Befehl `git status` aus, um den Status der Änderungen anzuzeigen:
   ```bash
   git status
   ```
4. Fügen Sie die geänderten Dateien dem Staging-Bereich hinzu:
   ```bash
   git add <Dateiname>
   ```
   oder fügen Sie alle geänderten Dateien hinzu:
   ```bash
   git add .
   ```
5. Committen Sie die Änderungen mit einer aussagekräftigen Commit-Nachricht:
   ```bash
   git commit -m "Beschreibung der Änderungen"
   ```

## Schritt 3: Push des Branches auf GitHub

1. Führen Sie den Befehl `git push` aus, um den Branch und die Änderungen auf GitHub hochzuladen:
   ```bash
   git push origin <Branch-Name>
   ```
   Ersetzen Sie `<Branch-Name>` durch den Namen Ihres erstellten Branches.

## Schritt 4: Pull Request erstellen

1. Gehen Sie auf die GitHub-Seite Ihres Repositorys.
2. Klicken Sie auf den Tab "Pull Requests" und dann auf den grünen Button "New pull request".
3. Wählen Sie den Branch, den Sie in den Hauptcode (normalerweise den `main`- oder `master`-Branch) einfügen möchten, aus dem Dropdown-Menü "base".
4. Wählen Sie Ihren erstellten Branch aus dem Dropdown-Menü "compare".
5. Geben Sie eine aussagekräftige Beschreibung für den Pull Request ein, die Ihre Änderungen erläutert.
6. Klicken Sie auf den grünen Button "Create pull request", um den Pull Request zu erstellen.

*Alternativ:*
Das Erstellen eines Pull Request ist auch über die CI möglich, dafür einfach auf den Link im Response nach dem Push auf den Feature Branch klicken (cmd + click)

## Typische Anwendungsfehler und Lösungen

### Fehler 1: Konflikte beim Merging

Konflikte können auftreten, wenn der Code auf dem Hauptbranch seit dem Erstellen Ihres Feature-Branches geändert wurde. Dies führt dazu, dass Git nicht automatisch zusammenführen kann.

**Lösung:** Lösen Sie die Konflikte manuell, indem Sie die betroffenen Dateien bearbeiten und die Konflikte auflösen. Führen Sie dann die Schritte zum Committen und Pushen erneut durch.

### Fehler 2: Falscher Branch für den Pull Request ausgewählt

Es kann vorkommen, dass Sie den falschen Branch für den Pull Request auswählen.

**Lösung:** Überprüfen Sie sorgfältig, welchen Branch Sie in den Hauptcode einfügen möchten, und welchen Branch Sie in Ihrem Pull Request verwenden. Erstellen Sie gegebenenfalls einen neuen Pull Request mit den korrekten Branches.

### Fehler 3: Codeänderungen ohne neuen Branch committen

Manchmal vergessen Entwickler, einen neuen Branch zu erstellen, bevor sie Codeänderungen durchführen und committen.

**Lösung:** Erstellen Sie einen neuen Branch, indem Sie den Befehl `git checkout -b <Branch-Name>` ausführen, bevor Sie Änderungen am Code vornehmen und committen.

## Fazit

Herzlichen Glückwunsch! Sie haben gelernt, wie Sie mit Git Branches arbeiten und Pull Requests auf GitHub erstellen. Durch die Verwendung von Branches können Sie Codeänderungen sicher isolieren und testen, bevor sie in den Hauptcode eingeführt werden. Pull Requests ermöglichen es Teammitgliedern, Änderungen zu überprüfen und Feedback zu geben, bevor sie in das Hauptrepository übernommen werden. Beachten Sie typische Anwendungsfehler und deren Lösungen, um einen reibungslosen Workflow in Ihrer Entwicklungsarbeit zu gewährleisten.