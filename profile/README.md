# Nôm Na Việt (喃哪越)

> Open tools for Vietnamese Hán Nôm (漢喃) studies — dictionary, OCR, input methods, and a classical text reader.

Hán Nôm is the logographic script Vietnamese was written in for roughly a thousand years. Almost nobody can read it today. We build the tools that make it approachable: look up a character you can't pronounce, photograph a woodblock page, type Nôm on a phone keyboard, or read Truyện Kiều with per-character annotations.

**→ [nomnaviet.com](https://nomnaviet.com)**

## What we build

| | |
|---|---|
| **Dictionary** | Search by character, Hán Việt reading, Vietnamese meaning, or semantics. Component and radical search for when you can only see the shape. 45,000+ compounds, readings in Mandarin, Cantonese, Japanese and Korean, Middle Chinese phonology from Guangyun (廣韻). |
| **Reader** | 31 classical texts — 5 Truyện Kiều variant editions (1866–1902) with scholarly footnotes, Hồ Xuân Hương, Chinh Phụ Ngâm Khúc, Tam Quốc Chí Diễn Nghĩa, Catholic Nôm prayers — in stacked, side-by-side, or classical vertical layouts. |
| **Camera OCR** | Photograph a woodblock or manuscript page. 96.6% top-1 on real-world crops; rare Nôm characters reach 93.9% via style-transfer augmentation. |
| **Input methods** | Type Vietnamese in Telex, get Chữ Nôm — on the web, as a native iOS and Android **system keyboard** (works in any app), in Chrome, or through RIME on desktop. |
| **Learning** | Spaced-repetition flashcards over 3,990+ characters graded by level, with formation classifications explaining *how* each character was built. |

Available on the web, iOS, and Android, in Vietnamese, English, French, and Traditional Chinese.

## Repositories

| Repo | What it is |
|---|---|
| [**nomnaviet-contrib**](https://github.com/nomnaviet/nomnaviet-contrib) | Community character data and translations. Plain JSON and CSV — no build step, edit in the browser. |
| [**rime-nom-viet**](https://github.com/nomnaviet/rime-nom-viet) | RIME input schema for Chữ Nôm. 100,000+ entries including 46,000 compounds. macOS, Windows, Linux, iOS, Android. |
| [**make-me-a-chunom**](https://github.com/nomnaviet/make-me-a-chunom) | Stroke order editor for Chữ Nôm, including CJK Extension B/C/D. Fork of [make-me-a-hanzi](https://github.com/skishore/makemeahanzi). |

## Contributing

The most useful thing you can do needs no code at all. Two datasets have large, well-defined gaps:

- **Character formation classifications** — ~18,000 of 25,827 characters are still unclassified. Each one is a single letter-number code from a decision tree.
- **Dị thể (異體字) variant pairs** — same Vietnamese word, different Unicode codepoint. Coverage for pure-Nôm characters sits at 2.3%, because Unihan is Sinophone-centric and simply doesn't record them.

Both live in [nomnaviet-contrib](https://github.com/nomnaviet/nomnaviet-contrib) as flat files you can edit from the GitHub web UI. Translations into Vietnamese, English, French and Chinese are welcome there too.

If you read Hán Nôm and want to help in a bigger way — reviewing readings, digitizing a dictionary, checking OCR output — open a discussion or reach out.

## Built on the work of others

Our data stands on [Nomfoundation.org](https://nomfoundation.org/), [ThiVien](https://hvdic.thivien.net/), the Unicode [Unihan Database](https://unicode.org/charts/unihan.html), Nguyễn Quang Hồng's *Tự Điển Chữ Nôm Dẫn Giải* (NXB Khoa học Xã hội, 2014), [Vietnamese Wikisource](https://vi.wikisource.org/), [CC-CEDICT](https://cc-cedict.org/), and [EDRDG](https://www.edrdg.org/). Thank you.
