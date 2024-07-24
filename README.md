# Awesome-Video-Multi-modal Large Language Models
> A curated list of Video Multimodal Large Language Models. 

<!-- ## About Me: 
I'm an incoming Ph.D. student at the University of California San Diego. I received my M.S.E in Computer Science at Johns Hopkins University being a member of CCVL advised by [Alan Yuille](https://www.cs.jhu.edu/~ayuille/). I also work closely with [Haohan Wang](https://haohanwang.github.io/) from University of Illinois Urbana-Champaign.
Feel free to visit my [homepage](https://williamium3000.github.io/) and contact me for collaboration and discussion. -->


## Table of Contents
- [Awesome-Video-Multi-modal Large Language Models](#awesome-video-multi-modal-large-language-models)
  - [Table of Contents](#table-of-contents)
  - [🔥 Video Multimodal Large Language Models](#-video-multimodal-large-language-models)
    - [Training Recipe](#training-recipe)
    - [Evaluation Dataset](#eval-dataset)
  - [🔥 Video MLLM with Referring and Grounding](#-video-mllm-with-referring-and-grounding)

## 🔥 Video Multimodal Large Language Models

### Training Recipe

| Method | Recipe | Architecture |
|------------|--------------|--------------|
| [Video-LLaMA](https://arxiv.org/pdf/2306.02858) | <li> PT video/image-caption: [Webvid-2.5M](https://www.robots.ox.ac.uk/~vgg/research/frozen-in-time/), [LLaVA-CC3M](https://github.com/haotian-liu/LLaVA/blob/main/docs/Data.md) <li> SFT image-video inst tuning: [llava-150k](https://huggingface.co/datasets/liuhaotian/LLaVA-Instruct-150K), [minigpt-4 3k](https://github.com/Vision-CAIR/MiniGPT-4/blob/main/dataset/README_2_STAGE.md), [videochat-11k](https://github.com/OpenGVLab/InternVideo/tree/main/Data/instruction_data)| place_holder |
|[VideoChat](https://arxiv.org/pdf/2305.06355)|<li> PT video/image-caption: [Webvid-10M](https://www.robots.ox.ac.uk/~vgg/research/frozen-in-time/), COCO Cap, VG, SBU, CC3M, CC12M <li> SFT image-video inst tuning: [videochat-11k](https://github.com/OpenGVLab/InternVideo/tree/main/Data/instruction_data), [minigpt-4 3k](https://github.com/Vision-CAIR/MiniGPT-4/blob/main/dataset/README_2_STAGE.md), 4k from [llava](https://github.com/haotian-liu/LLaVA?tab=readme-ov-file) | place_holder |
|[VideoChat2](https://arxiv.org/pdf/2305.06355)|<li> Stage1: [Webvid-10M](https://www.robots.ox.ac.uk/~vgg/research/frozen-in-time/), CC3M, CC12M <li> Stage2: COCO, VG, SBU, [InternVid-10M](https://huggingface.co/datasets/OpenGVLab/InternVid) <li> Stage3: [VideoChat2-IT](https://huggingface.co/datasets/OpenGVLab/VideoChat2-IT) | place_holder |


### Evaluation Dataset

## 🔥 Video MLLM with Referring and Grounding

