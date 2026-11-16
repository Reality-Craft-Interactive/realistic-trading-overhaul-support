# Configuration

RTO has one setting. It lives in `config/realistictradingoverhaul-local.toml` on the server (in single
player, in the client's `config` folder):

```toml
# 2 gamemasters (default), 3 admins, 4 owners
permissionLevel = 2
```

- It sets the operator permission level needed for the [trade editor](Trade-Editor).
- Values outside 2 to 4 are moved to the nearest of them, with a warning in the log. Ordinary
  players can never use the editor.
- A change applies to editor requests at once, and to the `/rto editor` command after the next start
  or `/reload`.

Trade changes are not configuration. They are made with the editor and saved as a datapack.
