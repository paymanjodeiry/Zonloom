<img src="Zonloom-logo.png" alt="Zonloom logo" width="220">
# Zonloom — 1.0 Beta

Building energy modeling tools for Rhino and Grasshopper, with gbXML export for DesignBuilder.

Developed by **Payman Jodeiry**, Architect.

## Overview

Zonloom simplifies building geometry creation and preparation for energy modeling. It provides a model creation wizard, geometry preview tools, and a Honeybee-to-gbXML workflow for transfer to DesignBuilder.

## Software requirements

- Rhino 8 and Grasshopper
- Ladybug Tools / Honeybee
- Human UI for components that use its interface
- DesignBuilder to import and further edit the exported gbXML model

## Geometry input rules

- Use closed polygonal boundaries made of straight segments. Curved boundaries and curved segments are not currently supported; approximate them with straight segments before input.
- Draw all boundary curves clockwise when viewed from above. All current tests have been performed using this direction.
- The staircase boundary must lie entirely inside the building boundary.

## Current Beta limitations

- Windows are not generated on sloped surfaces.
- Internal voids, atriums, and light wells are not currently supported.
- Staircase and elevator shaft spaces are represented floor by floor. Continuous vertical openings are not generated automatically. Edit these spaces and create the required holes manually in DesignBuilder.
- Duplex units are not currently handled as connected spaces across floors. Each floor is modeled separately.
- Multiple apartments or units on the same floor are not divided into separate thermal zones. The floor is imported into DesignBuilder as a single zone, with the staircase handled separately.

Review the imported geometry and zoning in DesignBuilder before running an energy simulation.

## Downloads

When available, compiled Beta packages will be published in the
[Releases section](https://github.com/paymanjodeiry/Zonloom/releases).

## Tutorials and updates

- [Blog](https://paymanjodeiry.blogspot.com)
- [Aparat](https://www.aparat.com/Zonloom)
- [YouTube](https://www.youtube.com/@zonloom)

## Bug reports

Please report problems through
[GitHub Issues](https://github.com/paymanjodeiry/Zonloom/issues).

Include:
- A description of the problem
- Steps to reproduce it
- Screenshots and any error messages
- Your Rhino, Honeybee, and Human UI versions
- A small example file, if possible
