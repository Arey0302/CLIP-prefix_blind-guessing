# CLIP-Prefix for Image Captioning and an Experiment on Blind Image Guessing 👁️📜🖋️

Image caption generation resides at the intersection of computer vision and natural language processing, with its primary goal being the creation of descriptive and coherent textual narratives that faithfully depict the content of an image. 

We presents two models that leverage CLIP as the image encoder and fine-tune GPT-2 for caption generation on the Flickr30k and Flickr8k datasets. The first model utilizes a straightforward mapping network and outperforms the original architecture. The second model constitutes a new architecture exploring the boundaries of minimal visual information required for captioning. It incorporates CLIP's text encoder to produce input for the generator, while the image embedding serves solely as a validation mechanism. Despite its relatively lower performance, this model demonstrates the decoder's ability to create captions based on keyword descriptions alone, without direct access to the context vector.

_Full report temporarily unavailable_ ⏱️

## Dataset

We use the [Flickr8k](https://www.kaggle.com/datasets/adityajn105/flickr8k) and [Flickr30k](https://www.kaggle.com/datasets/eeshawn/flickr30k) dataset

## Evaluation

We use 6 metrics: Bleu-1 to 4, Meteor and Rouge

_Full results temporarily unavailable_

## Inference

Run our demo on Colab:
* [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1l7yHUMrhL_6JF_2_VQcvjHltLCEKy5ZH?usp=sharing) CLIP-prefix
* [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/19zLqmFVkE5kxbHJbyY62ZxJqjg6EcMGX?usp=sharing) SBG

The model weights are published on Huggingface:
* <a> <img src="https://workable-application-form.s3.amazonaws.com/advanced/production/61557f91d9510741dc62e7f8/c3635b59-a3d2-444a-b636-a9d0061dcdde" style="height: 1em;"></a> [CLIP-prefix](https://huggingface.co/Anshler/clip-prefix) _(gradient clipping flickr8k)_
* <a> <img src="https://workable-application-form.s3.amazonaws.com/advanced/production/61557f91d9510741dc62e7f8/c3635b59-a3d2-444a-b636-a9d0061dcdde" style="height: 1em;"></a> [SBG](Anshler/selective-blind-guessing) _(flickr8k)_

We also create a _[Stable diffusion WebUI](https://github.com/AUTOMATIC1111/stable-diffusion-webui) extension_ to interact with our models (_Clip-prefix gradient8k & SBG 8k_) locally. Load from this [repo](https://github.com/Anshler/ICG_sd_extension)
