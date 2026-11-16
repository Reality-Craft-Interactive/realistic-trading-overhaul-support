# FAQ and known issues

## Is RTO client-only?

No. Install it on both client and server. Single player includes both sides.

## Does RTO change prices or add a currency?

No. Prices are vanilla's, including demand, gossip and Hero of the Village, and each cart unit
counts as one vanilla trade.

## Do edited trades change my existing villagers?

No. Edits apply after a server restart and only to new offers: a new villager, or a villager
reaching a new level.

## Does it work with mods that add professions?

Professions that define their trades as trade sets (for example Homesteads) work with both the cart
and the editor. Professions whose offers come from code work with the cart but do not appear in the
editor.

## Can I use it in a modpack?

Yes, when the unmodified file is delivered through CurseForge's approved project dependency and
distribution systems. See [Modpack permission](Modpack-Permission).

## Where is the source code?

Development is private. This repository contains public support and documentation only.

## Known issues

- **Unlimited Villager Trades** is incompatible. It rewrites villager offers after every trade, so a
  cart stops after its first unit. Nothing is lost or duplicated: the units after the first are
  neither charged nor delivered.
- Vanilla caps every trade cost at one stack of the cost item. The editor warns about this.
