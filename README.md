# git-im-team

# Git im Team Prozess (kurz)

## Branches benennen

In diesem Artikel findet ihr typische Konventionen für Branch Namen:
https://medium.com/@abhay.pixolo/naming-conventions-for-git-branches-a-cheatsheet-8549feca2534
(siehe Beispiele in der Section => "Sample branch names")

Empfehlung für Final Projects:
- feature/<feature-task>
- fix/<fix-fuer-fehler-ohne-crash>
- hotfix/<fix-fuer-fehler-mit-crash-oder-security-risk>
- docs/<update-an-readme>

Beispiele:
- feature/add-authentication-form
- bugfix/fix-header-styling
- hotfix/security-patch-auth-middleware
- docs/update-readme-ai-section

## Conventional Commit messages 

Semantic commit messages:
https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716

Zusammenfassend: 
- feat: (neues Feature für User, keine Code oder Doc Optimierungen)
- fix: (bug fix für den User, keine änderung von features code / logik)
- style: (formatting, fehlende semi colons, etc; keine änderung von features code / logik)
- refactor: (code ändern, eg. renaming a variable, keine änderung von features code / logik)
- docs: (updates an der documentation / readmes)
- chore: (update konfiguration / build prozess, etc; keine änderung von features code / logik)
- test: (neue oder ergänzte tests, refactoring von tests; keine änderung von features code / logik)


## Team Dev Prozess

- Sicherstellen dass ich zum Start auf main Branch bin: `git checkout main`
- Auf letzten Stand von Main upgraden: `git pull`
- Branch erstellen: `git checkout -b feature/<meinFeature>` meinFeature ersetzen durch dein Feature
- Coden coden coden
- Fertig mit Coden => `git add .` und `git commit`
- Checken, ob in der Zwischenzeit Leute was im Main geändert haben: `git pull origin main`
- Wenn es Merge Konflikte gibt: In unserem Branch fixen oder in Team-Meeting (wenn unklar, wie wir das lösen)
- Wenn es keine Konflikte gibt / alle behoben sind: `git push`
- PULL REQUEST auf Github stellen (=> grüner Button "OPEN & COMPARE PullRequest")
- Wenn die Meldung kommt "Able to Merge" => Branch mergen
- Danach: Den main branch lokal aktualisieren: `git checkout main` und danach `git pull`
- Danach: NÄCHSTEN Feature Branch erstellen `git checkout -b /feature/<naechstesFeature>`
- Und dann wiederholt sich alles immer wieder :)
