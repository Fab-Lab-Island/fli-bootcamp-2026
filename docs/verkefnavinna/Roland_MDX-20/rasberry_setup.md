# Rasberry pi uppsetning MDX-20

Modela mdx er keyrð á rassbery pi smá tölvu.



## Rasberry pi imager

Hægt er að nota hvaða rasberry pi tölvu sem er. Við notuðum raberry pi 3(32bit)

Með raberry pi imager er hægt að skifa stýrikerfið rasbian á SD kort t.d. 32 GB.

Eftir það er tölvan tengd við wifi og setup í SSH ham á eftirfarandi hát:

**Via Desktop GUI:**
If your Pi is connected to a monitor:

1. Go to the **Start Menu > Preferences > Raspberry Pi Configuration**.
2. Select the **Interfaces** tab.
3. Find **SSH** and toggle it to **Enabled**, then click **OK**.

**Via Terminal (raspi-config):**
If you are already at a terminal prompt:

1. Run `sudo raspi-config`.
2. Navigate to **Interface Options** (or Interfacing Options) and press Enter.
3. Select **SSH**, choose **Yes** to enable it, and then select **Finish**.

Á rasberry pi tölvuni er hægt að finna IP töluna með `ifconfig`

Eftir það er prófa tenginguna á annari tölvu með því að fara í terminal og slá inn: `ssh <nafn_tölvu>@<ip_tala_tölvu> `

## Rabbery pi tölva tengd við Modela fræsaara

Fræssin er tengdur með ds-25 tengi sem er tengt í hd-15 sem er sem tengist í rs-232 usb millistykki.

Næst er náð í [Mods](https://gitlab.cba.mit.edu/pub/mods) og mods er set upp á raberry tölvuna í gegn um SSH eða í tölvuni sjálfri ef hún er tengd við skjá. 

