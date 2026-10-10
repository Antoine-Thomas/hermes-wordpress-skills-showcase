# FAQ

**1. How do I install the skills?**
Clone the (private) pack, then copy each skill folder into your Hermes skills directory:

```bash
cp -r skills/* ~/.hermes/skills/          # Linux / macOS
Copy-Item -Recurse skills\* $env:LOCALAPPDATA\hermes\skills\   # Windows
```

Then fill the `.env` with your Local/WP-CLI/SSH values. See `Requirements` in the README.

**2. Where do I buy the full version?**
On Agensi: **https://www.agensi.io/@thomas-leroyer**. The showcase here contains documentation and
examples only; the working scripts ship with the purchase.

**3. What support is included?**
Purchase support (setup questions, bug reports) is handled by email —
searching.murphy@gmail.com. Please include your Agensi order reference.

**4. What is the license?**
Proprietary, *all rights reserved*: the showcase may not be copied, modified, redistributed,
sublicensed or used commercially. A commercial license is granted with the Agensi purchase.
Details in [`../LICENSE`](../LICENSE).

**5. How do I get updates?**
Updates to the pack are published to the private repository and announced to buyers on Agensi.
This showcase documents the current feature set; new skills are listed there as they ship.
