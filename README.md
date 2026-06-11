# youtube-title-ab-tester

Compare 2 to 5 candidate video titles side by side. Length, word overlap, signal patterns, search-result preview. Browser only.

**Live demo:** https://0xelitesystem.github.io/youtube-title-ab-tester/

## Use

Open [`index.html`](./index.html). Type or paste up to five title variants. Click Compare.

For each variant, the tool shows:

- Character count and visible-area warning (titles over ~60 chars truncate)
- Word count
- Signals detected (number, year, question, brackets, all-caps, multi-exclamation, emotion words, colon, "vs", "how to", explanation pattern)
- Search-result-style preview

Across all variants, the tool also shows a word-overlap visualization. Heavy overlap means your variants test the same hook with cosmetic changes; little overlap means they test genuinely different framings. That's the comparison that actually matters.

## Why

Title testing is mostly intuition. Real YouTube A/B test tools require the video to be live and accumulate impressions before they tell you anything. By then it's too late to change your gut feeling about which title to start with.

This is a pre-publish gut-check tool. It surfaces patterns you can use as inputs to your judgment. It does NOT predict which title will perform better, because no tool can do that reliably.

## What this is not

- Not a CTR predictor. Anyone selling that is selling a fantasy.
- Not a clickbait optimizer. Some signals it surfaces (multi-exclamation, all-caps) are flags AGAINST overuse, not goals to hit.
- Not connected to YouTube. No API. No login. No data leaves your browser.
- Not a substitute for actually testing on your channel. YouTube has its own A/B test feature for that.

## Privacy

Everything runs locally. The titles you paste never leave your browser. Verify with DevTools network tab.

## Run locally

```
git clone https://github.com/0xelitesystem/youtube-title-ab-tester
cd youtube-title-ab-tester
```

Open `index.html` in any browser. Or:

```
python -m http.server 8000
```

## Contribute

PRs welcome:

- Better signal detection (named entity recognition, sentiment lexicon)
- Localization (different languages have different effective title lengths)
- Additional comparison metrics
- Specific YouTube category context (gaming titles work differently from tutorial titles)

Don't add: external scripts, npm dependencies, telemetry. Single file.

## Build

No build. Single HTML file.

## License

MIT.

## Related

- [youtube-thumbnail-tester](https://github.com/0xelitesystem/youtube-thumbnail-tester) - preview thumbnails across YouTube placements
- [youtube-chapter-marker-builder](https://github.com/0xelitesystem/youtube-chapter-marker-builder) - validate chapter timestamps
- [youtube-creator-checklist](https://github.com/0xelitesystem/youtube-creator-checklist) - pre-publish checks
