# Nôm Na Việt (喃哪越)

> Free tools for Vietnamese Hán Nôm (漢喃) studies — dictionary, converter, OCR, input methods, and a classical text reader.

Hán Nôm is the logographic script Vietnamese was written in for roughly a thousand years. Almost nobody can read it today. We build the tools that make it approachable: look up a character you can't pronounce, turn a Vietnamese sentence into Chữ Nôm, photograph a woodblock page, type Nôm on a phone keyboard, or read Truyện Kiều with per-character annotations.

**→ [nomnaviet.com](https://nomnaviet.com)**

## What we build

| | |
|---|---|
| **Dictionary** | 46,000+ characters (19,000 of them in CJK Extension B) and 72,000+ compounds, including 30,000+ thành ngữ idioms. Search by character, Hán Việt reading, Vietnamese meaning, or semantics, with component and radical search for when you can only see the shape. Definitions are shown one dictionary at a time, in an order you choose: Tự Điển Chữ Nôm Dẫn Giải, Nguyễn Trãi Quốc Âm Từ Điển, Khang Hy Tự Điển (康熙字典, the Kangxi Zidian), Thuyết Văn Giải Tự (說文解字) and more. Readings in Mandarin, Cantonese, Japanese and Korean, and Middle Chinese phonology from Guangyun (廣韻). |
| **Converter** | Vietnamese ↔ Chữ Nôm in both directions. Việt → Nôm weighs each word's candidates against the rest of its line, using a model trained on the aligned Hán Nôm corpus. |
| **Reader** | 36 classical texts — 5 Truyện Kiều variant editions (1866–1902) with scholarly footnotes, Quốc Âm Thi Tập (15th century), Hồ Xuân Hương, Chinh Phụ Ngâm Khúc, Việt Nam Bách Gia Thi, Tam Quốc Chí Diễn Nghĩa, Catholic Nôm prayers — in stacked, side-by-side, or classical vertical layouts. |
| **Camera OCR** | Photograph a woodblock or manuscript page. 96.6% top-1 on real-world crops; rare Nôm characters reach 93.9% via style-transfer augmentation. |
| **Input methods** | Type Vietnamese in Telex, get Chữ Nôm — on the web, as a native iOS and Android **system keyboard** (works in any app), in Chrome, or through RIME on desktop. |
| **Learning** | Spaced-repetition flashcards over 3,990+ characters graded by level, with formation classifications explaining *how* each character was built. |
| **For AI assistants** | An [MCP server](https://nomnaviet.com/en/mcp) (`com.nomnaviet/han-nom` in the official registry) gives Claude and other clients character lookup, full dictionary entries, conversion, and corpus search, with every definition attributed to its source. In the app, Bé Na answers questions about Hán Nôm. |
| **Nommoji** | A Hán Nôm notes app: six calligraphic styles, classical vertical writing, and a built-in Telex → Nôm keyboard. [Coming to the App Store](https://nomnaviet.com/en/nommoji). |

Available on the web, iOS, and Android, in Vietnamese, English, French, and Traditional Chinese.

## Repositories

The platform itself is closed source and free to use. These are the parts that are open:

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

You can also correct OCR output on manuscript pages at [nomnaviet.com/contribute](https://nomnaviet.com/contribute).

If you read Hán Nôm and want to help in a bigger way — reviewing readings, digitizing a dictionary, checking OCR output — open a discussion or reach out.

## Built on the work of others

None of this exists without the scholars and institutions who did the hard part first:

- [**Vietnamese Nôm Preservation Foundation**](https://nomfoundation.org) · [**Digitizing Vietnam**](https://www.digitizingvietnam.com) **(Columbia University)** — Nôm character data, glyph variants, and historical citations (co-owned by VNPF & Columbia/DVN). VNPF also created the [NomNaTong](https://github.com/nomfoundation/font) typeface (MIT), which is why rare Extension B/C glyphs render here at all.
- ***Tự Điển Chữ Nôm Dẫn Giải*** — Nguyễn Quang Hồng, NXB Khoa học Xã hội (2014). Source of the A1–G2 formation classifications; digital edition mirrored via [Digitizing Vietnam](https://github.com/panda1835/digitizing-vietnam-website).
- ***Giúp Đọc Nôm và Hán Việt*** — LM. Anthony Trần Văn Kiệm, NXB Đà Nẵng (2004); digital edition mirrored via [Digitizing Vietnam](https://github.com/panda1835/digitizing-vietnam-website).
- ***Nguyễn Trãi Quốc Âm Từ Điển*** — Trần Trọng Dương; used by permission, digital text provided by [Digitizing Vietnam](https://www.digitizingvietnam.com).
- ***Khang Hy Tự Điển*** (康熙字典, 1716) — text digitised by [Simon Wiles](https://simonwiles.net/projects/kangxi-zidian/) (CC0), converted by [kangxiDictText](https://github.com/7468696e6b/kangxiDictText) (MIT).
- ***Thuyết Văn Giải Tự*** (說文解字, Hứa Thận) with Đoàn Ngọc Tài's commentary (說文解字注, 1815) — text digitised by [shuowen.org](https://github.com/shuowenjiezi/shuowen) (Apache-2.0).
- [**chinese-xinhua**](https://github.com/pwxcoo/chinese-xinhua) — idiom list and their sources (出處).
- [**ThiVien**](https://hvdic.thivien.net) — Hán Việt and Nôm readings.
- [**Unihan Database**](https://unicode.org/charts/unihan.html) — Unicode Consortium.
- [Vietnamese Wikisource](https://vi.wikisource.org/), [CC-CEDICT](https://cc-cedict.org/), [EDRDG](https://www.edrdg.org/), and [ctext.org](https://ctext.org/) for classical texts and cross-script readings.

Full attribution, including every bundled font and its designer: [nomnaviet.com/about](https://nomnaviet.com/en/about)
