# Game ideas and open design questions

These notes capture product and worldbuilding discussions from October 2026. They preserve the player's intended experience, the approaches proposed during discussion, and questions that remain open. They are **not** a list of implemented features, a fixed specification, or permission to build all of these ideas. The [documentation guide](documentation-guide.md) explains where understood decisions and implemented behavior will eventually be documented.

**Narrative spoilers:** These working notes include a proposed revelation about Earth. Do not copy that material into player-facing descriptions.

## The experience

**Desired direction.** Coffee Among the Stars should feel calm enough to accompany study or rest, yet reward attention and exploration. The visual goal is *minimalist but beautiful*: simple scenes should feel complete through composition, light, sound, and meaningful details. A quiet view from a landed ship on the Moon, with jazz playing inside the cabin, is an example. The game is not aiming for the density or graphical detail of a large open-world space game.

**Guiding distinction.** Use real astronomical destinations and measurements where possible. Keep observed facts, calculated approximations, fictional technology and travel rules, and display choices distinguishable. Realism should shape the experience without requiring a full physical simulation of every object.

## Physical scale, approaches, and surfaces

**Desired direction.** Planetary and stellar sizes and distances should have their real physical meaning in the game's underlying model. The player should be able to approach a planet, enter an atmosphere where one exists, and look out from within it. Landing on a body such as the Moon should allow the player to enjoy the sky from the surface.

**Proposed rendering approach.** Draw what is visible, with a margin for what will soon enter view. Use simpler representations at great distances and more detail as the ship approaches. Keep physical measurements separate from camera position, visual scale, and navigation markers. Very large distances and nearby surface details may require local, camera-relative rendering coordinates to preserve precision. None of this selects a rendering engine or requires detailed terrain everywhere.

