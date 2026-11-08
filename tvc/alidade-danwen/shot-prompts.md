# ALIDADE ·《但闻》— AI Shot Prompts

**Workflow:** Midjourney / Flux (still plates) → Runway / Luma / Kling (I2V) → resolve / grade → composite type & bottle  
**Aspect:** 16:9 · cinematic still photography look · photoreal · no on-screen text in generation

---

## Global negative prompt

Use on every still and every I2V pass:

```
no particles, no glowing dust, no light leaks as VFX, no slow motion, no floating bottle,
no on-screen text, no logos, no watermarks, no subtitles, no typography,
no hands writing, no hands spraying perfume, no perfume mist spray visible,
no wind whipping trees, no exaggerated tree sway, no flying petals, no liquid splash,
no exploding liquid, no black-and-gold luxury cliché, no mansion, no epic sky replacement,
no morphing face, no extra fingers, no warped wood grain, no shaky cam, no orbit move
```

---

## Reference sheets (generate first, lock, reuse)

### REF-A · Lookout turnaround

```
photoreal character turnaround sheet, same woman three views front side back,
East Asian woman mid-30s, weathered calm face, short practical hair under wool beanie,
heavy charcoal wool sweater, faded olive field trousers, leather boots,
fire lookout ranger, neutral studio soft daylight, plain grey backdrop,
consistent face across views, full body, 16:9 --ar 16:9
```

### REF-B · Lookout cabin + Osborne Fire Finder set

```
photoreal interior of wooden fire lookout cabin, circular Osborne Fire Finder map table
at center with brass alidade sighting arms and thin taut wire across center pin,
topographic map under glass, azimuth ring, iron wood stove to the side,
panoramic windows, fir forest visible outside, pre-dawn cold blue light,
practical cabin clutter muted, no text readable, 16:9 cinematic --ar 16:9
```

### REF-C · Bottle hero still (for 3D / comp reference)

```
photoreal perfume bottle product still, acid-etched frosted glass body like rime ice,
pale grey-violet iris juice, charred shou sugi ban fir wood cap with cracked carbonized grain,
standing upright on matte wood, soft side light, no label text, no logo, no floating,
macro material detail, 16:9 --ar 16:9
```

### REF-D · Tower exterior

```
photoreal wooden fire lookout tower on mountain ridge among dense fir forest,
tall stilts, small glassed cabin on top, cold pre-dawn blue hour, no smoke,
no people, crisp silhouette, 16:9 landscape cinematic --ar 16:9
```

---

## Paired-plate method

| Pair | Shared base plate | Variant A | Variant B |
|------|-------------------|-----------|-----------|
| Shots 1 & 7 | REF-D composition locked | no smoke, cold blue | one thin chimney smoke thread, warmer sunrise |
| Shots 3 & 8 | top-down Fire Finder from REF-B | empty center pin, open logbook blank | bottle on center pin (comp), slightly warmer light |

Generate one locked still, then img2img / inpaint the delta only. Feed each still to I2V with near-zero camera move.

---

## Shot prompts

### Shot 1 · 0:00–0:04 · Pre-dawn exterior wide

**Refs:** REF-D  
**Duration:** 4s  
**Camera:** locked off, no move

**First frame:**

```
photoreal extreme wide shot, wooden fire lookout tower on fir-covered mountain ridge,
pre-dawn cold blue hour, clear air, absolutely no smoke, still forest, cinematic 16:9,
anisotropic landscape photography, fine grain --ar 16:9
```

**Motion (I2V):**

```
locked camera, almost no motion, only the faintest distant atmospheric stillness,
real-time speed, no cloud rush, no tree sway
```

**Sound cue:** distant soft bird call; near silence.

---

### Shot 2 · 0:04–0:07 · Lookout senses smoke

**Refs:** REF-A, REF-B  
**Duration:** 3s  
**Camera:** locked medium

**First frame:**

```
photoreal medium shot inside fire lookout cabin, woman from REF-A seated by window
holding enamel mug with both hands static grip, cold blue window light on face,
fir forest outside, calm then alert expression, cinematic 16:9 --ar 16:9
```

**Motion (I2V):**

```
locked camera, real-time, she pauses, subtle nose flare, eyes shift toward window,
minimal head turn, mug stays still in hands, no walking, no complex gestures
```

**Sound cue:** off-screen phantom wood crackle (very soft); tiny cup tick.

---

### Shot 3 · 0:07–0:11 · Fire Finder top-down

**Refs:** REF-B  
**Duration:** 4s  
**Camera:** locked overhead  
**Type:** later composite log line only — generate blank pages

**First frame:**

```
photoreal top-down shot of Osborne Fire Finder, circular topographic map table,
brass alidade arms and thin wire across exact center pin, azimuth ring,
blank open logbook at edge with no writing, cold blue cabin light,
one hand resting static on alidade arm edge, no text anywhere, 16:9 --ar 16:9
```

**Motion (I2V):**

```
locked overhead camera, real-time, alidade arm already stopped, tiny metal settle,
hand almost motionless, no writing motion
```

**Sound cue:** soft metal tap; pencil silence; phantom crackle weaker.  
**Post:** burn in `07:12 烟味。无火。` / `07:12 Smoke. No fire.` on log page.

