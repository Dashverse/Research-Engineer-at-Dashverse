# 🧪 Join Dashverse Research

**Build the Future of Generative Content Creation**

Welcome to **Dashverse** — where we don't just use generative AI… we **push it to its limits**.

Backed by Z47, PeakXV, and Stellaris, we're a small team building powerful creation tools for the next generation of storytellers. Our products — like **[Frameo.ai](https://frameo.ai/create)** and **[Dashtoon Studio](https://studio.dashtoon.ai/)** — let creators instantly turn ideas into viral videos, comics, and more using AI. If you're someone who thrives on deep technical problems *and* wants to see your work used by millions — this is your playground.

## 🧠 The Role: Research Engineer

This isn't your average research gig.

You're not here to write papers and wait six months for reviews. You're here to:

* Prototype bleeding-edge generative models
* Ship tools that change how stories are made
* Build the infra and internal tools to move 10x faster

## 🧩 What We're Solving

We’re not here to slap LoRA on a checkpoint and call it innovation. We’re building real tools for real creators — and that means diving deep into unsolved problems at the frontier of generative media.

Here are just a few areas we’re actively working on:

### 🎨 Supercharging Visual Quality with Diffusion

Diffusion models are powerful — but not always pretty out of the box. Whether it's a single comic panel or 120 frames of an AI-generated video, quality matters — and we're obsessed with pushing it further.

### 🎛 Controllability is King

We're building **creative tools**, not black boxes. That means giving creators the ability to *steer* generations in meaningful ways:

* Text + image **multi-modal prompts**
* Conditioning on **pose**, **expression**, **scene layout**, and **panel structure**
* Temporal control for **frame-to-frame consistency** in videos
* Spatial control for **region-specific edits**

We’re constantly exploring new ways to inject structure and intent into the chaos of generative noise.

### 🧑‍🎤 Identity Matters

Characters aren’t just faces — they’re brands. We're developing pipelines for:

* **ID-consistent inpainting** to fix or change parts of a character without losing identity
* **Low-data personalization** (e.g., custom LoRA without fine-tuning)
* Seamless **multi-angle rendering** of the same character across scenes or panels

For tools like *Dashtoon Studio*, this means creators can design a character once and use it across dozens of scenes without needing to redraw or re-prompt.

### 🧥 Scene-Aware Object & Clothing Transfer

We’re building tools that let creators swap a character’s outfit, pose, or even **scene props** without breaking the art style or spatial integrity.

This includes:

* **Semantic segmentation** + feature-level transfer
* Training-free pipelines using **adapter stacking**
* Support for both photoreal and stylized (anime/comic) domains

Imagine changing a character from a lab coat to battle armor — with one click.

### 🔄 Training-Free Customization & Distillation

We’re exploring fast, lightweight ways to personalize and adapt models **without full retraining**:

* Tuning-free **ID adapters** and **style injectors**
* **LoRA + ControlNet combos** with zero additional training
* Fast model distillation for **mobile inference** and low-latency previews

This unlocks real-time use in creator tools, where speed and flexibility are non-negotiable.

If any of this sparks ideas for you — dive into one of our sample problems, or just fork the repo and show us what you’d build differently.

We're excited to see what *you* can create with the right canvas. You’ll own entire flows — from training scripts to serving infra to UI playgrounds. And if you see something slowing you down? You’ll build the tool to fix it.

## 🧬 What You’ll Work On

Some recent open-source drops from our team:

* 🎞 [Keyframe LoRA: Video generation using only keyframes](https://insiders.dashtoon.com/introducing-hunyuan-keyframe-lora-open-source-keyframe-based-video-generation/)
* 🧑‍🎨 [Tuning-free ID-consistent inpainting](https://insiders.dashtoon.com/a-road-towards-tuning-free-id-consistent-character-inpainting/)
* 👗 [DashTailor: Object transfer for AI-generated comics](https://insiders.dashtoon.com/dashtailor-training-free-clothing-and-object-transfer-for-ai-comics/)
* 🌀 [Adversarial Diffusion Distillation](https://insiders.dashtoon.com/exploring-the-future-of-comic-generation-insights-from-our-adversarial-diffusion-distillation-poc/)
* ✨ [DashAnimeXL: Stylized diffusion for comic-style animations](https://insiders.dashtoon.com/dashanimexl/)

If any of these excite you, try one of the sample problems. Blow us away.

## 🧪 Who We’re Looking For

We don’t care about your degree, resume, or pedigree. We care about what you’ve **built**, **trained**, or **broken and fixed**.

You might be a great fit if you:

* Have trained/fine-tuned models like **Stable Diffusion**, **AnimateDiff**, or **StyleGAN**
* Are comfortable with **PyTorch**, **LoRA**, **ControlNet**, **DreamBooth**, or **IP-Adapters**
* Can wrangle multi-GPU training jobs, inference optimization, and debugging fast
* Like to move fast and own the full stack from training → UI

Bonus if:

* You’ve written clean infra or internal tools before
* You’ve contributed to open-source or have a killer side project
* You’ve got opinions on how generative models should evolve

## 🛠 How to Apply

* Clone this repo.
* Try one of the sample problems (or fork it and show us something better).
* Then drop us a line: **[soumyadeep@dashtoon.com](mailto:soumyadeep@dashtoon.com)**

No leetcode. Just real problems and real builders.

If you're the kind of person who wants to go **own the entire stack** — owning fine-tuning, infra, and everything in between — come build with us.

**Dashverse — Dream it. Generate it. Share it.**
