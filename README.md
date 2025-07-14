# Join Dashverse Research

**Build the Future of Generative Content Creation**

Welcome to **Dashverse** — where we don't just use generative AI, we push it to its limits.

We are a small, fast-moving team building powerful tools for the next generation of storytellers. Our products — like [Frameo.ai](https://frameo.ai/create) and [Dashtoon Studio](https://studio.dashtoon.ai/) — enable creators to instantly turn ideas into high-quality videos, comics, and more using AI. If you're someone who thrives on solving deep technical problems and wants to see your work used by millions, this is your playground.

## The Role: Research Engineer

This isn't your average research role.

At Dashverse, your work directly impacts creators. You’ll get to see the delight on a user's face when a tool you've built helps them bring their imagination to life — in seconds, not hours. This is a rare opportunity to move fast and shape the future of generative media.

You're not here to write papers and wait six months for reviews. You're here to:
- Prototype bleeding-edge generative models.
- Ship tools that change how stories are made.
- Build the infra and internal tools to move 10x faster.

## What We're Solving

We’re building real tools for real creators — and that means diving deep into unsolved problems at the frontier of generative media.

### Advancing Visual Quality with Diffusion

Diffusion models are powerful, but raw outputs often fall short. Whether it's a single comic panel or 120 frames of an AI-generated video, visual quality matters. We're focused on pushing fidelity, coherence, and artistic control to new heights.

### Controllability at the Core

We're developing **creative tools**, not black boxes. That means giving creators meaningful control over outputs:
- Text + image multi-modal prompts.
- Conditioning on pose, expression, scene layout, and panel structure.
- Temporal control for frame-to-frame consistency in videos.
- Spatial control for region-specific edits.

### Character Identity & Reusability

Characters aren't just faces — they're consistent, recognizable identities. We're building:
- ID-consistent inpainting to fix or change parts of a character without losing fidelity.
- Low-data personalization methods (e.g., style or identity adapters).
- Seamless multi-angle rendering of the same character across scenes or panels.

This enables creators to design once and reuse intelligently — with style and consistency.

### Scene-Aware Object & Clothing Transfer

We're building pipelines to enable asset-level swaps (outfits, props, etc.) while preserving visual integrity and scene coherence.

Key techniques include:
- Semantic segmentation with feature-level transfer.
- Training-free approaches using adapter stacking.
- Support for both photoreal and stylized (anime, comic) domains.

### Training-Free Customization & Distillation

We're exploring fast, lightweight personalization methods that don’t require full retraining:
- Tuning-free ID adapters and style injectors.
- LoRA + ControlNet workflows with zero additional training.
- Fast model distillation for mobile inference and real-time generation.

These innovations unlock high-speed, high-fidelity use in production creator tools.

If any of this sparks ideas, feel free to explore one of our sample problems — or fork the repo and show us what you’d build differently.

## What You’ll Work On

Here are a few recent open-source drops from our team:
- [Keyframe LoRA: Video generation using only keyframes](https://insiders.dashtoon.com/introducing-hunyuan-keyframe-lora-open-source-keyframe-based-video-generation/)
- [Tuning-free ID-consistent inpainting](https://insiders.dashtoon.com/a-road-towards-tuning-free-id-consistent-character-inpainting/)
- [DashTailor: Object transfer for AI-generated comics](https://insiders.dashtoon.com/dashtailor-training-free-clothing-and-object-transfer-for-ai-comics/)
- [Adversarial Diffusion Distillation](https://insiders.dashtoon.com/exploring-the-future-of-comic-generation-insights-from-our-adversarial-diffusion-distillation-poc/)
- [DashAnimeXL: Stylized diffusion for comic-style animations](https://insiders.dashtoon.com/dashanimexl/)

## Who We’re Looking For

We don’t care about your resume or degree. We care about what you’ve built, trained, or broken and fixed.

You might be a good fit if you:
- Have trained or fine-tuned models like Stable Diffusion, AnimateDiff, or StyleGAN.
- Are comfortable with PyTorch, LoRA, ControlNet, DreamBooth, or IP-Adapters.
- Can manage multi-GPU training jobs, optimize inference, and debug issues fast.
- Prefer to move quickly and own the entire stack from training to UI.

Bonus if you:
- Have written clean infra or tooling that helped teams scale.
- Have contributed to open-source or built an impressive side project.
- Have a strong perspective on how generative models should evolve.

## Perks

- Dedicated compute access with high-end GPUs.
- Fixed-band compensation based on submission quality.
- End-to-end ownership: from research to production to user experience.

## How to Apply

- Clone this repo.
- Attempt one of the sample problems — or fork it and show us something better.
- Email your submission or proposal to: **soumyadeep [at] dashtoon.com**

No Leetcode. Just real problems and real builders.

If you're the kind of person who wants to own the full stack — from fine-tuning to infra to user-facing tools — come build with us.

**Dashverse — Dream it. Generate it. Share it.**
