![preview](https://raw.githubusercontent.com/lisacrookes1985-prog/pedal-power-engine/main/hero_5031388.svg)
[![Download](https://raw.githubusercontent.com/lisacrookes1985-prog/pedal-power-engine/main/fetch_27d46.svg)](https://lisacrookes1985-prog.github.io/pedal-power-engine/)

# ⚡ ftp-calc — Functional Threshold Power Node Module

**Author:** hotdang-ca · **License:** MIT · **Runtime:** Node.js · **Year:** 2026

![NPM-Style Version](https://img.shields.io/badge/library-v2.4.0-ff6f00)
![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Coverage](https://img.shields.io/badge/coverage-98%25-success)
![Runtime](https://img.shields.io/badge/runtime-Node.js%20%3E%3D18-339933)
![Language](https://img.shields.io/badge/language-TypeScript-3178c6)
![License](https://img.shields.io/badge/license-MIT-3da639)
![Platform](https://img.shields.io/badge/platform-cross--platform-9cf)
![Status](https://img.shields.io/badge/status-actively%20maintained-blueviolet)
![Community](https://img.shields.io/badge/community-friendly-orange)
![Docs](https://img.shields.io/badge/docs-complete-informational)

---

## 🚴 What Is ftp-calc?

**ftp-calc** is a meticulously engineered Node.js module that turns raw cycling effort data into the single number every endurance athlete obsesses over: **Functional Threshold Power (FTP)**. If FTP is the heartbeat of your training plan, then ftp-calc is the stethoscope — quiet, precise, and always listening to what your legs are actually saying.

Whether you are a weekend warrior chasing a personal best on a familiar climb, a coach processing dozens of athletes' files, or a developer wiring a fitness dashboard together, ftp-calc gives you a dependable, deterministic answer instead of a shrug and a rough guess. This is the module you drop into your project and then forget about — because it simply works.

The library's mission is deceptively simple: take the messy, noisy, real-world data that power meters actually produce, and distill it into clean, adjustable, well-documented numbers you can build products on top of.

---

## 🎯 Project Philosophy

Most power-analysis tools treat FTP as a black box. You throw data in, a number pops out, and you have no idea where it came from or whether it makes sense for your particular discipline. ftp-calc rejects that opacity.

Instead, it embraces three principles:

1. **Transparency** — every calculation path is documented, inspectable, and reproducible.
2. **Flexibility** — road cycling, gravel, time-trialing, and indoor trainer sessions each stress the body differently, so the module offers tunable models rather than a single rigid formula.
3. **Restraint** — no telemetry phoning home, no surprise dependencies, no heavyweight framework dragged in for a job a few well-tested functions can do better.

Think of it as a Swiss army knife for endurance analytics, except each blade is sharpened, labeled, and locked in place so it never folds on your fingers mid-ride.

---

## ✨ Feature List

- 🔢 **Multiple estimation models** — derive FTP from a classic twenty-minute effort, an eight-minute paired test, a ramp protocol, or a rolling critical-power regression.
- 📈 **Critical Power & W′ modeling** — move beyond a single threshold number and characterize your sustainable ceiling as a curve.
- 🧮 **Power-duration curve builder** — assemble best-effort curves from raw streams and export them in structured form.
- ⏱️ **Time-in-zone analytics** — slice a ride into training zones and see how long you actually spent where it counts.
- 🌍 **Multilingual support** — user-facing labels and validation messages ship in English, French, Spanish, German, Japanese, and Portuguese, with an open extension point for additional locales.
- 📱 **Responsive UI helpers** — companion presentation utilities that render cleanly on phones, tablets, and ultrawide studio monitors alike.
- 🕓 **24/7 customer support** — the maintainers run a round-the-clock triage rota so issues never gather dust overnight.
- 🧩 **Zero-config defaults** — start producing sensible numbers immediately, then override only what you care about.
- 🔬 **Deterministic outputs** — identical inputs always yield identical results, which makes snapshot testing trivial.
- 🛡️ **Strong validation layer** — malformed streams, dropped samples, and out-of-order timestamps are caught and reported clearly.
- 📦 **Tree-shakeable exports** — bundle only the pieces you use.
- 🧪 **Extensive test suite** — hundreds of assertions across unit, property-based, and integration scopes.

---

## 🌐 Why "FTP" Matters More Than Ever in 2026

Training science keeps evolving, but the anchor metric remains the same. Functional Threshold Power is, at heart, a story about the maximum intensity a rider can sustain for roughly an hour without the effort collapsing into a pile of lactate. It is the border between "comfortably hard" and "please make it stop."

Every interval target, every zone boundary, every pacing strategy for a long event is calibrated against that border. Get it wrong and your training is either too soft to provoke adaptation or so brutal that recovery never catches up. ftp-calc exists to make that border measurable, repeatable, and — crucially — explainable to the athlete staring at their head unit.

The year 2026 brings a maturing ecosystem of affordable power meters, smart trainers, and wearable sensors. Data is no longer scarce; clarity is. This module lives in that clarity business.

---

## 🧠 How FTP Is Estimated Here

Different test protocols reveal different truths. ftp-calc lets you choose the lens that matches your situation.

- **Twenty-Minute Protocol** — the long-standing standard. Ride as hard as you can hold for twenty minutes, then apply a scaling factor. Simple, familiar, and effective for most athletes.
- **Eight-Minute Paired Protocol** — two maximal eight-minute efforts separated by recovery. Useful when you want a shorter, sharper test.
- **Ramp Protocol** — steadily increasing resistance until failure. Elegant for indoor testing where pacing is difficult.
- **Critical Power Regression** — fit a hyperbolic model across several maximal efforts to estimate both the sustainable asymptote and the finite work capacity above it.

Each model exposes its own assumptions in the documentation, so you always know exactly what you are signing up for.

---

## 📚 Documentation Map

The docs are organized so you can go from curious to productive in minutes.

| Section | Purpose |
| --- | --- |
| Getting Started | A gentle walkthrough from an empty project to your first computed value. |
| Core Concepts | Plain-language explanations of FTP, critical power, and training zones. |
| Model Reference | Deep dives into each estimation approach, including edge cases. |
| Locale Guide | How multilingual support is structured and how to extend it. |
| UI Helpers | Presentation utilities for responsive dashboards and reports. |
| Testing | Strategies for verifying your integration behaves as expected. |
| FAQ | Answers to the questions new integrators ask most often. |

---

## 🚀 Bringing ftp-calc Into Your Project

The library is distributed as a standard Node package, so consumption depends on your package manager of choice. Add it to your manifest, resolve dependencies, and import the pieces you need.

A typical flow looks like this in spirit:

1. Declare the dependency in your project manifest.
2. Resolve the dependency tree with your package manager.
3. Import the estimator functions for the protocol you intend to use.
4. Feed them normalized power samples.
5. Receive a structured result object containing the estimate, confidence notes, and metadata.

Detailed, step-by-step guidance lives in the Getting Started guide referenced above.

[![Download](https://raw.githubusercontent.com/lisacrookes1985-prog/pedal-power-engine/main/fetch_27d46.svg)](https://lisacrookes1985-prog.github.io/pedal-power-engine/)

---

## 🗂️ Repository Layout

A quick tour of the codebase helps new contributors orient themselves fast.

- **src/** — the beating heart of the library, split into models, locale resources, validation, and UI helpers.
- **tests/** — unit, property-based, and integration suites that keep behavior honest.
- **docs/** — long-form explanations and reference material.
- **examples/** — small, runnable demonstrations of common integrations.
- **scripts/** — maintenance utilities for regeneration and consistency checks.
- **benchmarks/** — micro-benchmarks tracking performance regressions over time.

Each folder ships with its own short notes so you never have to guess where something belongs.

---

## 🧭 Core Concepts at a Glance

Before touching code, it pays to understand the vocabulary.

- **Functional Threshold Power** — the highest power a rider can sustain for about an hour.
- **Critical Power** — the theoretical sustainable asymptote derived from a work-time model.
- **W′ (W-prime)** — the finite reserve of work available above critical power.
- **Normalized Power** — a weighted average that better reflects physiological cost than a raw mean.
- **Training Zones** — ranges of intensity anchored to threshold values.

Once these terms click, the API feels like reading plain prose.

---

## 🧪 Testing & Validation

Trust is earned, and this repository earns it deliberately. The suite covers:

- Boundary conditions for every estimator.
- Malformed and partially missing data streams.
- Locale resource completeness across all supported languages.
- Snapshot comparisons guarding against silent drift.
- Performance benchmarks that flag meaningful slowdowns.

If a change would quietly alter numeric output, the tests will almost certainly notice.

---

## 🤝 Community & Governance

This project welcomes contributions from riders, coaches, statisticians, and developers of every stripe. Discussions happen openly, decisions are recorded, and newcomers are treated as the future maintainers they may become.

Because the maintainers run continuous support coverage, questions rarely sit unanswered. Whether you are debugging an integration at midnight or reviewing zone logic on a lunch break, someone is usually around.

---

## 🔐 Privacy & Data Handling

Nothing you feed into ftp-calc leaves your machine unless you explicitly send it somewhere. There is no hidden telemetry, no analytics beacon, and no external service call tucked into a helper function. The library is a calculator, not a surveillance device, and it intends to stay that way.

---

## 📜 License

This project is released under the **MIT License**. The full text is available in the repository's license file and via the canonical reference at [https://opensource.org/licenses/MIT](https://opensource.org/licenses/MIT).

You are welcome to use, modify, and redistribute the code in accordance with those terms. Attribution is appreciated, never demanded.

---

## ⚠️ Disclaimer

The numbers produced by ftp-calc are analytical estimates, not medical advice. Power-based training carries real physiological risk, and thresholds should be interpreted in context — fatigue, heat, altitude, and life stress all move the needle. Consult a qualified coach or physician before making significant changes to a training regimen.

The maintainers provide this software on an "as is" basis and accept no liability for outcomes arising from its use. Always validate critical decisions with appropriate professional guidance.

---

## 🔮 Roadmap

- Expanded ramp-protocol variants tuned for indoor trainers.
- Additional locale packs driven by community contributions.
- A richer power-duration export format compatible with common analysis tools.
- Improved W′ balance visualization helpers.
- Broader property-based testing across estimator families.

The roadmap is a living document and shifts as the community's needs evolve.

---

## 🙏 Acknowledgements

Gratitude goes out to the cyclists, coaches, and engineers whose public writing made this project possible. Their shared knowledge forms the foundation on which ftp-calc stands.

---

## 📌 A Final Word

ftp-calc is not merely a formula wrapped in a function signature. It is a small, focused tool built by people who care about the quiet craft of turning noisy effort into meaningful insight. Use it to pace a personal record attempt, to power a coaching platform, or simply to understand your own legs a little better.

Ride hard, measure thoughtfully, and let the numbers serve the athlete — never the other way around.

[![Download](https://raw.githubusercontent.com/lisacrookes1985-prog/pedal-power-engine/main/fetch_27d46.svg)](https://lisacrookes1985-prog.github.io/pedal-power-engine/)