# Steam Multiplayer

借助 Sh0wdown 的 RedirectPlay 库，可以通过 Steam 游玩 Stronghold Crusader！

## 用法

### 游戏内

1. 启用此扩展。
2. 在主菜单中选择多人游戏。
3. 选择 Steamworks 作为服务提供者。

![Steamworks](https://github.com/gynt/ucp-extension-steam-multiplayer/blob/main/locale/image.png?raw=true)

4. 点击 Host（创建）或 Join（加入）。创建时会弹出大厅设置窗口。请选择 Public（公开），而非 Friends only（仅好友）；若只想与熟人游玩，请设置密码。加入有密码的大厅时可能会出现密码输入窗口。

### 从 Steam 加入（仅支持加入）

也可以使用 Steam 个人资料页的“加入游戏”链接。房主先创建大厅，再按 Shift+Tab 打开 Steam 界面，点击自己的名字或头像进入个人资料。右键点击“加入游戏”并复制链接，分享给其他玩家。点击此链接后，Steam 会启动游戏并立即连接大厅。

### 命令行

- `+connect_lobby <lobby id>` — 由 Steam 添加。大厅 ID 为 uint64。
- `+host_game` — 声明房主身份，所有人等待你加入大厅。如果未通过 +connect_lobby 指定大厅，则创建一个大厅。
- `+join_directly` — 启动时按大厅 ID 直接加入，不枚举可用大厅，因此没有方便的选择界面。房主尚未响应时，界面可能看起来卡住。适合仅邀请可加入的私人大厅。
- `+join_enumerated` — 枚举大厅，将其 ID 与指定的大厅 ID 比较，匹配则加入。仅适用于公开或好友大厅。

## 已知问题

1. 玩家加入无密码的公开大厅可能导致正在进行的游戏崩溃。
2. 弹窗可能被游戏窗口遮挡；按 Alt+Tab 可查看。
