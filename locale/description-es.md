# Steam Multiplayer

¡La biblioteca RedirectPlay de Sh0wdown permite jugar a Stronghold Crusader a través de Steam!

## Uso

### Dentro del juego

1. Activa esta extensión.
2. Selecciona Multijugador en el menú principal.
3. Elige Steamworks como proveedor.

![Steamworks](https://github.com/gynt/ucp-extension-steam-multiplayer/blob/main/locale/image.png?raw=true)

4. Pulsa Host o Join. Host abre una ventana para configurar la sala. Selecciona Public en vez de Friends only y añade una contraseña si solo quieres jugar con conocidos. Al entrar en una sala protegida puede aparecer una solicitud de contraseña.

### Desde Steam (solo unirse)

También puedes usar el enlace «Unirse a la partida» de un perfil de Steam. El anfitrión debe crear primero una sala, abrir la interfaz de Steam con Mayús+Tab y pulsar su nombre o icono para acceder al perfil. Haz clic derecho en «Unirse a la partida» y copia el enlace para compartirlo con los demás. Al pulsarlo, Steam abre el juego y este se conecta inmediatamente a la sala.

### Desde la línea de comandos

- `+connect_lobby <lobby id>` — Steam lo añade. El identificador de sala es un uint64.
- `+host_game` — Asume el papel de anfitrión; todos esperan a que te unas. Si +connect_lobby no especifica una sala, crea una.
- `+join_directly` — Se une directamente a la sala al iniciar mediante su identificador, sin enumerar salas disponibles ni ofrecer una interfaz cómoda de selección. La interfaz puede parecer bloqueada si el anfitrión aún no responde. Es el método preferido para salas privadas por invitación.
- `+join_enumerated` — Enumera las salas, compara sus identificadores con el indicado y se une si coinciden. Solo funciona con salas públicas y para amigos.

## Problemas conocidos

1. La entrada de personas en una sala pública sin contraseña puede bloquear una partida en curso.
2. La ventana emergente puede quedar detrás del juego; usa Alt+Tab para verla.
