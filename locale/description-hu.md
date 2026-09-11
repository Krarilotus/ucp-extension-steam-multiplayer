# Steam Multiplayer

Sh0wdown RedirectPlay könyvtárának köszönhetően a Stronghold Crusader Steamen keresztül is játszható!

## Használat

### A játékban

1. Kapcsold be ezt a bővítményt.
2. Válaszd a Többjátékos módot a főmenüben.
3. Válaszd a Steamworks szolgáltatót.

![Steamworks](https://github.com/gynt/ucp-extension-steam-multiplayer/blob/main/locale/image.png?raw=true)

4. Kattints a Host vagy Join gombra. Létrehozáskor felugrik a szoba beállítóablaka. A Friends only helyett válaszd a Public lehetőséget, és adj meg jelszót, ha csak ismerősökkel játszanál. Védett szobához csatlakozáskor jelszókérés jelenhet meg.

### Steamből (csak csatlakozás)

A Steam-profil „Csatlakozás a játékhoz” hivatkozása is használható. A házigazda előbb hozzon létre szobát, nyissa meg a Steam átfedést Shift+Tabbal, majd a nevére vagy ikonjára kattintva a profilját. Jobb kattintással másolja ki a „Csatlakozás a játékhoz” hivatkozást, és adja át a társaknak. A hivatkozásra kattintva a Steam elindítja a játékot, amely azonnal csatlakozik a szobához.

### Parancssorból

- `+connect_lobby <lobby id>` — A Steam adja hozzá. A szobaazonosító uint64 típusú.
- `+host_game` — Lefoglalja a házigazda szerepét; mindenki a csatlakozásodra vár. Ha a +connect_lobby nem adott meg szobát, létrehoz egyet.
- `+join_directly` — Induláskor közvetlenül csatlakozik a megadott szobához, az elérhető szobák felsorolása és kényelmes választófelület nélkül. Ha a házigazda még nem válaszol, a felület lefagyottnak tűnhet. Meghívásos, privát szobákhoz ajánlott.
- `+join_enumerated` — Felsorolja a szobákat, összehasonlítja azonosítójukat a megadottal, és egyezéskor csatlakozik. Csak nyilvános és baráti szobáknál működik.

## Ismert hibák

1. A jelszó nélküli nyilvános szobához csatlakozók összeomlaszthatják a folyamatban lévő játékot.
2. A párbeszédablak a játék mögött maradhat; Alt+Tabbal tehető láthatóvá.
