# OpenProject-Manual-Testing
QA : Fehler, Checklisten, Testfälle

# Fehlerbericht OP-001: Integer Overflow im Feld "Work"


| Kategorie | Details |
| :--- | :--- |
| Name | Integer Overflow im Feld "Arbeit" |
| Priorität | Hoch |
| GIVEN | Ein Arbeitspaket ist im Bearbeitungsmodus geöffnet; das Feld "Arbeit" ist leer. |
| WHEN | 1.Der Benutzer gibt den Wert 9999999999999999 (16 Neunen) in das Feld "Work" ein. 2. Der Benurzer beobachtet die automatische Berechnung des Feldes "Remaining Work".3 Der Benutzer klickt auf das Häkchen "Save"|
| EXPECTED RESULT | Das System validiert die Eingabe korrekt (zeigt Fehler an oder begrenzt den Wert). 2. Nach dem Speichern muss der ursprüngliche Wert 9999999999999999 im Feld "Work" unverändert bleiben. |
| ACTUAL RESULT | Das Feld "Remaining Work" zeigt den gegründeten Wert 9999999999999998 an (15 Neunen und eine Acht am Ende). Die Zahl wird falsch gerundet/berechnet. 2. Nach dem Speichern wird auch der Wert "Work" überschrieben und auf 9999999999999998 (15 Neunen und eine Acht am Ende) geändert. |
| Environment | Browser Brave, OS Windows 10,  Open Project Community Edition   |

![Bug Screenshot](bug_overflow_OP_001.png)



