# Coffee Among the Stars

*A quiet cockpit. A warm cup. An entire universe ahead.*

A cozy, browser-based space exploration game about taking the long way through the cosmos. Real astronomical destinations, slow music, and the small comforts of a ship drifting toward somewhere new.

The idea is simple: choose a destination, settle into your cockpit, and let the journey accompany a study session, an evening of work, or a quiet moment with a cup of coffee. Return to discover how far you have travelled.

## Project status

**Early development.** This README describes the intended experience and current technical direction. The features below are goals, not a list of completed functionality. A playable demo and local setup instructions will be added as development reaches those milestones.

## The experience we're building

- **Explore real destinations.** Discover planets and stars through journeys informed by astronomical data.
- **Make yourself at home.** Enjoy a comfortable cockpit, gentle ship ambience, small interactions, and coffee within reach.
- **Listen while you travel.** A carefully curated soundtrack of slow jazz, blues, classical music, and other quiet sounds is central to the atmosphere.
- **Leave room for life outside the game.** Journeys should support long, relaxed sessions without demanding constant attention, with progress that can be saved and resumed.
- **Remember where you've been.** Collect discoveries and badges as you reach new destinations.

## Real space, understandable models

The project aims to use real astronomical data while making its assumptions explicit. Real distances do not require waiting a lifetime to reach the next star: accelerated time, simplified motion, and fictional travel mechanics can make exploration playable.

The distinction matters. Observed data, mathematical approximations, game rules, and visual scale should remain clearly distinguishable. A planet drawn larger for visibility does not become larger in the underlying model.

Mathematics is part of the development journey, too. Each calculation should have a clear purpose, explicit units, understandable assumptions, and a meaningful way to check its result.

## Technical direction

- **Python** for scientific calculations, astronomical data preparation, and simulation models.
- **TypeScript** for the browser interface, rendering, audio, and local playback of journeys.
- **One repository** for the website and the game, with boundaries introduced as their responsibilities become clear.

The browser should animate a journey locally without requesting a new simulation result for every frame. How Python supplies the necessary data will evolve with the requirements; a dedicated backend is not assumed from the outset.

Frameworks, rendering tools, and storage choices will be selected when there is a concrete reason to introduce them.

## How development works

Coffee Among the Stars is both a game and a deliberate learning project. Development follows Clean Architecture principles, with small, understandable changes and a roadmap that can change as evidence accumulates.

The working rhythm is to discuss one conceptual unit, understand its purpose and alternatives, implement it when authorized, verify it, and review the result before moving on. Tests and documentation grow alongside that understanding.

See [AGENTS.md](AGENTS.md) for the complete development guidelines. Start there before contributing code or using an AI coding agent in this repository.

## Music and sound

Sound is part of the experience: the hum of the cockpit, a button press, a cup set down, and music worth staying to hear.

The soundtrack and sound library are still being developed. Asset sources, credits, and applicable usage terms will be documented as assets are introduced. Production assets may be distributed separately from the source code when their permissions require it.
