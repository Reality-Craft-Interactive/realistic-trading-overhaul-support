# Troubleshooting and crash reporting

## Version mismatch or connection failure

Confirm the client and server use the same RTO JAR, Minecraft 26.3, NeoForge 26.3.0.84 or later, and
Java 25. RTO is required on both sides.

## The vanilla trading screen appears

Confirm RTO is listed on the Mods screen, then reproduce with only RTO and NeoForge installed. Attach
`latest.log`.

## Confirm stays inactive or a purchase is refused

Read the status line or hover over Confirm. The server refuses carts you cannot pay for, lines above
the remaining stock, and lines whose price changed until you accept the new price. See
[Cart trading](Cart-Trading).

## A cart stops after one unit

Another mod or datapack is rewriting the villager's offers after every trade. This is a known
incompatibility with Unlimited Villager Trades; see [FAQ and known issues](FAQ-and-Known-Issues).

## Trade editor

| Symptom | Check |
| --- | --- |
| `/rto` has no completion | Your permission level is below the configured one |
| *The editor is not available on this server* | Server log lines starting with `[RTO` |
| An edit does not show after the restart | The log line `[RTO pack] Started: …` should read `live present, selected yes, pending no`; only new offers use the edit |
| An edit stays pending across restarts | The server was not stopped cleanly; use `/stop` |
| *These trades are too large to load in the editor* | Edit that pool with a datapack instead |

## Preparing a useful report

Attach:

- `logs/latest.log`;
- the full file under `crash-reports/`, when present;
- exact RTO, Minecraft, and NeoForge versions;
- whether RTO is on the client, the server, or both;
- the complete mod list; and
- minimal reproduction steps.

Do not attach only a screenshot of the last exception line.
