# Trade editor

The trade editor lets an operator change, in game, which trades villagers and wandering traders
draw. It edits vanilla's trade pools and saves them as a world datapack.

**A change takes effect only after the next server restart, and villagers keep the offers they
already have.**

## Who can use it

Operators at the configured permission level (default 2); see [Configuration](Configuration). A
player below the level gets vanilla's unknown-command message. In single player the world needs
cheats allowed. The command must be run by a player, not the server console.

## Editing

Run `/rto editor`. Pick a profession (or the wandering trader) on the left and a level tab, then:

- set **Offers drawn**, how many offers a villager draws from the pool at that level;
- click a trade to edit its costs, result, max uses, villager XP and reputation discount;
- use **New trade**, **Remove from pool**, **Duplicate** and **Revert** as needed.

Some trades are shared by several pools, and the dialog says so. Use *Duplicate* to change only this
pool. Special vanilla trades (enchanted books, explorer maps, potions and similar) keep their special
behaviour; fields vanilla computes are shown as *Computed*.

Vanilla caps every cost at one stack of the cost item. The dialog warns when a cost is above that.

## Apply and restart

Press **Apply** to save every changed pool. The server checks the whole change and saves all of it or
nothing; *Issues (n)* lists anything to fix.

1. Apply writes a staged pack. Nothing changes in the running game.
2. On a clean stop (`/stop`, or *Save and Quit to Title* in single player) the staged pack becomes
   `<world>/datapacks/realistictradingoverhaul_trades.zip`.
3. From the next start, new offers use the edited pools. Existing offers never change.

If the server crashes before a clean stop, the change stays pending and is applied at the next clean
stop. **Discard** cancels changes still waiting for a restart. To undo a live change, edit the trade
back and apply again.

Change the editor's datapack only through the editor. A datapack loaded above it that changes the
same trade wins, and the editor marks that trade as overridden.

## Several operators

Several operators can edit at once. When one applies, the others see **Reload**. Reloading keeps
their own unapplied changes on top.