**Scientific examples.** Mars has a thin, dusty atmosphere; Venus has a dense, cloudy one. Their descents should not look interchangeable. The Moon has no substantial atmosphere, so its daytime sky is black even when the ground is brightly sunlit. A clear view of Saturn from Titan's surface is not a sound assumption because Titan's thick haze strongly obscures visible light. A scene above the haze, or a view through an instrument, would be a different premise. These examples guide visual honesty; no destination or descent sequence has been chosen for implementation. [NASA: Mars](https://science.nasa.gov/mars/facts/), [Venus](https://science.nasa.gov/venus/venus-facts/), [the lunar sky](https://science.nasa.gov/solar-system/moon/phenomena-nasa-astronauts-will-encounter-at-moons-south-pole/), and [Titan's haze](https://science.nasa.gov/solar-system/planets/saturn/saturn-moons/on-titan-the-sky-is-falling/).

**Open.** How close to a surface may the ship travel? Is landing a short guided sequence, free flight near terrain, or something else? Which destinations should support it first?

**Proposed initial scope.** The pilot could remain aboard the ship when visiting a surface. A landing could offer a view from the cockpit and access to local contacts without requiring walking controls, character animation, traversable terrain, or city interiors. Leaving the ship may be reconsidered later; no landing behavior has been implemented.

## Light, stars, and safety

**Desired direction.** Lighting should carry much of the visual impact. Passing a red giant might softly tint the cockpit red while the music continues. Color, direction, and intensity of light can make a sparse scene memorable; transitions should remain comfortable rather than startling.

**Desired direction.** Stars have a safe approach limit. The ship should signal increasing heat, and an autopilot should prevent a suicidal approach. This is a player-facing safety behavior, not yet a defined thermal model. A future rule may account for the star's energy output, distance, and the ship's fictional tolerance instead of using one universal distance.

**Open.** The player is leaning against character death, including failed landings, but has not made a final decision. The discussed starting direction is recoverable danger: warnings and automatic escape near a star, or a safe recovery from a poor landing. If used, warnings need a visible form as well as sound so a player listening to other audio or playing muted can understand them.

## Badges, the Fleet, and the pilot

**Desired direction.** Badges should recognize memorable combinations of place and action, as well as reaching distant planets and stars. Illustrative examples include having morning coffee on Mars and listening to jazz near Jupiter. Tuning into a previously unknown radio station could itself earn a badge. These examples are prompts for design, not approved trigger rules or promises of particular licensed tracks.

**Further idea.** Every authored mission could have its own badge. That makes badges mementos of particular journeys and stories. If adopted, routine repeated errands would need care so the collection does not become a catalogue of indistinguishable awards.

**Desired direction.** Badges contribute to the pilot's standing in the International Exploration Fleet. The Fleet provides a sense of belonging and progression alongside the quiet journeys.

**Proposed refinement.** Ranks could mark accumulated discoveries rather than granting a new rank for every badge. Badge conditions eventually need clear meanings: for example, whether “morning” follows local simulated time or the player's time, and what counts as listening to music near a destination. Progression should recognize curiosity without demanding constant attention or exhaustive collection.

**Open.** The pilot was first imagined as a man. A compulsory male avatar has not been chosen. A simple spacesuit or pilot figure with selectable presentation, including a feminine option, could support identification when the character is actually visible. The amount and form of customization remain undecided.

## Story told through places and voices

**Desired direction.** The setting is a post-cataclysm human civilization in the year 3029. The history should not arrive as a single explanatory account. Missions, local broadcasts, ordinary conversation, and scattered clues should allow attentive players to connect events for themselves. A radio host's casual story may suggest the place and action behind a future badge.

**Illustrative story seed.** A broadcaster on the Welders of Ganymede station might mention a traveller's unusual ritual at another destination. The player could later repeat the ritual and discover a badge. The earlier “dinner on Titan while looking at Saturn” example was only an illustration; Titan's haze makes that specific surface view scientifically doubtful.

**Proposed refinement.** Broadcasts should include ordinary chatter as well as consequential clues. Important lines should be replayable or readable later so studying, muting the game, or missing one transmission does not permanently block understanding. Players who do not follow every clue should still enjoy the journey; the deeper history is a reward for attention.

**Open.** The content and eventual explanation of the cataclysm, the Fleet's history, and the extent of the final revelation have not been defined.

## A return to Earth — narrative spoilers

**Desired direction.** The player's journey may begin somewhere other than Earth. Returning to Earth later would then be a major discovery: the familiar landmasses would be gone, and the visible surface would be an ocean world. The catastrophe behind this change and humanity's departure would be pieced together rather than announced at the beginning. Ocean exploration by the ship is a possible later extension, not part of the current visit idea.

**Scientific boundary.** Melting all of Earth's present glaciers and ice caps would raise sea level by roughly 70 metres, not submerge every mountain. A fully ocean-covered Earth therefore needs an extraordinary fictional cause, perhaps involving much more than ice melt. The exact cause is intentionally unresolved. [USGS: total ice-melt sea-level rise](https://www.usgs.gov/faqs/how-would-sea-level-change-if-all-glaciers-melted).

**Visual and story consideration.** An ocean-covered Earth may reduce the need to represent continents and cities in an orbital view, though convincing water, clouds, atmosphere, and lighting still require work. Entering the Solar System could reveal archived or rebroadcast radio from early human space exploration. Original centuries-old broadcasts would have travelled outward at light speed rather than remaining available locally. These recordings could carry clues about the catastrophe and migration. [NASA: electromagnetic waves in space](https://science.nasa.gov/learn/basics-of-space-flight/chapter6-1/).

## Galactic reach, a possible starting system, and terraformed worlds

**Desired direction.** Human settlements in 3029 may be spread across parts of the Milky Way. Intergalactic exploration need not be part of the game. Some encountered planets would have been terraformed, with human atmospheres, vegetation, small cities, or outposts. Their built environments could be viewed from the ship without requiring fully explorable urban worlds.

**Scientific and fictional boundary.** A practical space-warp drive is not established science. Whether it could cross between galaxies follows from fictional rules we have not chosen. Keeping the journey within the Milky Way is a coherent scope and story choice: its disk is roughly 100,000 light-years across, while Andromeda is about 2.5 million light-years away. A human presence in selected regions would leave vast areas unknown even with fictional faster-than-light travel. [NASA/JPL: Milky Way and Andromeda scale](https://www.jpl.nasa.gov/images/pia08787-amazing-andromeda-galaxy/).

**Starting-place proposal, not a decision.** One candidate is the ship in orbit over a small colony on **Kepler-62f**, with a local radio and a possible first descent to a port. Kepler-62 is a real five-planet system around a star smaller and cooler than the Sun, about 1,200 light-years away. Kepler-62e and Kepler-62f lie in its habitable zone; the known radius of Kepler-62f is about 1.4 Earth radii. Its actual surface and atmosphere are not known. A terraformed colony there would be fiction set among measured astronomical facts. Kepler-452b is an alternative if a star more like the Sun matters more than having several known planets in the starting system. Neither suggestion fixes the player's starting location or the first route to implement. [NASA: Kepler-62 system](https://science.nasa.gov/photojournal/kepler-62-and-the-solar-system/), [NASA Exoplanet Archive: Kepler-62](https://exoplanetarchive.ipac.caltech.edu/overview/Kepler-62%20f), and [NASA: Kepler-452b](https://science.nasa.gov/exoplanet-catalog/kepler-452-b/).

**Terraforming boundary.** A planet's habitable-zone orbit does not establish that it has a suitable atmosphere, oceans, or a terraformable surface. Treating a list of discovered exoplanets as known terraforming candidates would overstate present evidence; even global terraforming of Mars is beyond present-day technology. Advanced terraforming in 3029 would be a deliberate fictional achievement. Different settlements could show different stages, from enclosed habitats to worlds with altered atmospheres and plants. The particular planets, methods, timelines, and ecological consequences remain open. [NASA: habitable zones and their limits](https://science.nasa.gov/exoplanets/terrestrial/) and [NASA: limits of Mars terraforming](https://www.nasa.gov/news-release/mars-terraforming-not-possible-using-present-day-technology/).

## Visiting cities and remote outposts

**Desired direction.** A player could overfly a human city by day or night, take photographs, or choose to park. Each city or control outpost would mark its authorised landing places with a familiar, repeated symbol. After parking, the player would see the people or organisations available to contact at that location. A port near bars might offer different contacts from a Fleet office. The Fleet should always be available as a contact in some form.

**Presentation idea.** The interaction could shift from the flight view through a fade to black into illustrated still scenes, inspired by the way Final Fantasy Tactics presents places. An image of the pilot at a bar counter with local jazz, or entering a Fleet office beneath the stars, could carry dialogue without requiring walking controls or a fully modelled city. This is a proposed scene language, not a selected UI or art pipeline. Its writing, illustration, music, and accessibility would still need deliberate work.

**Meaningful arrival.** A city or outpost should offer more than scenery and a badge. Local radio, a contact, a message to carry, a clue, an updated route, or another small exchange could change what the player understands or can do next. A repeated landing symbol and a limited set of presented contacts would make the scope of interaction clear without suggesting that every visible street is freely explorable.

**Illustrative mission seed.** A character near the bars asks the pilot to carry a love letter to her husband at a distant place provisionally called “Quasar 5.” It is an example of a personal errand that could lead to a larger story, not a named destination or confirmed mission.

**Longer story idea.** Two or three substantial message-delivery stories might require the player to collect clues from broadcasts, places, conversations, and perhaps photographs, then connect them. The player should be able to revisit acquired clues without having the game solve the mystery automatically. These stories should remain optional enough for a player who mainly wants a quiet journey. Missions and their badges, characters, plots, and exact inference mechanics are undecided.

**Communications boundary.** Space networks can store data and forward it when a link becomes available, so ordinary messages need not all travel aboard a ship. A courier could matter when a region lacks coverage, a physical object or trusted handoff is required, or a fictional faster-than-light ship can beat light-speed transmissions. If the Fleet contact is always present in the interface, its central office need not always answer live: a local Fleet representative might respond at a port, while a distant message waits for a connection. The relation between warp travel and information transfer remains an open world rule. [NASA: delay- and disruption-tolerant networking](https://www.nasa.gov/communicating-with-missions/delay-disruption-tolerant-networking/).

## Photography and sharing

**Desired direction.** Taking screenshots should be a regular pleasure of travel. Flying over a settlement at different times of day, finding a striking angle, and recording quiet views could become part of the player's personal exploration. Community challenges for especially beautiful images are a possible later extension.

**Proposed refinement.** A focused way to hide the interface and frame or export an image may be more useful initially than an in-game social platform. Saved images could also help the player remember places or story clues, but a photo journal, sharing service, contests, moderation, and accounts have not been chosen. Lighting and composition need to make photographs worth taking before social features are considered.

## Regional radio and music

**Desired direction.** Stations should feel local, like terrestrial radio, but their regions may be much larger. Some might cover much of the Solar System; others may be heard only around Jupiter or Pluto. “Welders of Ganymede” and “Forgotten of the Solar System” are examples of regional identities. Discovering and tuning a station should be a meaningful sign of exploration.

**Scientific and fictional boundary.** Radio waves travel through space, but received signals weaken with distance and can be blocked or relayed. Interplanetary transmissions also have travel time. A future human communications network could give a station wide regional coverage; a single ordinary FM transmitter would not explain uninterrupted Solar System coverage. The precise coverage rule can be a declared game simplification. Recorded or delayed programs fit the setting without implying instantaneous distant conversation. [NASA: radio propagation](https://science.nasa.gov/learn/basics-of-space-flight/chapter6-1/) and [Mars relay network](https://science.nasa.gov/mars/mars-relay-network/).

**Desired direction.** Each station would have its own music and voices. A possible initial content size is three songs and three or four spoken pieces per station, repeated over time. Some speech is everyday filler; some carries lore. Distant stations may reward travel with especially appealing music and stories. The ship also has a basic music collection for travel outside any station's coverage.

**Proposed refinement.** A small loop is useful as an initial scope but could tire a player during long study sessions. Speech could recur less often than music, with enough spacing, variation, and replay access to make clues pleasant to find. The ship's basic collection should itself be enjoyable; remote stations add variety and discovery. Radio listening and music volume should remain under the player's control.

**Open.** Direct song selection could belong to the ship's saved collection while a live station keeps its own programming. Whether stations themselves allow choosing or skipping tracks remains undecided.

**Desired direction.** Discovering a station might allow the ship to save it or record its programs, rewarding exploration and preserving music for regions with no reception. A possible distinction is between receiving a local broadcast and playing material already archived aboard the ship. The exact archive behavior is open.

**Music permissions.** A Miles Davis recording was an aspirational example, not an asset choice. Commercial recordings would depend on obtaining rights appropriate to the game's use; the musical work and the recording may have different rights holders. Recording or on-demand replay may require separate consideration. Until an asset is cleared, badges should not depend on access to it. [U.S. Copyright Office: musical works and sound recordings](https://www.copyright.gov/music-modernization/sound-recordings-vs-musical-works.pdf).

## Dark matter as a mystery

**Desired direction.** The player may eventually discover that humanity in 3029 has found a way to “see” something about dark matter. This could make apparently empty travel more intriguing. The phenomenon should initially be unexplained; players would discover its significance through experience and scattered clues.

**Scientific boundary.** Dark matter has mass and is inferred from gravitational effects, but its composition is unknown and it has no established visible color. Current large-scale maps show structures such as cosmic filaments; they do not imply bright, detailed clouds along an ordinary route through the Solar System. [NASA: dark matter](https://science.nasa.gov/dark-matter/) and [ESA: large-scale map](https://www.esa.int/ESA_Multimedia/Images/2007/01/3D_map_of_dark_matter_as_seen_by_Hubble).

**Proposed fictional approach.** A future ship instrument could measure a newly discovered property or reconstruct a density map and translate the result into false colors, like a weather map. With the instrument off, the sky remains dark. With it on, subtle contours or concentrations might appear. Rare patterns that the Fleet cannot explain could become story clues. Detecting fine local structure would be a fictional scientific discovery of 3029, not a fact about today's dark-matter model.

**Open.** The instrument, the appearance of its display, the meaning of any anomaly, and its relationship to the cataclysm are undecided. Dark matter should not be used as a compulsory visual filler for every quiet stretch of travel.

## What these notes do not decide

These conversations do not select an engine, a rendering technique, a radio protocol, a music catalogue, a badge catalogue, a rank table, a specific landing model, an avatar system, a starting system, a communications model, or the underlying truth of the dark-matter mystery. Those choices need their own discussion when a current product or implementation need makes them concrete. Future documentation can move an understood term to the glossary, an accepted milestone to the roadmap, or implemented behavior to the relevant architecture and concept documents without treating every idea here as a requirement.
