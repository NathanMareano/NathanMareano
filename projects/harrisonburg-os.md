# Harrisonburg OS

**City data and traffic simulation · Personal datathon project · Interactive baseline prototype**

[Back to profile](../README.md) · [Full walkthrough](https://nathanielmareano.com/projects/harrisonburg-os/)

![Harrisonburg map showing the simulation clock, public geography, and modeled movement](../assets/harrisonburg-map.jpg)

*Actual prototype captured September 27, 2026. Movement and activity are simulated. The live VDOT feed remains disabled.*

## Why I built it

Living and studying in Harrisonburg made me interested in how residential trips, commuters, class schedules, and events shape traffic. I started this project to bring the city's data into one inspectable model and build a foundation for comparing potential transportation changes.

## My contribution

I'm responsible for framing the problem, integrating public datasets, and developing the simulation interface. That includes deciding what each source can support and making those assumptions visible.

**Stack and inputs:** React, TypeScript, MapLibre GL JS, public GIS and street geometry, VDOT traffic-volume records, and Census-derived aggregate inputs.

## How it works

1. Public geography establishes the street network, city boundary, terrain, and mapped signal locations.
2. Annualized road-volume records and aggregate population inputs provide demand context.
3. Time profiles and deterministic routes generate weighted vehicle agents and anonymous synthetic population groups.
4. Map layers, clock controls, a source registry, and an intersection inspector expose the model.

## Decisions that matter

- **Separate evidence from estimates.** Public observations, derived inputs, and simulated outputs are labeled distinctly.
- **Use aggregate population data.** Synthetic groups represent modeled demand rather than the movements of identifiable residents.
- **Make the baseline inspectable.** A useful scenario comparison needs traceable sources and clear assumptions before optimization claims.

## Current status

The interactive map, source registry, and intersection inspector work. Vehicle agents do not yet respond to displayed signal phases, and delay and queue-risk cards are provisional presentation formulas. The next step is to validate network behavior and connect movement to signal logic before comparing baseline and adaptive strategies.

The source code is private. This page shares the current prototype and its limitations.
