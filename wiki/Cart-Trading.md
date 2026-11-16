# Cart trading

Use (right-click) a villager or wandering trader as in vanilla. Whenever vanilla would open its
trading screen, the cart screen opens instead. A merchant that vanilla would not trade with still
does not trade.

## The screen

| Part | What it shows |
| --- | --- |
| Header | The merchant's name, level and XP bar (wandering traders have neither) |
| Offer grid (left) | Every offer, as in vanilla. A red cross means out of stock; the number on a result is how many units are in your cart |
| Cart (right) | One line per offer: result, name, count, and `−` / `+` buttons |
| Footer | A status line, the *You pay* totals, and the Clear and Confirm buttons |

## Filling the cart

| Action | Mouse | Keyboard (offer focused) |
| --- | --- | --- |
| Add one unit | Left-click the offer | Enter |
| Add every remaining unit | Shift + left-click | Shift + Enter |
| Remove one unit | Right-click, or `−` on the cart line | Delete |
| Remove the whole line | Shift + right-click | Shift + Delete |

- A count never exceeds the offer's remaining stock (*No more in stock*).
- A cart holds up to 128 lines (*The cart is full*).
- When a price differs from the base price (demand, gossip, Hero of the Village), the cost tooltip
  shows *Base price*.

## Confirm

*You pay* adds up the cost of every unit in the cart. Confirm is active only when the server would
accept the cart. Otherwise hover over it or read the status line for the reason, such as
*You cannot pay for this cart* followed by what is missing.

Confirm buys everything at once. The server checks the cart again and trades each unit in order,
exactly as vanilla would.

| Result | Cart afterwards |
| --- | --- |
| *Trade complete* | Emptied; the items are in your inventory |
| *Prices changed. Check the marked lines* | Kept; changed lines are marked |
| *The merchant has run out of something in your cart* | Kept |
| *You cannot pay for this cart* | Kept; the status line lists what is missing |
| *The merchant is no longer trading with you* | The screen closes |

After any failure nothing is traded and the cart is kept. Clear, or closing the screen, discards the
cart.

## Changed prices

Prices can change while the screen is open. Each line remembers the price at which you added it and
is never changed silently: a changed line shows a `!` marker. Press it to accept the new price, or
remove the line. Confirm stays inactive until every marked line is handled.

## Accessibility

Everything works with the keyboard: Tab moves between the grid, the cart and the buttons, and the
arrow keys move within the grid. The narrator reads offers, cart lines and totals.
