---
title: Photography Lexicon for UGC AI Decisions
author: Compiled from multiple photography sources (see Sources)
type: guide
domain: photography
source: knowledge/sources/phography/photography_lexicon/ (cross-source synthesis)
compiled: 2026-04-30
tokens_estimate: ~2600
---

## TL;DR

A pragmatic glossary for AI agents producing or judging UGC-style imagery. Each term names the **visual effect** an agent should expect — not just the spec — so an automated pipeline can pick "85mm portrait" vs "phone wide selfie" or "Rembrandt key + low fill" vs "high-key clamshell" based on intended look, not generic standards. Cross-references the source packs in `knowledge/sources/phography/photography_lexicon/`.

## When to use

Reach for this lexicon whenever an AI agent must (a) describe the visual character of a photo, (b) pick a focal length / camera / shooting distance / lighting setup for a UGC brief, or (c) detect distortion, exposure, color, or compression artifacts in user-submitted images.

## Prerequisites

- The agent has access to or is proposing camera settings, lens choices, framing instructions, or lighting placement.
- The deliverable is UGC-adjacent: selfies, talking-head, product-in-hand, lifestyle, ad creative, YouTube/TikTok video — not high-end studio work where a real photographer holds the call.

---

## Focal length — full-frame equivalents

Use these as the reference scale. Smartphone lenses are listed below in their own section with equivalents.

