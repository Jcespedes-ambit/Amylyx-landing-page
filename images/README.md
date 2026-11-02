# Images

Drop generated/stock images here with these exact filenames and the page will use them
automatically. Until a file exists, the page falls back to a purple gradient (nothing looks broken).

| File | Used in | Target size | Format |
|------|---------|-------------|--------|
| `hero.webp` | Hero background (behind the purple overlay) | ~2000 × 1200 (5:3), landscape | WebP or JPG |
| `guide.webp` | "Meet Your Ambit Guide" portrait card | ~1200 × 750 (16:10), landscape | WebP or JPG |
| `topic-1.webp` | "Explore Topics" card 1 (Education) thumbnail | ~800 × 450 (16:9), landscape | WebP or JPG |
| `topic-2.webp` | "Explore Topics" card 2 (Symptoms) thumbnail | ~800 × 450 (16:9), landscape | WebP or JPG |
| `topic-3.webp` | "Explore Topics" card 3 (Next Steps) thumbnail | ~800 × 450 (16:9), landscape | WebP or JPG |

Notes
- The hero image sits **behind** a dark-violet gradient that is strongest on the left (where the
  headline is) and lighter on the right. Pick/generate an image whose important content sits
  **right-of-center**; the left third is covered by text.
- Keep file sizes small (ideally < 300 KB each) so the page stays fast. If you export JPG/PNG,
  you can keep the name (e.g. `hero.jpg`) but then update the `--hero-photo` / `--guide-photo`
  variables at the top of `../index.html` to match the extension.
- No people from real stock libraries that require licensing for commercial use unless the license
  is cleared; AI-generated or properly-licensed stock only.

## Generator prompts

**hero.webp (5:3 landscape):**
> Calm, hopeful lifestyle photograph for a healthcare landing page about a chronic lung condition.
> A relaxed middle-aged adult outdoors in soft natural morning light, breathing easily, serene
> expression, looking into the distance. Shallow depth of field, airy and bright, muted cool tones
> that sit well under a violet overlay. Subject positioned on the RIGHT side of the frame with open,
> uncluttered space on the left. No text, no logos, premium healthcare brand photography. 5:3 landscape.

**guide.webp (16:10 landscape):**
> Warm, approachable photograph of a friendly healthcare support professional (a patient "guide"),
> mid-adult, smiling gently, wearing a soft-colored top, in a bright, clean, out-of-focus office
> setting. Natural light, welcoming and trustworthy mood, soft cool/lavender color grade. Head and
> shoulders, looking toward camera. No text, no logos, premium brand photography. 16:10 landscape.
