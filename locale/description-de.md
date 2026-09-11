# Steam Multiplayer

Dank Sh0wdowns Bibliothek RedirectPlay lässt sich Stronghold Crusader über Steam spielen!

## Verwendung

### Im Spiel

1. Aktiviere diese Erweiterung.
2. Wähle Mehrspieler im Hauptmenü.
3. Wähle Steamworks als Anbieter.

![Steamworks](https://github.com/gynt/ucp-extension-steam-multiplayer/blob/main/locale/image.png?raw=true)

4. Klicke auf Host oder Join. Beim Erstellen erscheint ein Fenster für die Lobby-Einstellungen. Wähle Public statt Friends only und setze ein Passwort, wenn nur Bekannte mitspielen sollen. Beim Beitreten zu einer geschützten Lobby erscheint gegebenenfalls eine Passwortabfrage.

### Über Steam (nur beitreten)

Du kannst auch den Link „Spiel beitreten“ auf einem Steam-Profil verwenden. Erstelle als Gastgeber zuerst eine Lobby, öffne das Steam-Overlay mit Umschalt+Tab und gehe über deinen Namen oder dein Symbol zum Profil. Klicke dort rechts auf „Spiel beitreten“ und kopiere den Link. Gib ihn deinen Mitspielern: Ein Klick öffnet das Spiel über Steam und verbindet es direkt mit der Lobby.

### Über die Befehlszeile

- `+connect_lobby <lobby id>` — Von Steam hinzugefügt. Die Lobby-ID ist ein uint64.
- `+host_game` — Beansprucht die Gastgeberrolle; alle warten auf deinen Beitritt. Ohne über +connect_lobby angegebene Lobby wird eine erstellt.
- `+join_directly` — Tritt beim Start direkt über die Lobby-ID bei, ohne verfügbare Lobbys aufzulisten und daher ohne komfortable Auswahloberfläche. Solange der Gastgeber nicht antwortet, kann die Oberfläche eingefroren wirken. Bevorzugt für private Lobbys nur mit Einladung.
- `+join_enumerated` — Listet Lobbys auf, vergleicht deren IDs mit der angegebenen Lobby-ID und tritt bei Übereinstimmung bei. Funktioniert nur für öffentliche und Freunde-Lobbys.

## Bekannte Probleme

1. Wer einer öffentlichen Lobby ohne Passwort beitritt, kann ein laufendes Spiel zum Absturz bringen.
2. Das Dialogfenster kann hinter dem Spiel liegen; mit Alt+Tab wird es sichtbar.