---

### Shot 4 · 0:11–0:15 · Binocular search

**Refs:** REF-A, REF-B  
**Duration:** 4s  
**Camera:** locked over-shoulder / window frame

**First frame:**

```
photoreal over-shoulder shot, woman from REF-A holding binoculars to eyes with static grip,
looking out panoramic window over endless fir sea, no smoke columns in forest,
cold blue morning light, cinematic 16:9 --ar 16:9
```

**Motion (I2V):**

```
locked camera, real-time, slow horizontal pan of her torso and binoculars across the view
as if scanning, forest itself barely moves, no smoke appears
```

**Sound cue:** phantom crackle cut by metal stair tread clang; footsteps rising.

---

### Shot 5 · 0:15–0:19 · Stairwell descent / visitor ascending

**Refs:** REF-D materials (wood), grey-violet coat as iris note  
**Duration:** 4s  
**Camera:** locked vertical top-down  
**Character rule:** visitor = coat and shoulder only, no face

**First frame:**

```
photoreal vertical top-down shot into wooden fire lookout stairwell,
spiral or switchback timber stairs with fir handrails,
figure in pale grey-violet wool coat entering from bottom of frame ascending,
only shoulder and sleeve visible, no face, cold side light from narrow window,
cinematic 16:9 --ar 16:9
```

**Motion (I2V):**

```
locked top-down camera, real-time, figure climbs two or three steps upward into frame,
coat fabric micro-motion only, no face reveal, no other characters
```

**Sound cue:** metal-wood footfalls fill the mix; phantom crackle gone.

---

### Shot 6 · 0:19–0:23 · Recognition · match · real fire

**Refs:** REF-A, REF-B (stove)  
**Duration:** 4s  
**Camera:** locked close-up  
**Action:** match strike preferably off-screen; show face lit + flame entering stove

**First frame:**

```
photoreal close-up profile of woman from REF-A in lookout cabin, alertness softening
into recognition, iron wood stove nearby, cold light shifting as warm match glow begins,
cinematic skin texture, 16:9 --ar 16:9
```

**Motion (I2V):**

```
locked camera, real-time, subtle facial ease, warm light blooms on face,
small flame motion toward stove mouth, stove fire catches, no slow motion
```

**Sound cue:** bolt unlatches off-screen; match strike; real crackle replaces phantom.

---

### Shot 7 · 0:23–0:27 · Sunrise wide · single smoke thread (signature)

**Refs:** paired plate from Shot 1 / REF-D  
**Duration:** 4s  
**Camera:** identical lock to Shot 1

**First frame:**

```
photoreal extreme wide shot identical composition to the pre-dawn tower plate,
same wooden fire lookout tower among fir forest, now early sunrise warm gold light,
ONE thin straight smoke thread rising only from the cabin chimney,
rest of forest completely smokeless, cinematic 16:9 --ar 16:9
```

**Motion (I2V):**

```
locked camera identical to shot 1, real-time, only the thin chimney smoke drifts upward slowly,
no wind in trees, no extra smoke anywhere
```

**Sound cue:** near silence; farthest wind; tiny stove crackle as if inside the tower.

---

### Shot 8 · 0:27–0:30 · Bottle on center pin

**Refs:** paired plate from Shot 3 / REF-B + REF-C (comp)  
**Duration:** 3s  
**Camera:** identical lock to Shot 3  
**Product:** prefer 3D or photographed bottle composite onto empty-pin plate

**First frame (plate without bottle, for clean comp):**

```
photoreal top-down Osborne Fire Finder same composition as earlier overhead plate,
empty center pin, alidade arms unchanged, slightly warmer morning light than before,
no people, blank surfaces, no text, 16:9 --ar 16:9
```

**Optional full-gen fallback (if no 3D comp):**

```
same overhead Fire Finder plate, ALIDADE perfume bottle from REF-C standing on exact center pin,
frosted rime glass, pale grey-violet juice, charred fir cap, no label text, warmer light,
locked composition --ar 16:9
```

**Motion (I2V):**

```
locked overhead camera, almost still, tiny dustless air, real-time, no floating,
bottle remains planted on the pin
```

**Sound cue:** soft glass settle — or silence.  
**Post:** composite bottle if needed; add `ALIDADE` wordmark and optional film title 《但闻》 / SMOKE, NO FIRE in final frames only.

---

## Post-production checklist

- [ ] Shot 3: composite log line `07:12 烟味。无火。` (and/or EN `07:12 Smoke. No fire.`)
- [ ] Shot 8: composite bottle (3D/CG or plate) onto center pin; match warmth to sunrise grade
- [ ] Shot 8 end: composite `ALIDADE` wordmark; optional 《但闻》 / SMOKE, NO FIRE
- [ ] No generated typography left in any plate
- [ ] Grade arc: cold blue (1–4) → grey-violet accent (5) → warm gold (6–8)
- [ ] Sound design only: phantom crackle → stairs → match → real fire → silence on 7
- [ ] Pair QA: Shot 1 vs 7 pixel-align horizon and tower; Shot 3 vs 8 pixel-align map and arms
- [ ] Deliver 16:9 master, ~30s, no piano / epic score bed
