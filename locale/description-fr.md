# Steam Multiplayer

La bibliothèque RedirectPlay de Sh0wdown permet de jouer à Stronghold Crusader via Steam !

## Utilisation

### Dans le jeu

1. Activez cette extension.
2. Choisissez Multijoueur dans le menu principal.
3. Choisissez le fournisseur Steamworks.

![Steamworks](https://github.com/gynt/ucp-extension-steam-multiplayer/blob/main/locale/image.png?raw=true)

4. Cliquez sur Host ou Join. Host ouvre une fenêtre de configuration du salon. Choisissez Public plutôt que Friends only et ajoutez un mot de passe pour limiter la partie aux personnes que vous connaissez. En rejoignant un salon protégé, une demande de mot de passe peut apparaître.

### Depuis Steam (rejoindre uniquement)

Vous pouvez utiliser le lien « Rejoindre la partie » d’un profil Steam. L’hôte doit d’abord créer un salon, ouvrir l’interface Steam avec Maj+Tab puis accéder à son profil en cliquant sur son nom ou son icône. Un clic droit sur « Rejoindre la partie » permet de copier le lien à transmettre aux autres joueurs. Ce lien ouvre le jeu via Steam et le connecte immédiatement au salon.

### Depuis la ligne de commande

- `+connect_lobby <lobby id>` — Ajouté par Steam. L’identifiant du salon est un uint64.
- `+host_game` — Prend le rôle d’hôte ; tous attendent votre arrivée. Sans salon indiqué par +connect_lobby, en crée un.
- `+join_directly` — Rejoint directement le salon au lancement grâce à son identifiant, sans lister les salons disponibles ni proposer une interface de sélection pratique. L’interface peut sembler figée si l’hôte ne répond pas encore. Méthode conseillée pour les salons privés sur invitation.
- `+join_enumerated` — Énumère les salons, compare leurs identifiants à celui fourni et rejoint le salon correspondant. Fonctionne uniquement pour les salons publics et réservés aux amis.

## Problèmes connus

1. L’arrivée de joueurs dans un salon public sans mot de passe peut faire planter une partie en cours.
2. La fenêtre de dialogue peut être cachée derrière le jeu ; utilisez Alt+Tab pour la voir.