- **16 mm (ultrawide)** — Specialist range. Captures ~108° diagonal field of view on full-frame. Strong barrel distortion at edges; straight lines bow outward. Good for astrophotography or architectural interiors. Avoid for any face closer than full-body.
- **24 mm (wide)** — Wide enough for full-body and environmental shots. Pronounced perspective distortion: nearby elements look huge, distant ones disproportionately small. At 8 inches from a face, midface is vertically stretched ~12% vs gold standard — unflattering for portraits. *Default smartphone main-camera equivalent (~24–28 mm).*
- **35 mm (standard wide / "street")** — Approximates how the naked eye sees a scene. Less distortion than 24 mm but still wide enough that close-ups warp facial features (~14% midface stretch at 8"). Ideal for full or half-body portraits that **show subject + environment**. Classic street and reportage focal length.
- **50 mm ("nifty fifty" / standard)** — Closest to the human eye's central perspective. "Pure" rendering with minimal distortion at normal distances; still produces midface stretch (~19%) at 8". Versatile for half-body to close-up if shooting distance is respected. Demands an interesting subject because the rendering is undramatic.
- **85 mm (the portrait classic)** — The "holy grail" of headshots. Flattering compression keeps facial proportions accurate, shallow depth of field at f/1.8–f/1.2 produces the signature subject-pop with creamy bokeh. Comfortable working distance — neither subject nor photographer crowds the other.
- **100 mm (macro / portrait crossover)** — Marketed as a macro lens but excellent for portraits: longer reach than 85 mm with similar flattering compression. Useful for tight headshots and beauty close-ups.
- **135 mm (telephoto portrait)** — Background elements appear larger and closer due to **compression**; produces a "grandiose" cinematic feel against scenic backdrops. Very shallow depth of field; focus is harder to nail at close range. Best for half-body portraits at distance.
- **200 mm+ (telephoto / sports / wildlife)** — Extreme compression. Subject pops sharply against a heavily blurred background. Awkward shooting distance for portraits (the photographer is 5–10 m away). Common in fashion editorials and sports.

> **Reference rule (clinical study):** To avoid midface distortion on a full-frame camera, shoot **at least 24 inches** from the subject's face regardless of focal length. ([quantifying-facial-distortion.md](../../sources/phography/photography_lexicon/quantifying-facial-distortion.md))

## Lens categories (full-frame)

- **Ultrawide:** < 24 mm. Specialist; heavy distortion.
- **Wide-angle:** 16–35 mm. Environmental, landscape, architecture.
- **Standard:** 35–85 mm. "Natural perspective"; everyday and portrait.
- **Telephoto:** 85 mm+. Compressed perspective; subject isolation.
- **Super-telephoto:** 300 mm+. Sports, wildlife, distant subjects.

---

## Exposure triangle — aperture, shutter, ISO

The three dials that control how much light hits the sensor. **Each is measured in "stops"**: one stop = doubling or halving the light. Change one, compensate with another to keep the same exposure but a different look.

### Aperture (f-number)

The size of the opening inside the lens. **Backwards numbering: small number = big opening = more light + shallower depth of field.**

Standard full-stop scale (each step halves the light vs the previous):

`f/1.4 → f/2 → f/2.8 → f/4 → f/5.6 → f/8 → f/11 → f/16 → f/22`

- **f/1.2–f/1.8 (fast / wide open)** — Heavy background blur; razor-thin focus plane. At 85 mm and close range, only one eye may be sharp. Use sparingly: just because a lens *can* shoot f/1.2 doesn't mean every shot should.
- **f/2.8** — Standard "fast" zoom aperture. Good subject separation while keeping the whole face in focus.
- **f/4–f/8 (stopped down)** — Both eyes and nose in focus on a portrait. Backgrounds still soften with longer focal lengths.
- **f/8–f/11** — Landscape range; sharp foreground to horizon.
- **Aperture's creative trade-off:** It controls brightness *and* depth of field on the same dial. That tension is what makes the choice non-trivial.

### Shutter speed

How long the sensor is exposed. Measured in fractions of a second; each step doubles the time and the light.

`1/1000 → 1/500 → 1/250 → 1/125 → 1/60 → 1/30 → 1/15 → 1/8`

- **1/1000 s+ (fast)** — Freezes action. Sports, splashing water, jumping subjects.
- **1/250–1/125 s** — Safe handheld for normal lenses. Stops casual movement.
- **1/60 s** — Hand-holdable threshold for static subjects on a standard lens.
- **1/30 s and slower** — Tripod required. Introduces motion blur (silky waterfalls, light trails).
- **Reciprocal rule:** Minimum handheld shutter speed = 1 / focal length. On a 50 mm lens, use 1/50 s or faster; on 200 mm, 1/200 s. Stabilization buys ~2 stops; the principle holds. **Camera-shake blur ≠ creative motion blur.**

### ISO

How sensitive the sensor is to light. Doubling ISO doubles brightness, like opening one stop of aperture or doubling shutter time.

`100 → 200 → 400 → 800 → 1600 → 3200 → 6400`

- **ISO 100–200** — Cleanest files, full dynamic range. Default for daylight and tripod work.
- **ISO 400–800** — Indoor / overcast. Still very clean on modern cameras.
- **ISO 1600–3200** — Low-light handheld. Visible noise, especially in shadows; manageable on full-frame, more aggressive on smartphones.
- **ISO 6400+** — Survival mode. Noise becomes a stylistic choice or a known compromise. *A noisy photo of the moment beats a sharp photo of nothing.*

### Depth of field & bokeh

- **Depth of field (DoF)** — How much of the scene is in focus front-to-back. **Shallow DoF** (blurred background) requires wide aperture + longer focal length + closer subject + larger sensor. **Deep DoF** results from narrow aperture, wide lens, or small sensors (which is why smartphones look "everything-in-focus" by default).
- **Bokeh** — Aesthetic quality of the out-of-focus areas. Round/smooth = "creamy"; busy/polygonal = "nervous" / "distracting."
- **Reciprocal compensation example:** Open aperture from f/5.6 → f/2.8 (2 stops more light) → either speed shutter from 1/500 → 1/2000 (2 stops faster) or drop ISO from 200 → 50. Same exposure, different look.

### Quick mode-by-mode cheat sheet

- **Portraits:** Aperture Priority, f/1.8–f/4, Auto ISO with min shutter 1/125.
- **Landscapes:** Aperture Priority, f/8–f/11, ISO 100, tripod if shutter < 1/60.
- **Action:** Shutter Priority, ≥ 1/500, Auto ISO.
- **Low-light handheld:** Open wide, slowest handheld shutter (reciprocal rule), raise ISO until exposed.

---

## Distortion vocabulary

- **Perspective distortion (the "selfie effect")** — Caused by short focal length + close distance, not the lens itself. The closer the camera, the more exaggerated the nearest feature. At 8" with a 24–50 mm lens, the midface stretches 12–19% vertically; nose looks larger; chin and forehead appear smaller.
- **Barrel distortion** — Straight lines bow outward, especially near frame edges. Worsens with shorter focal length. Visible curving of building edges or door frames in ultrawide shots.
- **Vignetting** — Darkening at the corners of the frame. Often a wide-aperture or wide-lens artifact; can be corrected or stylistically exaggerated in post.
- **Compression (telephoto compression)** — The opposite of distortion: longer focal lengths make background elements look closer to and larger relative to the subject. Visually flattens depth.
- **Crop factor / focal length multiplier** — On a smaller (APS-C) sensor, a lens's effective focal length is multiplied (1.6× on Canon APS-C). A 50 mm lens on APS-C frames like an 80 mm lens on full-frame.

---

## Smartphone / UGC presets

Translate to full-frame equivalents for consistency with the focal-length section above.

- **Main camera (1×, "Wide")** — ~24–28 mm equiv, f/1.5–f/1.8. Largest sensor in the phone. Best image quality, best low-light. **Default for everything except deliberately wide or zoomed-in shots.** Visual character: slight wide-angle perspective, deep DoF (everything sharp unless you're very close).
- **Ultra-wide (0.6×, "UW")** — ~12–15 mm equiv, ~100–120° field of view, often f/1.8–f/2.2. Smaller sensor → lower resolution (e.g. 12 MP vs 50 MP on main), worse low-light. **Visible barrel distortion at edges; faces near the frame edge stretch.** Use for landscapes, interiors, group shots — not headshots.
- **Telephoto (2×, 3×, 5×, "T")** — ~50–120 mm equiv, smaller aperture (f/2.4–f/2.8), smaller sensor. Optical zoom — much sharper than digital zoom. **Best phone option for flattering portraits**: compression is similar to 50–85 mm full-frame. Needs good light; struggles in dim conditions.
- **Front camera ("selfie")** — Typically wide (~24–28 mm equiv). Held at arm's length (8–18 inches), produces the classic "selfie distortion": stretched midface, larger nose, smaller ears. **Unflattering for headshots by physics, not user error.**
- **Front camera, ultra-wide selfie mode** — Even wider FoV for group selfies. Center subject is fine; subjects at the edges look stretched.
- **Portrait mode (simulated shallow DoF)** — Software-generated background blur using AI/depth estimation. Can fail at hair edges, glasses, or busy backgrounds. Visually mimics 85 mm f/1.8 but looks "computational" on close inspection (sharp halo around subject, blurred parts of the subject itself, geometric blur inconsistencies).
- **Macro mode** — Triggered automatically on many phones when the lens is moved very close to a subject; usually switches to the ultra-wide lens with closer focusing. Useful for product detail; not for faces.
- **Night mode** — Multi-frame capture and merge to brighten shadows and reduce noise. Requires steady hold (or tripod). Increases the chance of motion blur on moving subjects.
- **Digital zoom** — Pure crop of the main sensor's image. Degrades detail proportionally. **Always prefer optical (telephoto) zoom when available.**
- **Panorama mode** — Stitches a horizontal or vertical pan into one wide image. Use 1×+ (not ultra-wide) to reduce distortion in the stitch.

---

## Lighting — core components

The vocabulary every lighting setup is built from. **Each light has a job**: illuminate, shape, separate, or fill.

- **Key light** — The dominant ("boss") light source. Establishes exposure, defines where shadows fall, sets mood. Most commonly placed 45° from camera, slightly above eye level. Using only a key light produces a high-contrast, dramatic look.
- **Fill light** — The secondary light placed opposite the key. **Lifts shadows without erasing them.** Can be a dedicated light, a bounce/reflector, or a scrim-diffused source. The key:fill ratio controls drama (see "Contrast ratios" below).
- **Backlight** — Light placed behind the subject, pointing toward the camera. **Creates separation from the background**, can produce a halo or silhouette. Often used as the third light in a three-point setup.
- **Hair light** — A specialised backlight aimed at the **top/back of the head**. Subtle highlight on hair and shoulders. Critical when subject has dark hair on a dark background. Position: above + slightly behind the subject.
- **Rim light** — Light from **directly behind**, lower than hair light, aimed at the subject's back. Creates a thin "silver lining" that traces the entire silhouette. Higher power than a hair light (e.g. 1/4 power vs 1/128).
- **Kicker light** — A backlight placed **opposite the key**, skipping across the shadow side of the face. Adds a highlight on the cheek; brings out facial structure. Often dialled low so only reflected light reads. Great for portraits of men and dramatic looks.
- **Background light** — A separate light aimed at the backdrop. Eliminates background shadows or adds detail/colour to the wall behind the subject. Should be flagged so it doesn't spill onto the subject.
- **Catch light** — A specular highlight in the subject's eyes caused by any light source. Small but **brings the face alive**. Photographers actively position lights to land catch lights at "10 or 2 o'clock" in the iris.
- **Ambient light** — Whatever light already exists in the room (windows, overheads, reflected daylight). Often treated as **unwanted** unless deliberately mixed with controlled sources.

### Hair light vs Rim light vs Kicker — a clarifying triplet

Often used interchangeably, but they're three distinct visual effects:

- **Hair light:** *Above* the subject, on the same side as the key. Subtle hair/shoulder highlight. Lowest power. Job = polish, depth.
- **Rim light:** *Behind* the subject. Outlines the entire silhouette in a thin glow. Mid-to-high power. Job = subject-from-background separation.
- **Kicker light:** *Opposite the key*, low and to the side, skipping across the shadow cheek. Low power. Job = sculpt the shadow side; adds drama and modeling.

## Lighting — quality & contrast

- **Hard light** — Small light source relative to subject (the sun, bare bulb, distant flash). **Sharp shadow edges.** Sculptural, dramatic, unforgiving on skin. As a light source moves further away, it effectively becomes harder.
- **Soft light** — Large light source relative to subject (overcast sky, big softbox, window with sheer curtain). **Gentle shadow edges.** Flattering for skin. Achieved by diffusing (sending light through silk/scrim) or bouncing off a large surface.
- **Diffusion vs Distance vs Dimming:** All reduce intensity, but **not interchangeably**. Diffusion also softens; distance also hardens (smaller relative source) and can spread the light wider; dimming changes only intensity, not character.
- **High-key** — Bright, low-contrast scene, mostly highlights, soft shadows. Reads upbeat, clean, commercial. Achieved with high fill ratio (key:fill close to 1:1).
- **Low-key** — Dark, high-contrast scene, mostly shadows with selective highlights. Reads moody, intimate, cinematic. Achieved with low fill ratio (key:fill 4:1+) or no fill.

## Lighting — contrast ratios (key:fill)

The ratio between key and fill brightness — the single biggest lever for mood.

- **1:1 (flat / commercial)** — Even illumination both sides; almost no visible shadow. Beauty, e-commerce, corporate headshots.
- **1.5:1** — Inviting, polished, slight modeling. Talking-head YouTube, interviews.
- **2:1 (cinematic standard)** — Key twice as bright as fill. Visible shadow side; dimensional. Default for narrative film and most "professional" YouTube.
- **3:1–4:1** — Dramatic. Shadow side clearly darker; mood-forward.
- **8:1+** — Near-silhouette territory; only shape reads on the shadow side. Horror, noir.
- **Practical fill rule (video):** Fill at 50–75% of key for cinematic; 85–95% for commercial; 25–45% for narrative drama.

## Lighting — common setups

- **One-light setup** — Single key (often a flash) + ambient daylight as de facto fill. Key 45° from camera, just above head height. The cheapest professional look.
- **Three-point lighting** — Key (front-side) + Fill (opposite, lower intensity) + Back/Hair/Rim/Kicker (separation). The "home base" of portrait and video lighting; nine out of ten polished talking-head videos use it.
- **Butterfly (paramount) lighting** — Key directly in front of subject, well above head, angled down. Creates a small **butterfly-shaped shadow under the nose**. Optional reflector below to lift the chin. Glamour, beauty, fashion.
- **Rembrandt lighting** — Key 45° to the side, 6–7 ft up. Creates a small **triangle of light on the shadow cheek** (under the eye). Flattering on most face shapes; the canonical "classical portrait" look.
- **Split lighting** — Key directly to the side (90°) and lower. Illuminates exactly **half the face**. Slimming, dramatic. Use minimal or no fill for max effect.
- **Loop lighting** — Key 30–45° to the side at slightly above eye level. Creates a small loop-shaped shadow from the nose toward the cheek (doesn't touch). Versatile, flattering default.
- **Clamshell lighting** — Two-light: key above eye-line + fill directly below the subject (often a reflector at chest height). **Soft, even, flattering** — strong eye catchlights. Standard for beauty and influencer/UGC headshots.
- **Rim / profile lighting** — Subject turned 90° to camera; key placed behind to illuminate the profile edge. Hair/background lights optional, on the opposite side. Editorial, dramatic.
- **Headshot lighting** — Rembrandt-style key + dedicated hair light 3–4 ft above subject (with diffuser). Used for darker backgrounds where the subject's head would blend in.

## Lighting — placement vocabulary (video)

- **Smart side** — The side of the subject **facing away from camera**. Traditionally where the key is placed; gives the most depth.
- **Dumb side** — The side of the subject **closer to camera**. Traditionally where the fill is placed.
- **Motivation** — The implied real-world source for a light in a scene (e.g. "the practical lamp on the desk justifies the warm key from camera-left"). Cinematic lighting reads as natural when motivated.
- **Flagging** — Blocking part of a light's path with a flag/barn-door so it doesn't spill where it shouldn't (e.g. into the lens or onto the background).

## Color temperature & white balance

Light has color, measured in **Kelvin (K)** on a scale roughly from 1,000 K to 10,000 K. **Lower K = warmer/oranger; higher K = cooler/bluer.**

### Reference values

- **~1,800 K** — Candle flame.
- **~2,700–3,000 K** — Tungsten / incandescent / warm-white fluorescent. Cozy, domestic.
- **~3,200 K** — Standard "tungsten" film light. Warm.
- **~4,000 K** — Warm fluorescent / early evening. Slightly warm but more neutral.
- **~5,200 K** — **Direct sunlight.** The reference "neutral" for most cameras' "Daylight" preset.
- **~5,400 K** — Electronic flash / strobe.
- **~5,600 K** — Standard "daylight" video LED. Industry default for professional video.
- **~6,000 K** — Overcast daylight.
- **~6,500 K** — Daylight fluorescent.
- **~8,000 K** — Open shade / blue hour.
- **~9,000–10,000 K** — Deep shade, twilight, "moonlight" stylization.

### White balance (WB)

A camera setting that compensates for the color of the light source so **true whites read as white**. Set the camera's WB to match the Kelvin of your scene's dominant light.

- **Auto WB (AWB)** — The camera picks. Reliable for daylight, struggles under mixed light or strong color casts.
- **Match-the-source WB** — Set camera to the light's actual K (5,600 K under daylight LEDs, 3,200 K under tungsten). This is the **professional default** when you control the lights.
- **Preset WB** — Camera presets (Daylight, Cloudy, Shade, Tungsten, Fluorescent, Flash) approximate the standard Kelvin values above. Useful when you don't know exact values.
- **Custom / Preset Manual WB** — Photograph a neutral gray or white card under the actual lighting; the camera derives the precise WB. Use under mixed/colored light or studio strobes where AWB fails.

### Creative WB ("warm" / "cool" looks)

- **Cool / moonlight effect:** Keep camera WB at 5,600 K but set lights warmer (e.g. 4,000 K) — image leans warm. Reverse to make the scene look cold/blue (lights at 9,000–10,000 K, camera at 5,600 K).
- **Warm / cozy effect:** Camera WB matched, but lighting choice (tungsten, late-afternoon natural) gives the scene its warm cast.
- **Golden hour** — The hour after sunrise / before sunset. Naturally warm (~3,000–4,500 K), low-angle, soft. Universally flattering; the most-used natural-light window for UGC and brand content.
- **Blue hour** — The 20–30 min before sunrise / after sunset. Cool, ambient, no harsh shadows. Cinematic; common in lifestyle and travel content.

### Mixed-light gotcha

Tungsten + daylight in the same scene = one will read orange and the other blue, no matter what WB you pick. Either gel a light (CTO/CTB) to match the other source, or kill one and rebuild.

---

## Watch out for

- **Don't equate focal length with distortion.** The clinical study shows distortion is driven by **distance**, not the lens. A 24 mm shot at 60 inches is fine; a 50 mm shot at 8 inches is not. Always check both.
- **Smartphone "wide" is what a full-frame "wide" looks like.** Don't double-count — when an agent says "use a wide lens" on a phone, that's already the default 1× main camera, not the 0.6× ultra-wide.
- **Portrait mode ≠ real shallow DoF.** Software bokeh fails at edges. Don't treat it as equivalent to an 85 mm f/1.8 capture for high-end work.
- **Don't conflate hair / rim / kicker.** They sit in different positions and do different jobs. An agent recommending a "rim light" when the user wants a subtle hair highlight will overlight the shot.
- **Auto WB will fight you under mixed light.** When designing a UGC brief, specify both the light's color temperature and the camera's WB setting — otherwise different shooters will get inconsistent looks.
- **Diffusion, distance, and dimming are not interchangeable** for reducing light intensity — they each change quality differently.
- **High ISO is the compromise dial, not a default.** Raise it only when aperture and shutter speed cannot get enough light alone.

## Frameworks / models

- **Distance-first framing rule:** Pick subject distance before focal length. ≥24" from a face avoids midface distortion regardless of lens.
- **Smartphone lens decision tree:** Default to 1× main → switch to telephoto for portraits or distant subjects → switch to 0.6× only when the scene won't fit and you accept resolution + edge-distortion tradeoffs.
- **DoF triangle:** Background blur increases with (longer focal length) × (wider aperture) × (closer subject) × (larger sensor). Smartphones are short on the last two, which is why phone backgrounds rarely blur naturally.
- **Exposure triangle:** Aperture (DoF) × Shutter (motion) × ISO (noise). For a given scene brightness, infinite combinations produce the same exposure but different *looks*. Choosing the trade-off = the photographer's job.
- **Three-point lighting:** Key (illuminate) + Fill (control contrast) + Back/Hair/Rim/Kicker (separate from background). The home base for 90% of UGC and YouTube setups.
- **Source × Angle × Intensity (S.A.I.):** Every light decision boils down to (1) where it physically originates, (2) the path/angle to subject, (3) brightness. Same source can produce wildly different looks across the three.

## How to apply

- **In Path A (automated visual decisions):** Cite specific entries by name when justifying a lens, distance, or lighting choice. E.g. "Choosing 85 mm at 1.5 m + Rembrandt key with 2:1 fill per `photography_lexicon.md` — flattering compression, classical portrait modeling."
- **In creative briefs:** Translate target visual ("intimate cinematic close-up") into lexicon-grounded specs ("85 mm equivalent at 1.5 m, low-key, 3:1 contrast ratio, soft window key from camera-left + bounce fill, WB 5,200 K").
- **In QA of AI-generated or user-submitted UGC:** Use the distortion + lighting + WB vocabulary to name what's wrong ("midface stretching consistent with selfie distance; flat 1:1 ratio reads commercial when brief asked for moody; WB skewed warm — looks like AWB lock under tungsten + daylight").

## See also

- [_focal-length-portrait.md](../../sources/phography/photography_lexicon/focal-length-portrait.md) — Fstoppers, Illya Ovchar
- [_understanding-focal-length.md](../../sources/phography/photography_lexicon/understanding-focal-length.md) — Canon Georgia
- [_perfect-portrait-lens.md](../../sources/phography/photography_lexicon/perfect-portrait-lens.md) — B&H eXplora
- [_quantifying-facial-distortion.md](../../sources/phography/photography_lexicon/quantifying-facial-distortion.md) — Derakhshan et al., *The Laryngoscope* 2024 (clinical distortion study)
- [_mobile-photography.md](../../sources/phography/photography_lexicon/mobile-photography.md) — A.D.A.M. Singapore
- [_wide-angle-lens.md](../../sources/phography/photography_lexicon/wide-angle-lens.md) — Adobe
- [_wide-lens-android.md](../../sources/phography/photography_lexicon/wide-lens-android.md) — Popsa, Dan Mold
- [_exposure-triangle-explained.md](../../sources/phography/photography_lexicon/exposure-triangle-explained.md) — Fstoppers, Alex Cooke
- [_exposure-triangle-beginner.md](../../sources/phography/photography_lexicon/exposure-triangle-beginner.md) — Photography Life, Elizabeth
- [_lighting-for-photography.md](../../sources/phography/photography_lexicon/lighting-for-photography.md) — Corel Discovery Center (one-light, butterfly, Rembrandt, rim, split, headshot)
- [_photography-lighting.md](../../sources/phography/photography_lexicon/photography-lighting.md) — Aftershoot (split, butterfly, clamshell, Rembrandt)
- [_three-light-portrait.md](../../sources/phography/photography_lexicon/three-light-portrait.md) — Envato Tuts+, Jamie Evan (hair vs rim vs kicker)
- [_three-point-video-lighting.md](../../sources/phography/photography_lexicon/three-point-video-lighting.md) — StudioBinder, SC Lannom (key/fill/back, contrast ratios, smart vs dumb side)
- [_light-techniques.md](../../sources/phography/photography_lexicon/light-techniques.md) — Ed Verosky (backlighting: halo, hair, rim/kicker, silhouette, lens flare)
- [_color-temperature.md](../../sources/phography/photography_lexicon/color-temperature.md) — Hyph Tech (WB & Kelvin scale)
- [_achieving-natural-colors.md](../../sources/phography/photography_lexicon/achieving-natural-colors.md) — Nikon (white balance presets table with Kelvin values)
