# Steam Multiplayer

Sh0wdown’ın RedirectPlay kütüphanesi sayesinde Stronghold Crusader Steam üzerinden oynanabilir!

## Kullanım

### Oyun içinden

1. Bu uzantıyı etkinleştirin.
2. Ana menüden Çok Oyunculu’yu seçin.
3. Sağlayıcı olarak Steamworks’ü seçin.

![Steamworks](https://github.com/gynt/ucp-extension-steam-multiplayer/blob/main/locale/image.png?raw=true)

4. Host veya Join’a tıklayın. Host, lobi yapılandırma penceresini açar. Friends only yerine Public seçin; yalnızca tanıdıklarınızla oynamak için parola ekleyin. Parolalı bir lobiye katılırken parola penceresi açılabilir.

### Steam üzerinden (yalnızca katılma)

Steam profilindeki “Oyuna katıl” bağlantısını da kullanabilirsiniz. Ev sahibi önce bir lobi oluşturmalı, Shift+Tab ile Steam arayüzünü açmalı ve adına veya simgesine tıklayarak profiline gitmelidir. “Oyuna katıl” düğmesine sağ tıklayıp bağlantıyı kopyalayın ve arkadaşlarınızla paylaşın. Bağlantıya tıklandığında Steam oyunu açar ve oyun hemen lobiye bağlanır.

### Komut satırından

- `+connect_lobby <lobby id>` — Steam tarafından eklenir. Lobi kimliği uint64 türündedir.
- `+host_game` — Ev sahibi rolünü üstlenir; herkes lobiye katılmanızı bekler. +connect_lobby ile lobi belirtilmemişse yeni lobi oluşturur.
- `+join_directly` — Mevcut lobileri listelemeden, dolayısıyla kullanışlı bir seçim arayüzü olmadan, başlangıçta lobi kimliğiyle doğrudan katılır. Ev sahibi henüz yanıt vermiyorsa arayüz donmuş görünebilir. Yalnızca davetle girilen özel lobiler için tercih edilir.
- `+join_enumerated` — Lobileri listeler, kimliklerini verilen lobi kimliğiyle karşılaştırır ve eşleşene katılır. Yalnızca herkese açık ve arkadaş lobilerinde çalışır.

## Bilinen sorunlar

1. Parolasız herkese açık bir lobiye katılan kişiler devam eden oyunu çökertebilir.
2. Açılır pencere oyunun arkasında kalabilir; görmek için Alt+Tab kullanın.
