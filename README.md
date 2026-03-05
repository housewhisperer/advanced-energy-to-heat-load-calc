# Advanced Energy Use to Load Calculator

A free, open-source HVAC sizing tool from **[Nate the House Whisperer](https://natethehousewhisperer.com)**.

This calculator estimates your home's heating design load from annual fuel use — no Manual J required. It's designed to help homeowners and contractors understand proper HVAC sizing using real energy data.

## 🔥 Live Tool

👉 **[Use it here](https://natethehousewhisperer.github.io/advanced-energy-calc)** *(update URL after GitHub Pages setup)*

Or find the full suite of HVAC sizing calculators at [natethehousewhisperer.com](https://natethehousewhisperer.com).

---

## What It Does

Enter your annual heating fuel use (gas, oil, propane, electric, etc.) and your city, and the calculator:

- Estimates your **building UA value** (how leaky/lossy your envelope is)
- Calculates your **design heat load** at the 99% outdoor design temperature
- Shows a **±20% sizing sweet spot** and a **1.4× maximum** recommendation
- Displays a full **heat load by temperature chart** with hourly bin data
- Supports adjustable **balance point**, **indoor setpoint**, and **setback** controls
- Lets you subtract **backup/supplemental heat** (wood stove, pellet, space heaters)
- Includes **°F / °C toggle**

## Coverage

- **185 US and Canadian cities** with ERA5 1991–2020 hourly temperature bin data
- **US ZIP code lookup** (5-digit)
- **Canadian postal code lookup** (FSA — first 3 characters, e.g. `M5V`, `T2P`)

## Methodology

The calculator uses the **Energy Use to Load** method:

1. Delivered BTUs = Annual fuel use × fuel energy content × appliance efficiency
2. UA (BTU/hr·°F) = Delivered BTUs ÷ annual degree-hours (base 65°F balance point)
3. Design Load = UA × (indoor setpoint 72°F − 99% design outdoor temp)

This approach is an alternative to Manual J that often produces more accurate results for existing homes because it's based on *actual observed energy use* rather than estimated inputs.

> **Key insight:** A properly sized system runs near 100% at design conditions. Oversized equipment short-cycles, reduces comfort, and costs more. The goal is continuous low-output operation.

For a full explanation, see the [Load Calc Training materials](https://natethehousewhisperer.com) and the book *Common Sense HVAC* (coming soon).

---

## Deploying on GitHub Pages

1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Set source to **Deploy from a branch → main → / (root)**
4. Your tool will be live at `https://yourusername.github.io/repo-name`

The entire calculator is a single `index.html` file with no external dependencies beyond React (loaded from CDN). It works offline once cached.

---

## Related Tools

All available at [natethehousewhisperer.com](https://natethehousewhisperer.com):

- **Simple Energy Use to Load Calculator** — streamlined version of this tool
- **Heat Pump Sizing Calculator** (hp-sizing) — includes manufacturer performance curves
- **Runtime Optimization Calculator** — find the ideal size for maximum runtime
- **Likely Load Range (LLR) Calculator** — quick load estimate from home characteristics

---

## License

MIT License — free to use, share, and adapt. Attribution appreciated.

Built with ❤️ by [Nate the House Whisperer](https://natethehousewhisperer.com) to help homeowners get properly sized HVAC systems.
