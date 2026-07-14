# Shivam Raj

Founder-engineer in NYC. I build AI products end to end and ship them: five live products in the past 12 months, all built solo. Before that I co-founded a dev studio (grew it to 7 people) and was the founding engineer at a D2C skincare brand.

Most of my product code lives in private repos, so here's what the work actually looks like.

## Live products

- **[Next Stop](https://nextstop.homes)** — housing aggregator for international students moving to NYC/NJ. Ingests listings from closed WhatsApp and Facebook groups (a Manifest V3 Chrome extension intercepts Facebook's GraphQL responses instead of scraping the DOM), structures them with delta-cached LLM extraction, and kills cross-posted duplicates with media hashing + fuzzy matching. ~2,500 structured listings. *Next.js 16, React 19, Convex, Python, Claude.*

- **[Slop Feed](https://slopfeed.io)** — describe an app in plain English and it's live on a social feed in ~5 minutes. A multi-agent system (built on the Pi Coding agent) plans, generates, and deploys each app in sandboxed Daytona containers; every published app gets AI features (chat, image gen, music gen) with no API-key setup. iOS beta on [TestFlight](https://testflight.apple.com/join/rnqrqSuE). *React Native, Expo, TypeScript, Hono, Supabase, Redis, Cloudflare R2.*

- **[Pageshift](https://pageshift.io)** — turns dense long-form PDFs (VC letters, research reports, decks) into scrollable hosted microsites in ~7 minutes, with an agent-based generation pipeline: specialized subagents for creative direction, copywriting, and imagery. *Next.js 15, TypeScript, Hono, GCP Cloud Run, Daytona, Supabase.*

- **[Math Dash: Brain Game](https://apps.apple.com/us/app/math-dash-brain-game/id6786055630)** — 3D endless-runner math game, live on the App Store. Shipped solo in ~6 weeks; every asset (3D models, SFX, music, store art) came from AI-generation pipelines I scripted (Tripo, ElevenLabs, Suno). Cut the bundle from 277 MB to roughly half by fixing uncompressed GLB textures. *Unity 6, C#, URP.*

- **[F1Mock](https://f1mock.com)** — real-time voice AI mock interviews for the U.S. F-1 visa interview, with sub-300ms voice latency. 1,000+ users acquired organically, paying subscribers at $10/month. Code is public: [visa-voice-prep](https://github.com/tech-cosmos/visa-voice-prep). *Next.js, Pipecat, Deepgram, GCP Cloud Run.*

Also: **[useclaw.xyz](https://useclaw.xyz)** — deploy an OpenClaw or Hermes personal assistant onto a Hetzner VPS, bot running in ~5 minutes.

## Open source & research

- Improved Google's **EfficientDet** (the state-of-the-art object detector in 2020) with a Quad Feature Pyramid Network: mAP 33.5% → 35% on COCO, [published in IEEE](https://ieeexplore.ieee.org/document/9225379), and the code was merged into Google's official EfficientDet repo.
- 2 PRs merged into [jina-ai/jina](https://github.com/jina-ai/jina): face indexing and search for their neural search framework.

## Hackathon wins

- **Daytona HackSprint NYC** — Best Use of Daytona + 2nd place overall for Pitchbox: drop a GitHub URL, get a narrated video demo (RAG over the repo, ElevenLabs voiceover, Puppeteer + FFmpeg recording in Daytona containers).
- **HopHacks 2025 (Johns Hopkins)** — Best Use of Gemini API for [Progonomix](https://github.com/tech-cosmos/cliniq-app), an AI platform for doctors built in 36 hours.

## Contact

[shivamraj.me](https://shivamraj.me) · [LinkedIn](https://www.linkedin.com/in/shivamraj78) · [X](https://x.com/shivam_types) · connect2shivamraj2024@gmail.com

Happy to walk through any of the private codebases.
