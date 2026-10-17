# Thelonious Muck — Swamp Lips Side Quest Dossier

Oct 17, 2026 · @mohini

Thelonious Muck is a standalone dancing, dress-up toy built from the spiky swamp ball creature with big pink lips from The Ribbiting Republic: Swamp World (v1.4).

## Origin

- On 2026-10-17 Mohini made the swamp ball creature (her POV avatar with big lips) lick the frogs for screen recordings and shots, then left the frogs singing on a second monitor and napped.
- She sent a screenshot to Noah (Ambiguous). He replied: "I like his feet", "That guy is hilarious", "He should jump".
- That evening it grew into its own side quest: long-armed dances, a dress-up picker, pun names, a lilypad dressing stage and sky modes.
- Lineage: Ribbiting Republic (2025 frog pond, Chonkly) to Swamp World remake (ribbiting-world repo, minted on Chonkly) to this character.
- Earlier roots Mohini named: Paper Dusk palettes (the joy of seeing one piece in many light/dark palettes), CryptoKitties and generative punks (collecting individual variants), and a mountaineering-club friend who named his folding camp stove "Stovey Wonder".

## The character

- Body: round, mossy-green spiky ball with two eyestalks, same as the swamp avatar.
- Lips: big glossy pink double lips, the main feature; they flap on some moves.
- Feet: stubby round feet (Noah's favorite part); keep them.
- Arms (decided: middle ground): long enough that knuckles drag on the ground at idle, Lurch-style. Built from 4-5 segments with lag and follow-through so they swing and flop behind moves. Can stretch about 1.5x on big moves, then snap back. Not infinite Elastic Man stretch.
- Motion: stop-motion "on twos" (about 12 fps poses, smooth camera), chunky not smooth. Mohini dislikes overly smooth motion.

## Dances

The long arms are the point: every move should use them. Mohini wants to screen-record him dancing to music.

| Move | What happens |
| --- | --- |
| Windmill | Arms spin like propellers; lips flap in the wind |
| Noodle wave | A ripple travels hand to body to other hand |
| Self-hug wrap | Arms wrap around his ball body twice |
| Ground drum | Slaps the mud in rhythm; eyestalks bounce |
| Swamp sprinkler | One arm out, ratcheting around |
| The jump (Noah) | Big squash, slow heavy hang, splat landing, arms trailing above |
| Breakdance spin | Floor spin powered by the long arms |
| Fortnite-style emote dance | A goofy viral-emote style loop (original moves, not a copy) |

## Dressing room, outfits, sky

He lives on a stage: a big lilypad or turtle-shaped rock mound in the swamp, framed with bamboo, short palms and hanging vines.

**Outfit slots (start with 3 options each):**

| Slot | Options Mohini named |
| --- | --- |
| Head | Hats, wigs (a wig can make him a her) |
| Face | Retro glasses, big nose, beard |
| Arms | Sleeves, gloves |
| Feet | Funky socks |

**Material styles (later):** glitter, metallic, punk, preppy.

**Viewing while dressing:** orbit camera like the 3D worlds (drag to rotate, scroll or pinch to zoom); when idle it slowly auto-turns like a lazy-susan product shot. Optional mirror toggle shows his back at the same time.

**Sky modes:** day, dusk, night toggle, reusing Paper Dusk palettes. Same satisfaction as dark mode: seeing the same piece in different light makes people want to try every look.

## Names system

Main name: Thelonious Muck. Each outfit combo gets one fixed full pun name (no mixing first and last names, which gets too all over the place). The name shows above his head as a clean, bold, high-contrast label: readability beats comic style.

**Full names so far (jazz, soul, rock homages):**

- Herbie Handcock (an option; long arms)
- Thelonious Muck (main name)
- Lipps Davis
- Dizzy Bogspie
- Charles Mudgus
- Swamp Ra (good for night sky)
- Swampy Hendrix (Mohini's)
- Stovey Wonder (the camp-stove origin joke)

**Pop-star style pool to add:** Tadpole Swift, Bogyonce, Billie Eyelash, Frank Swampatra, David Bogwie, Prince Ribbit, Muddy Mercury, Swampina Turner, Fleetwood Muck, Elon Muck (short, degens will get it), Mossy Khalifa (adult-star pun: keep or cut depending on where it's shown).

**Mechanic idea:** each outfit combo maps to one fixed full name (a wig or glitter lands on a pop-star name; a beard or beret on a jazz one). Keep names as parody puns, not real likenesses.

Possible brand or collection name: Swamp Ra Arkestra Outfitters.

## Toy vs collection: both, toy first

Decision (Mohini asked Claude to decide): build it as a viewer toy first, with a seed underneath.

- Toy: anyone can dress him, pick dances, flip the sky.
- Seed: every outfit + palette + name combo comes from a seed number. A Random button rolls a new seed; the current seed shows on screen.
- Collection later: seeds that feel special become fixed editions, punks or CryptoKitties style. No rebuild needed, because the seed system already exists.
- Brand and fake ad campaigns: screen-recorded later, after he exists.

## Scope phases

1. v0.1 - Thelonious dances: lilypad stage, middle-ground arms, 5-6 dances on number keys and tap buttons, day/dusk/night toggle, on twos, orbit and zoom camera, name label (Thelonious Muck).
2. v0.2 - Dressing room: 3 slots x 3 options, turntable view, optional mirror, name changes with outfit.
3. v0.3 - Style and seeds: glitter/metallic/punk/preppy materials, Random seed button, seed shown on screen.
4. Later - Brand name, fake ad campaigns, collection editions, moving him into Swamp World as a guest, maybe music sync for dances, XR mode where you wear him as your avatar and trigger custom emotes (mope, sad, smirk) and dances.

## Tech and repo notes for Claude Code

- New repo (keeps ribbiting-world clean); named swamp-lips. Local Path = WebExperiments, push via GitHub Desktop, auto-deploy on Vercel.
- Single self-contained index.html, pure ASCII (Chonkly mangles non-ASCII).
- three.js 0.160 via jsdelivr importmap (same as Swamp World). Tone.js 14.7.77 if sound is added. Vanilla JS, no frameworks.
- Reuse from Swamp World (read ../ribbiting-world/index.html, same WebExperiments folder): the swamp ball body, lips, eyestalks, feet, materials, on-twos pose timing, Paper Dusk palettes.
- Arms: segmented chain with spring/lag follow-through, evaluated on twos.
- Name tag: canvas-texture sprite or text mesh above head, bold comic lettering, always readable.
- Audio unlock (if sound): in click/touchend/pointerup/keydown, not pointerdown (iOS/Quest).
- Mobile: tap buttons for dances and sky; desktop: number keys. VR optional later.

## Open questions and parked ideas

- [ ] Final fixed-name list (main: Thelonious Muck; repo: swamp-lips)
- [ ] Lilypad or turtle-rock mound for the stage?
- [ ] Which outfit combos map to which fixed names?
- [ ] Music: dances to a built-in beat, or to music the viewer plays?
- [ ] Mint plan: Chonkly single, or editions from seeds later?

* Ideas Mohini lost mid-typing: add here as they come back.
