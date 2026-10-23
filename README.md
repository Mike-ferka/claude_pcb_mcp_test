You are designing a PCB in KiCad 10 using the KiCad MCP tools. Work in stages and STOP for my approval after each one.

PROJECT
- Name / path: [name], [C:\path]
- Purpose: [one paragraph on what the board does]

REQUIREMENTS
- Input power: [e.g. 12V solar/battery, max current]
- Rails: [e.g. 5V @ 1A, 3.3V @ 500mA]
- MCU / main ICs: [e.g. ESP32-S3-WROOM-1, or "recommend one and justify it"]
- Interfaces/connectors: [sensors, UART, I2C, antenna, headers]
- Board constraints: [size in mm, layer count, mounting holes, enclosure]
- Manufacturing: [e.g. JLCPCB, prefer basic parts, hand-solderable 0805 minimum]

STAGES
1. Architecture: block diagram in text, part choices with JLCPCB/DigiKey part numbers, and a power budget. Wait for approval.
2. Schematic: place parts, wire everything, label nets, run ERC, fix all errors, and report any warnings you're leaving with reasons. Wait.
3. Board setup: outline, layer stack, design rules and netclasses (power traces sized for current). Wait.
4. Placement: propose placement with reasoning (decoupling caps next to pins, regulator thermal areas, antenna keep-out). Wait.
5. Routing: route power and sensitive nets manually; autoroute only the remaining signal nets. Add ground pours and stitching vias. Run DRC. Wait.
6. Outputs: gerbers, drill files, BOM, and position file for [fab].

RULES
- Check every footprint against the datasheet before using it; say which ones you verified.
- Never invent part numbers. If you can't find a part, say so.
- Save the project after each stage.
