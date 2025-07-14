# Who’s That Character?

Build a scalable, modular pipeline to extract clean, structured metadata from a noisy, large-scale dataset of character images or textual descriptions.

This is not a toy problem. Imagine dealing with millions of inconsistently labeled character entries, and needing to create a foundational layer for training our next-generation character generation models. If the pipeline breaks at 5 million samples — it doesn’t work.

## Dataset Realities

You will be working with large-scale datasets that may include:

- Character images in various art styles and qualities.
- Textual descriptions of characters, ranging from concise tags to full prompts.
- Real-world inconsistencies, such as:
  - Missing or conflicting attribute data.
  - Multiple characters in a single image.
  - Noisy or ambiguous tags (e.g., “cool” as both mood and fashion).

Start with this open dataset:  
https://huggingface.co/datasets/cagliostrolab/860k-ordered-tags

You may use additional sources — but assume that the final goal is to scale to approximately 5 million entries.

## The Goal

Extract the following structured attributes for each character (from an image or description):

- Age (child, teen, young adult, middle-aged, elderly).
- Gender (male, female, non-binary).
- Ethnicity (Asian, African, Caucasian, etc.).
- Hair Style (ponytail, curly, bun, etc.).
- Hair Color (black, blonde, red, etc.).
- Hair Length (short, medium, long).
- Eye Color (brown, blue, green, etc.).
- Body Type (slim, muscular, curvy, etc.).
- Dress (casual, traditional, formal, etc.).
- Optional: facial expression, accessories, scars, tattoos, etc.

### Edge Case Handling

If an image contains multiple characters, you may skip it or flag it as ambiguous. Focus on clean, single-character extractions.

## Output Format

Return each character's attributes in a clean, machine-readable format:

```json
{
  "Age": "Young Adult",
  "Gender": "Female",
  "Ethnicity": "Asian",
  "Hair Style": "Ponytail",
  "Hair Color": "Black",
  "Hair Length": "Long",
  "Eye Color": "Brown",
  "Body Type": "Slim",
  "Dress": "Green Yukata"
}
````

This format will be used to train generative models conditioned on structured character attributes.

## Deliverables

Please submit **one** of the following:

### Option 1: Gradio App

Upload an image and view extracted attributes through an interactive UI.

### Option 2: Jupyter Notebook

Demonstrate the pipeline using sample inputs with visualizations and outputs.

Both versions should include:

* The core pipeline code.
* A working demo with 10–50 sample records.
* A brief explanation of how your pipeline will scale to 5 million samples.

## Evaluation Criteria

This task is not about building a perfect classifier. We are looking for a robust, scalable pipeline that:

### Scales Effectively

* Uses batching, caching, streaming, or parallelization where necessary.
* Handles partial failure or corrupted input gracefully.
* Avoids excessive RAM or GPU usage.

### Is Modular and Maintainable

* Easy to extend with new attributes or models.
* Cleanly separates logic across pipeline stages.
* Offers a clear interface for downstream integration and training.

### Maintains Accuracy and Consistency

* Adheres to the expected schema.
* Produces consistent outputs across different styles and datasets.

## Bonus Points

* Preprocessing for style normalization or occlusion handling.
* Heuristics for ambiguous cases or noisy data.
* Clustering logic to deduplicate near-duplicate entries.
* Use of distributed computing frameworks (Ray, Dask, Apache Beam).
* Dockerized or cloud-deployable implementations.

## Suggested Architecture

This is an open-ended task. However, here are some suggestions to guide your design:

### 1. Modular Design

Break the pipeline into testable stages:

```
[Input Loader] → [Preprocessing] → [Attribute Extractor] → [Validation] → [Exporter]
```

Each stage should be swappable or upgradable.

### 2. Model Choices

You can experiment with:

* **Image Embedding + Classifier**: Use CLIP, BLIP, or DINOv2 to extract embeddings. Train lightweight classifiers per attribute.
* **Text-to-Tag Parsers**: Use LLMs like LLaMA3 or Claude to extract attributes from unstructured text.
* **Vision-Language Models**: BLIP2, Kosmos, etc., for captioning and tag extraction.
* **Zero-shot Methods**: Use zero-shot classification with similarity scores; optionally fine-tune LoRA heads.

### 3. Large-Scale Processing

To handle millions of samples, consider:

* PyTorch Datasets or HuggingFace `datasets.map()` for batch inference.
* Ray, Dask, or multiprocessing for parallelism.
* Caching intermediate outputs (e.g., embeddings) via Redis, SQLite, or Parquet.

### 4. Deployment (Optional)

For portability and collaboration:

* Use Gradio or Streamlit for demos.
* FastAPI + Celery for endpoint + job queuing.
* Docker to encapsulate the environment.

### 5. Output Storage

Store results in accessible formats:

* JSONL, CSV, or SQLite/Postgres.
* Include schema definitions or manifests for compatibility.
* Optionally group outputs by dataset or image ID.

### 6. Preprocessing & Cleaning

Clean data before feeding it into models:

* Use detectors (YOLO, SAM) to skip multi-person or low-quality images.
* Normalize inputs for lighting, aspect ratio, and noise.
* OCR or VLM-based filtering for mismatches.
* Visual clustering for character-level deduplication.

## Tech Stack Overview

```plaintext
Data: HuggingFace Datasets, Custom Scrapers
Model: CLIP + Classifier | BLIP2 | OpenCLIP + LoRA
Infra: Python, PyTorch, Ray
Storage: JSONL / Parquet / SQLite
Deployment (optional): Docker, FastAPI, Gradio
```

Build what works — just ensure it scales, fails gracefully, and leaves room for growth.

If you’d like to discuss your ideas or approach, feel free to reach out.
**soumyadeep \[at] dashtoon.com**
