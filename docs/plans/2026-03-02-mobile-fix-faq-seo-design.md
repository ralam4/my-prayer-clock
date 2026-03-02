# My Prayer Clock — Mobile Fix, FAQ & SEO Redesign

## Date: 2026-03-02

## Problem
Mobile layout has footer overlapping content, excessive whitespace around phone mockup, and feature pills rendering below footer. Site also lacks FAQ content for AI/SEO discoverability.

## Page Structure

```
Nav (sticky)
─────────────
Phone Mockup (centered carousel, rotating)
─────────────
Eyebrow ("Free for iPhone · iOS 26+") + Headline + Subtitle
App Store Badge
"Free · No account · No tracking" note
Feature pills (2×2 grid on mobile)
─────────────
FAQ Section (4 expandable Q&As with FAQPage JSON-LD)
─────────────
Final CTA ("Ready to pray on time?" + App Store badge)
─────────────
Footer
```

## Changes

### 1. Fix Mobile Layout
- Remove `overflow: hidden` from body on ALL screen sizes
- Desktop hero uses `min-height: 100dvh` instead of rigid flex+hidden
- Phone mockup on mobile: centered, `height: 380px`, tight padding
- Feature pills: 2×2 grid with `margin-bottom: 32px`
- App Store badge: cap at `160px` width on mobile
- Footer: normal document flow, always below content

### 2. Update iOS Version
- Change "iOS 16+" → "iOS 26+" everywhere (eyebrow, FAQ, JSON-LD)

### 3. Add FAQ Section
Native `<details><summary>` elements, no JS. Questions:

1. **Is My Prayer Clock really free?**
   Yes — completely free with no in-app purchases, no subscriptions, and no ads.

2. **How accurate are the prayer times?**
   Calculated using precise GPS location with established Islamic methods (ISNA, MWL, Egyptian, Umm al-Qura, and more). Updates automatically as you travel.

3. **Does the app track my data or require an account?**
   No. Zero personal data collected. No account, no analytics, no third-party tracking. Location stays on device.

4. **What features does My Prayer Clock include?**
   All 5 daily prayer times, Qibla compass, Ramadan fasting tracker, prayer streak tracking, home screen widgets, light and dark modes. iPhone with iOS 26+.

JSON-LD `FAQPage` schema added to `<head>`.

### 4. Add Final CTA Section
Centered block: "Ready to pray on time?" + subtitle + App Store badge.

### 5. Desktop Adjustments
- Hero keeps side-by-side layout (copy left, phone right)
- Switches from `overflow: hidden` to `min-height: 100dvh` — allows natural scroll to FAQ/CTA
- FAQ + CTA are new sections below the fold

## Files Modified
- `index.html` — FAQ section, CTA section, iOS version, FAQPage JSON-LD
- `styles.css` — mobile layout fix, FAQ styles, CTA styles, remove overflow:hidden
