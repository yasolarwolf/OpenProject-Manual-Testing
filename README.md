# OpenProject-Manual-Testing
QA : Fehler, Checklisten, Testfälle

# Fehlerbericht OP-001: Integer Overflow im Feld "Arbeit"


| Kategorie | Details |
| :--- | :--- |
| Name | Integer Overflow im Feld "Arbeit" |
| Priorität | Hoch |
| GIVEN | Ein Arbeitspaket ist im Bearbeitungsmodus geöffnet; das Feld "Arbeit" ist leer. |
| WHEN | Der Benutzer gibt 9999999999999999 (16 Neunen) in das Feld "Arbeit" ein und speichert. |
| EXPECTED RESULT | Das System validiert die Eingabe korrekt (zeigt Fehler an oder begrenzt den Wert). Die Datenintegrität bleibt erhalten. |
| ACTUAL RESULT | Das Feld "Verbleibende Arbeit" zeigt 9999999999999998 (zeigt 15 Neunen und eine Acht am Ende). Die Zahl wird falsch gerundet/berechnet. |

![Bug Screenshot](bug_overflow_OP_001.png)



