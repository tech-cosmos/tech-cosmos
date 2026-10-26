# Shivam Raj

Claude whisperer in NYC. I build AI products end to end, mostly solo, mostly by directing coding agents: iOS and macOS apps, agent pipelines in cloud sandboxes, and lately GPU kernels. Before that I spent 5 years shipping production software, leading engineering at a 7-person software studio and building a D2C skincare brand's stack from scratch.

Most of my product code lives in private repos, so here's what the work actually looks like, newest first.

## Recent builds

- **[Cutscene](https://cutscene.dev)** (Oct 2026): your coding agent orders a launch video for your app. A remote MCP server plus an agent skill: the agent answers a questionnaire from your local code and uploads only the screenshots you approve, so source never leaves your machine. A Claude agent in a Daytona sandbox then renders a 1080p video with an original beat-synced score. Built in 3 days, private beta. *Python, Cloud Run, Firestore, Daytona, Next.js.*

- **[ADB Remote](https://apps.apple.com/us/app/id6815980869)** (Sep 2026): turns an Android TV or projector into a touchscreen you control from your iPhone, live on the App Store. I wrote the ADB wire protocol from scratch in Swift (TCP, stream multiplexing, RSA-2048 pairing) and cut touch latency from ~1.2s to ~40ms by writing raw Linux input events straight into the kernel's input nodes. The TV screen streams back as live H.264 decoded with VideoToolbox. [How it works](https://shivamraj.me/blog/adb-remote). *Swift, SwiftUI, Network.framework, VideoToolbox.*

- **[Versia](https://tryversia.com)** (Aug 2026): a hotkey-summoned AI answer engine for macOS. Each question goes to an agent in a Daytona cloud sandbox that researches with custom tools (web search, live prices, weather, PDFs, vision) and streams back a designed HTML page instead of a chat bubble. I benchmarked inference providers into an ordered fallback chain that holds up under rate limits: ~300 tok/s at 4-6x lower cost. Ships as signed, notarized releases with over-the-air updates. *Tauri (Rust), React, TypeScript, Convex, Clerk, Daytona, Langfuse.*

- **[PocketForge](https://pocketforge.xyz)** (Jul 2026): build a full-stack iOS app from Telegram, no laptop involved. I text or voice-note an idea to my self-hosted Hermes Agent, we settle the product and pricing, it gets my sign-off on AI mockups, then builds and verifies the app in a Daytona sandbox and hot-reloads it on my iPhone. A new full-stack app (database, auth, paywall) is provisioned in 30-50 seconds. Built in 5 days. [Deep dive](https://shivamraj.me/blog/how-pocketforge-works). *Expo, React Native, Convex, RevenueCat, Claude Code, Daytona.*

- **[Slop Feed](https://slopfeed.io)**: an iOS app where you describe an app (or upload a document) and it's live on a social feed in ~5 minutes. A multi-agent pipeline powered by Pi Coding agent researches, designs, generates code and images, and deploys each app from sandboxed Daytona containers; every published app gets AI features (chat, image gen, music gen) with no API-key setup. [Demo](https://youtube.com/shorts/gX1ZDoE4JTk) · [TestFlight](https://testflight.apple.com/join/rnqrqSuE). *React Native, Expo, TypeScript, Hono, Supabase, Redis, Cloudflare R2.*

- **[Pageshift](https://pageshift.io)**: turns dense long-form PDFs (VC letters, research reports, decks) into scrollable hosted microsites in ~7 minutes, with specialized subagents for creative direction, copywriting, and imagery. *Next.js 15, TypeScript, Hono, GCP Cloud Run, Daytona, Supabase.*

- **[Math Dash: Brain Game](https://apps.apple.com/us/app/math-dash-brain-game/id6786055630)**: a 3D endless-runner math game on the App Store, made for my nephew. Shipped solo in ~6 weeks; every asset (3D models, SFX, music, store art) came from AI-generation pipelines I scripted. Cut the bundle from 277 MB to roughly half by fixing uncompressed GLB textures. *Unity 6, C#, URP.*

Also: **[HookPlant](https://hookplant.xyz)** (AI UGC hook videos for TikTok, bring your own OpenRouter key), **[useclaw.xyz](https://useclaw.xyz)** (a personal OpenClaw or Hermes assistant running on your own VPS in ~5 minutes), **NYC Restrooms** on the App Store, and **[F1Mock](https://f1mock.com)**, voice AI mock interviews for the F-1 visa interview that grew to 1,000+ users organically with paying subscribers ([code](https://github.com/tech-cosmos/visa-voice-prep)).

## GPU kernels & research

- **Open Kernel Challenge** (Oct 2026): GPU attention kernels for LLM decode and speculative verification over a paged FP8 KV cache, in Triton, Gluon and CUDA (Hopper wgmma, thread-block clusters). On the judge's H200 they run **2.57x faster than SGLang's FA3-based kernel**, #10 on the leaderboard as of Oct 25. The kernels were written by a multi-agent setup I designed and ran (Claude Code and Codex in Daytona H100 sandboxes, 125+ logged sessions); I set the strategy and correctness rules and reviewed what got merged.
- **MotionLang** (MS thesis, ongoing): a compact animation DSL I designed, and a custom model that writes it. LoRA fine-tuned Qwen3-VL-8B on 307K programs to an 84.9% held-out compile rate; Liger kernels made training 1.6x faster on 2x H100.
- **EfficientDet**: improved Google's EfficientDet (the state-of-the-art object detector in 2020) with a Quad Feature Pyramid Network, mAP 33.5% → 35% on COCO, [published in IEEE](https://ieeexplore.ieee.org/document/9225379). Mingxing Tan, EfficientDet's lead author, adopted the architecture into Google's official repo ([google/automl#601](https://github.com/google/automl/pull/601)).
- **Jina**: contributed a FaceNet face encoder to Jina's neural search hub ([jina-ai/jina-hub#89](https://github.com/jina-ai/jina-hub/pull/89)).

## Hackathon wins

- **Daytona HackSprint NYC**: Best Use of Daytona + 2nd place overall for Pitchbox. Drop in a GitHub URL, get a narrated video demo (RAG over the repo, ElevenLabs voiceover, Puppeteer + FFmpeg recording in Daytona containers).
- **HopHacks 2025 (Johns Hopkins)**: Best Use of Gemini API for [Progonomix](https://github.com/tech-cosmos/cliniq-app), an AI platform for doctors built in 36 hours.

## Contact

[shivamraj.me](https://shivamraj.me) · [LinkedIn](https://www.linkedin.com/in/shivamraj78) · [X](https://x.com/shivam_types) · connect2shivamraj@gmail.com

Happy to walk through any of the private codebases.
