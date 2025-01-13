# Runway Stable Diffusion v1.5

## Overview

This repository contains the model **Runway Stable Diffusion v1.5** used for generating creative images from text prompts. Stable Diffusion is a latent text-to-image diffusion model capable of generating high-quality images based on descriptive text input. This version is fine-tuned to allow for rapid creative image generation with a wide variety of applications.

## Features

- **High-Quality Image Generation**: Produces creative and high-quality images from text prompts.
- **Real-time Results**: Generates images quickly, suitable for creative applications.
- **Versatile**: Works with a wide variety of prompts ranging from abstract art to realistic depictions.

## Installation

Runway Stable Diffusion can be run easily in Google Colab or in your local environment with the following requirements:

### Prerequisites

- **Google Colab (Recommended)**: The model can run with GPU acceleration in Google Colab.
- **Hugging Face Account**: Some models require authentication for access. You can create an account and generate an API token [here](https://huggingface.co/settings/tokens).

### Setup in Google Colab

1. **Open Google Colab** and create a new notebook.
2. **Install required libraries** using the following code:
    ```python
    !pip install diffusers transformers accelerate torch torchvision pillow
    ```

3. **Load the model** and generate images:

    ```python
    from diffusers import StableDiffusionPipeline

    # Load the model from Hugging Face
    model_id = "runwayml/stable-diffusion-v1-5"
    pipe = StableDiffusionPipeline.from_pretrained(model_id)

    # Example prompt
    prompt = "A futuristic city with neon lights at night"

    # Generate image
    image = pipe(prompt).images[0]
    image.show()
    ```

### Example Usage

Generate images from text using this model with custom prompts:

```python
prompt = "A serene beach at sunset"
image = pipe(prompt).images[0]
image.show()
