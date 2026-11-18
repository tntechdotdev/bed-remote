# Supported beds

Bed Remote works with adjustable bases that have a **Keeson KSBT** Bluetooth
controller. You can recognize it by its Bluetooth name, which starts with
**`KSBT`** (for example `KSBT03C000012345`). The app's bed list only shows
these controllers.

**Only `KSBT03C…` controllers have been tested.** When you choose any other
`KSBT` controller, the app connects but tells you it's untested, so you can
check every button (and that the bed stops when you let go) during the free 30
days before relying on it or paying. `KSBT03CR…` controllers are refused
because they use a different command format.

**Go by the Bluetooth name, not the brand.** Bed brands buy their controllers
from Keeson and other makers, and the same brand has shipped different
controllers over the years. Two "Member's Mark" bases can need different apps.
To check yours, open the app, go to **Settings → Bed → Choose** and see whether
a `KSBT…` controller appears.

## ✅ Confirmed

| Bed | Bluetooth name | Notes |
|---|---|---|
| **Member's Mark Premier Adjustable Base** (Sam's Club) | `KSBT03C…` | Tested by the owner: the motors move while an arrow is held and stop when it's released. |

## 👍 Should work

Other owners report that these use the same KSBT controller and the same
commands. They haven't been tested with this app.

| Bed | Bluetooth name | Notes |
|---|---|---|
| Ergomotion Rio 6.0 | `KSBT04…` | |
| Ergomotion Rio 5.0 / Denver Mattress Hibernation Platinum | `KSBT03C…` | Head and foot should work. Its third motor is **lumbar**, which the app doesn't have a button for yet (the app's Tilt is a different motor). |
| Beds sold with Keeson's **Adjustable Lite** app | `KSBT01C…` / `KSBT03C…` | Same commands. The memory buttons may be ordered differently from that app's MI/MII/MIII. |

## 🤔 Might work

Same KSBT controller family, but with a slightly different command format or
an unknown Bluetooth name. If you have one of these, please
[report whether it works](https://github.com/tntechdotdev/bed-remote/issues).

| Bed | Bluetooth name | Why it's uncertain |
|---|---|---|
| Purple **Premium Plus** | `KSBT04C…` | Purple's app adds an extra byte to every command. |
| Sleep Harmony bases | `KSBT04C…` / `KSBT03C…` | Its app adds a checksum byte to every command. |
| Ergomotion bases set up with the **Ergomotion 4.0** app (for example 4166, 4193, Flex, ErgoBalance, Aeroflex) | often `KSBT…` | Many use the same commands. They only appear in the app if the name starts with `KSBT`. |
| Q-Plus bases (Costco) with the app's **MX** remote | unknown | Same commands; name unknown. |
| 1500 Tilt Base | unknown | Same commands; name unknown. |

## ❌ Not supported

| Controller | How to recognize it | Found in |
|---|---|---|
| Keeson **KSBT03CR** | name starts with `KSBT03CR` | SomosBeds. Uses a different 7-byte command format; the app refuses it with a message. |
| Older Keeson controllers ("BaseI4/BaseI5") | name starts with `base-i4` or `base-i5`, or no `KSBT` name | Older Member's Mark bases, Purple Premium, Serta, Tempur Zero G / Curve, Beautyrest Black, GhostBed, GlideAway, ENSO, Restonic, King Koil, Sealy Ease, some Costco beds |
| OKIN / DewertOkin, Richmat, Linak, Leggett & Platt, Sleep Number and other brands | anything not starting with `KSBT` | Many other bases |

Support for the older Keeson controllers may come in a future version.

## Help grow this list

If your bed works, or doesn't, please
[open an issue](https://github.com/tntechdotdev/bed-remote/issues) with:

- the bed's brand and model,
- the controller's Bluetooth name (shown in the app under Settings → Bed),
- which buttons work and which don't.

---

Compatibility information comes from our own testing and from owner reports
collected by the open-source
[ha-adjustable-bed](https://github.com/kristofferR/ha-adjustable-bed) project.
Brand and product names are used only to describe compatibility. Bed Remote is
an independent app, not made by, affiliated with or endorsed by any of these
companies.
