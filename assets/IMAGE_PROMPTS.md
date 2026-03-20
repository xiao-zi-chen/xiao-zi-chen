# Image Prompt Pack

These prompts are for upgrading the current profile README from abstract cyber visuals to a stronger anime identity.

## Visual Direction

Use these style anchors consistently:

`anime + cyberpunk + clean composition + premium lighting + personal branding + not overcrowded`

Color direction:

- electric blue
- pink highlight
- violet glow
- deep navy background

Mood direction:

- cyber academy
- security lab at night
- holographic interface
- composed and intelligent, not chaotic

## Asset 1: Main Banner

Use:
- top hero image in `README.md`
- replace `assets/hero-cyber.svg`
- generate with aspect ratio: `21:9` first choice, `16:9` second choice
- crop after generation to a banner-friendly wide image
- file name: `assets/banner-anime.png`

Prompt:

```text
Anime-inspired personal branding banner for a young male cybersecurity and AI developer, half-body composition, calm confident expression, black or dark brown hair, modern clean outfit with subtle futuristic details, cyber academy aesthetic, neon blue and pink rim lighting, holographic user interface panels, code fragments, terminal glow, elegant tech city night atmosphere, premium composition, very high detail, clean negative space for title text, polished lighting, cinematic wide layout, sharp face details, professional but distinctly anime
```

Negative prompt:

```text
low quality, blurry, extra limbs, extra fingers, duplicate character, text, watermark, logo, cluttered composition, deformed hands, cropped face, noisy background
```

### Stable Version For Fewer Hallucinations

Use this version if the model keeps producing fake code, broken hands, or messy panels.

Prompt:

```text
Wide anime-style banner for a young male cybersecurity developer, upper-body portrait only, character placed on the left third of the frame, calm and confident expression, black hair, clean futuristic jacket, neon cyan and magenta rim light, elegant night city background, subtle holographic interface shapes without readable text, minimal abstract UI frames, premium lighting, polished anime illustration, clean composition, large empty space on the right for profile title, no hand gestures, hands mostly out of frame, visually sharp face, professional and refined
```

Negative prompt:

```text
readable text, letters, words, code, terminal text, watermark, logo, extra fingers, extra hands, malformed hands, extra limbs, duplicate character, multiple people, busy background, cluttered UI, distorted face, cropped head, blurry image, low quality
```

Why this is more stable:

- remove `code fragments` because models often turn that into fake text
- remove complex hand actions because fingers are a common failure point
- switch from `half-body` to `upper-body portrait only`
- ask for `abstract UI shapes` instead of actual screens with content
- force `left-third composition` so the banner has usable blank space

Recommended ratio on your platform:

- best: `21:9`
- fallback: `16:9`

Crop rule:

- keep the character on the left
- keep empty space on the right for the title area
- if the top area is too empty, crop some of the upper background away

### Banner V2: Safer Composition

Use this if the model keeps making the composition too dark, too empty, or keeps drawing fake interface text.

Prompt:

```text
Clean wide anime banner for a young male cybersecurity developer, chest-up portrait, character on the right third of the frame, facing slightly toward the center, calm serious expression, black hair, sleek dark futuristic jacket with subtle neon cyan and magenta accents, soft night city background, very light holographic glow only, no floating screens with content, no code, no readable interface, premium polished anime illustration, balanced lighting, clear silhouette, medium contrast, elegant and minimal composition, large clean empty space on the left for profile text, professional and refined
```

Negative prompt:

```text
readable text, code, terminal, letters, numbers, floating windows, charts, dashboard content, extra fingers, extra hands, extra limbs, bad anatomy, duplicate character, messy background, huge dark shadow block, overexposed neon, cropped face, low quality, blur
```

What changed:

- put the character on the `right third` because your last result naturally drifted there
- explicitly ban `floating windows`, `charts`, and `dashboard content`
- ban `huge dark shadow block` to reduce the heavy black area
- ask for `very light holographic glow only` instead of full UI panels
- keep `chest-up portrait` to avoid unstable torso and hand details

If it still fails, use this ultra-short version:

```text
Wide anime banner, young male cybersecurity developer, chest-up portrait, character on the right third, black hair, dark futuristic jacket, cyan and magenta rim light, soft night city background, minimal holographic glow, no readable text, no code, no floating screens, clean empty space on the left, polished anime illustration, professional, minimal, sharp face
```

## Asset 2: Portrait Card

Use:
- replace `assets/profile-panel.svg` later or embed beside the profile intro
- generate with aspect ratio: `3:4` first choice, `2:3` second choice, `1:1` if you want a safer avatar crop
- file name: `assets/avatar-card.png`

Prompt:

```text
Anime portrait card of a young male developer, intelligent and composed, subtle smile, upper body, refined line art, dark hair, futuristic minimal jacket, cyber security researcher vibe, soft blue and magenta lighting, dark background with faint holographic interface elements, premium polished illustration, striking but professional, centered composition, visual novel quality
```

Negative prompt:

```text
bad anatomy, blurry eyes, extra face, extra fingers, watermark, text, low detail, distorted body, oversaturated skin, messy background
```

