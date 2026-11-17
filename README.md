# Hash Collisions: From MD5 to SHA-1

Interactive presentation for **CEI 423 — Introduction to Cryptography and Computer Security**, Cyprus University of Technology.

**Presenters:** Μάριος Σιήττας · Μπογκντάν Νεματζιόνοβ

Link: https://marios-shittas.github.io/cei423-hash-collisions/hash-collisions-presentation.html

The whole presentation is a single self-contained HTML file: [`hash-collisions-presentation.html`](hash-collisions-presentation.html). It also embeds the two original SHAttered PDFs, so it works offline.

## How to open

Open `hash-collisions-presentation.html` in a recent version of Chrome, Edge, Firefox or Safari.

The live demos compute SHA-1 and SHA-256 with the browser's WebCrypto API, which needs a secure context. If a demo reports that WebCrypto is unavailable, serve the folder locally:

```sh
python3 -m http.server 8000
# then open http://localhost:8000/hash-collisions-presentation.html
```

MD5 (slide 3) uses a local RFC 1321 implementation, because WebCrypto does not support MD5.

## Controls

| Key | Action |
|---|---|
| `→` `↓` `Space` | Next slide or next animation step |
| `←` `↑` | Previous slide or previous step |
| `Home` / `End` | First / last slide |
| `PageUp` / `PageDown` | Previous / next slide, skipping the steps |
| `O` | Slide overview |
| `F` | Full screen |
| `?` | Help |
| `Ctrl/⌘ + Shift + 1 / 2 / 3` | Flame / SHAttered / Shambles deep dives |
| `Esc` | Close a dialog |

On slides 5, 7, 8 and 10 the arrow keys step through the timeline or the animated scenario first, then move to the next slide.

## Structure (≈ 15–16 minutes)

| # | Slide |
|---|---|
| 1 | Hash Collisions: From MD5 to SHA-1 |
| 2 | How a hash function works (properties; preimage / second preimage / collision resistance, compared visually) |
| 3 | Avalanche effect: live MD5 / SHA-1 demo |
| 4 | How hashing provides security |
| 5 | From MD5 to SHA-1: evolution & security (timeline) |
| 6 | Flame (2012): a real-world MD5 attack |
| 7 | Flame: the scenario step by step |
| 8 | SHAttered (2017): inside SHA-1 |
| 9 | Live verification of the SHAttered PDFs |
| 10 | SHA-1 is a Shambles (2020): forged PGP identity |
| 11 | Defenses & modern alternatives |
| 12 | Conclusions & references |

## Sources

- Microsoft MSRC, [Flame malware collision attack explained](https://www.microsoft.com/en-us/msrc/blog/2012/06/flame-malware-collision-attack-explained/) (2012)
- Google Security Blog, [Announcing the first SHA1 collision](https://security.googleblog.com/2017/02/announcing-first-sha1-collision.html) (2017)
- Stevens et al., [The First Collision for Full SHA-1](https://eprint.iacr.org/2017/190) (2017)
- Leurent & Peyrin, [SHA-1 is a Shambles](https://sha-mbles.github.io/), USENIX Security 2020
- NIST, [Policy on hash functions](https://csrc.nist.gov/projects/hash-functions/nist-policy-on-hash-functions) and [Transitioning away from SHA-1](https://www.nist.gov/news-events/news/2022/12/nist-transitioning-away-sha-1-all-applications)
- SHAttered PDF pair from [cr-marcstevens/sha1collisiondetection](https://github.com/cr-marcstevens/sha1collisiondetection/tree/master/test)