### Stable Version For Portrait

Prompt:

```text
Anime portrait of a young male cybersecurity developer, chest-up composition, centered face, calm expression, dark hair, minimal futuristic jacket, soft blue and magenta edge lighting, dark simple background, only a few abstract holographic lines behind the character, polished line art, clean skin details, visual novel quality, professional and elegant, no hands visible
```

Negative prompt:

```text
hands, fingers, extra face, asymmetrical eyes, text, watermark, blurry details, deformed anatomy, cluttered background, multiple characters
```

Recommended ratio on your platform:

- best portrait card: `3:4`
- fallback portrait card: `2:3`
- best for avatar/icon reuse: `1:1`

## Asset 3: Chibi Mascot

Use:
- side decoration in README
- issue templates, repo stickers, future portfolio site
- generate with aspect ratio: `1:1`
- file name: `assets/chibi-mascot.png`

Prompt:

```text
Cute chibi anime mascot version of a young male cybersecurity developer, dark hair, smart and calm expression, tiny futuristic jacket, floating holographic shield and terminal windows, blue pink neon accents, polished cel shading, transparent or simple dark background, adorable but clean and premium
```

Negative prompt:

```text
blurry, extra fingers, extra limbs, text, watermark, messy accessories, deformed face, duplicate elements
```

## Asset 4: Repo Cover Background

Use:
- repository social preview
- section backgrounds for the future website
- generate with aspect ratio: `16:9` first choice, `21:9` for extra cinematic space
- file name: `assets/repo-cover-01.png`

Prompt:

```text
Futuristic anime-style project cover background for cybersecurity and AI tools, dark premium interface surfaces, neon blue green pink accents, holographic layers, subtle network topology motifs, encrypted data streams, tactical dashboard feel, room for overlay title text, clean composition, high detail, no character
```

Negative prompt:

```text
text, watermark, chaotic layout, blurry, overexposed, low resolution, noisy background
```

### Stable Version For Background

Prompt:

```text
Minimal cyberpunk anime background for a cybersecurity project cover, no character, dark navy interface surface, neon cyan and violet accents, abstract network lines, abstract dashboard blocks, soft glow, premium clean composition, large empty area for overlay text, no readable interface content, elegant and restrained
```

Negative prompt:

```text
readable text, letters, numbers, watermark, chaotic panels, cluttered details, overexposed highlights, blurry image, low quality
```

## Practical Fix Rules

If image hallucination is still strong, follow these rules:

1. Do not ask for `code fragments`, `terminal content`, or `readable UI text`.
2. Prefer `upper body`, `chest-up`, or `portrait` over full body or hand-heavy poses.
3. Ask for `abstract holographic shapes` instead of multiple floating windows.
4. Keep only one character.
5. Ask for `simple background` or `subtle city night background`.
6. Generate first, then crop into the banner ratio instead of forcing too much detail into one shot.
7. If your generator supports it, use image editing or inpainting to fix only the face/background instead of regenerating everything.

## Asset 5: Pattern Texture

Use:
- section divider or website background
- generate with aspect ratio: `16:9`
- file name: `assets/pattern-grid.png`

Prompt:

```text
Minimal anime cyberpunk background texture, dark navy base, faint holographic grid, subtle diagonal scan lines, soft blue and violet glow, premium and restrained, elegant enough for website background, high detail, no characters, no text
```

Negative prompt:

```text
busy composition, extreme contrast, text, watermark, blur, low detail
```

## Asset 6: Sticker Set

Use:
- README decorations
- repo badges
- future website floating ornaments
- generate with aspect ratio: `1:1`

Prompt:

```text
Set of small anime cyberpunk sticker icons for a developer brand, holographic shield, terminal window, sakura pixel flower, cat-ear headset, chip icon, encrypted lock, glossy neon edges, consistent style, transparent background, polished illustration
```

Negative prompt:

```text
watermark, text, low quality, blurry, inconsistent style, messy outlines
```

## Optional Add-ons

For a stronger anime look, append:

```text
anime key visual, visual novel quality, polished cel shading, Japanese sci-fi illustration, cinematic bloom, layered depth
```

For a stronger security look, append:

```text
cyber defense dashboard, network topology glow, encrypted data streams, tactical hologram, blue alert lighting
```

## Replacement Map

After generation, you can replace these files or add new ones:

- `assets/banner-anime.png`
- `assets/avatar-card.png`
- `assets/chibi-mascot.png`
- `assets/repo-cover-01.png`
- `assets/pattern-grid.png`
- `assets/sticker-pack.png`

When you finish generating them, I can do the second pass:

1. swap the README from abstract SVG mode to custom-anime asset mode
2. build matching repo social preview images
3. build the full `xiao-zi-chen.github.io` site in the same visual language

## Quick Ratio Guide

Use this directly with your generator:

- banner: `21:9`
- portrait card: `3:4`
- avatar-only image: `1:1`
- chibi mascot: `1:1`
- project cover: `16:9`
- background texture: `16:9`
