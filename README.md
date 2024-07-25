# Awesome-Video-Multi-modal Large Language Models
> A curated list of Video Multimodal Large Language Models. 

<!-- ## About Me: 
I'm an incoming Ph.D. student at the University of California San Diego. I received my M.S.E in Computer Science at Johns Hopkins University being a member of CCVL advised by [Alan Yuille](https://www.cs.jhu.edu/~ayuille/). I also work closely with [Haohan Wang](https://haohanwang.github.io/) from University of Illinois Urbana-Champaign.
Feel free to visit my [homepage](https://williamium3000.github.io/) and contact me for collaboration and discussion. -->


## Table of Contents
- [Awesome-Video-Multi-modal Large Language Models](#awesome-video-multi-modal-large-language-models)
  - [Table of Contents](#table-of-contents)
  - [🔥 Video Multimodal Large Language Models](#-video-multimodal-large-language-models)
    - [Instruction Dataset](#instruction-dataset)
    - [Training Recipe](#training-recipe)
    - [Evaluation Dataset](#eval-dataset)
  - [🔥 Video MLLM with Referring and Grounding](#-video-mllm-with-referring-and-grounding)

## 🔥 Video Multimodal Large Language Models


### Instruction Dataset

| Dataset | Source | Data Source | Quantity | Cnstruction Method |
|------------|--------------|--------------|--------------|--------------|
[VideoInstruct100K](https://github.com/mbzuai-oryx/Video-ChatGPT/blob/main/docs/train_video_chatgpt.md) | [Video-ChatGPT](https://arxiv.org/pdf/2306.05424) | ActivityNet | 100k | |



### Training Recipe
| Method | Training Data | Eval Data | Recipe | Architecture |
|------------|--------------|--------------|--------------|--------------|
| [Video-LLaMA](https://arxiv.org/pdf/2306.02858) | <li> PT video/image-caption: [Webvid-2.5M](https://www.robots.ox.ac.uk/~vgg/research/frozen-in-time/), [LLaVA-CC3M](https://github.com/haotian-liu/LLaVA/blob/main/docs/Data.md) <li> SFT image-video inst tuning: [llava-150k](https://huggingface.co/datasets/liuhaotian/LLaVA-Instruct-150K), [minigpt-4 3k](https://github.com/Vision-CAIR/MiniGPT-4/blob/main/dataset/README_2_STAGE.md), [videochat-11k](https://github.com/OpenGVLab/InternVideo/tree/main/Data/instruction_data)|place_holder | place_holder | place_holder |
| [Video-LLaMA2](https://arxiv.org/pdf/2406.07476) | <li> PT video/image-caption: [Webvid-10M](https://www.robots.ox.ac.uk/~vgg/research/frozen-in-time/), [Panda-70M](https://snap-research.github.io/Panda-70M/), [VIDAL-10M](https://github.com/PKU-YuanGroup/LanguageBind/blob/main/DATASETS.md), [InternVid-10M], CC3M, [DCI](https://github.com/facebookresearch/DCI) <li> SFT image-video inst tuning: [videochat-11k](https://github.com/OpenGVLab/InternVideo/tree/main/Data/instruction_data), In-house data-12k, [Kinetics-710](https://github.com/OpenGVLab/UniFormerV2/blob/main/DATASET.md), [SthSthv2](https://developer.qualcomm.com/software/ai-datasets/something-something), NExTQA, CLEVRER, EgoQA, Tgif, WebVidQA, RealworldQA, Hm3d, Valley, VideoChatGPT, VideoChat, VTimeLLM, VideoChat2, sharegpt4v, [llava-665k](https://huggingface.co/datasets/liuhaotian/LLaVA-Instruct-150K/blob/main/llava_v1_5_mix665k.json)| place_holder | place_holder | place_holder |
| [VideoChat](https://arxiv.org/pdf/2305.06355)|<li> PT video/image-caption: [Webvid-10M](https://www.robots.ox.ac.uk/~vgg/research/frozen-in-time/), COCO Cap, VG, SBU, CC3M, CC12M <li> SFT image-video inst tuning: [videochat-11k](https://github.com/OpenGVLab/InternVideo/tree/main/Data/instruction_data), [minigpt-4 3k](https://github.com/Vision-CAIR/MiniGPT-4/blob/main/dataset/README_2_STAGE.md), 4k from [llava](https://github.com/haotian-liu/LLaVA?tab=readme-ov-file) | place_holder | place_holder | place_holder |
| [VideoChat2](https://arxiv.org/pdf/2305.06355)|<li> Stage1: [Webvid-10M](https://www.robots.ox.ac.uk/~vgg/research/frozen-in-time/), CC3M, CC12M <li> Stage2: COCO, VG, SBU, [InternVid-10M](https://huggingface.co/datasets/OpenGVLab/InternVid) <li> Stage3: [VideoChat2-IT](https://huggingface.co/datasets/OpenGVLab/VideoChat2-IT) | place_holder | place_holder | place_holder |
| [Valley](https://arxiv.org/pdf/2306.07207) | <li> PT video/image-caption: [LLaVA-CC3M](https://github.com/haotian-liu/LLaVA/blob/main/docs/Data.md)，[Valley-webvid2M-Pretrain-703K ](https://huggingface.co/datasets/luoruipu1/Valley-webvid2M-Pretrain-703K) <li> SFT inst tuning: [llava-150k](https://huggingface.co/datasets/liuhaotian/LLaVA-Instruct-150K), [videochat-11k](https://github.com/OpenGVLab/InternVideo/tree/main/Data/instruction_data), [Valley-Instruct-65K](https://huggingface.co/datasets/luoruipu1/Valley-Instruct-65k) | place_holder | place_holder | place_holder |
| [Video-ChatGPT](https://arxiv.org/pdf/2306.05424) | [VideoInstruct100K](https://github.com/mbzuai-oryx/Video-ChatGPT/blob/main/docs/train_video_chatgpt.md) | place_holder | place_holder | place_holder |
| [Video-LLaVA](https://arxiv.org/pdf/2311.10122) | <li> PT video/image-caption (same as [Valley](https://arxiv.org/pdf/2306.07207)): [LLaVA-CC3M](https://github.com/haotian-liu/LLaVA/blob/main/docs/Data.md)，[Valley-webvid2M-Pretrain-703K](https://huggingface.co/datasets/luoruipu1/Valley-webvid2M-Pretrain-703K) <li> SFT inst tuning: [llava-150k](https://huggingface.co/datasets/liuhaotian/LLaVA-Instruct-150K), [VideoInstruct100K](https://github.com/mbzuai-oryx/Video-ChatGPT/blob/main/docs/train_video_chatgpt.md) | [Video-ChatGPT Quantitative Evaluation](https://github.com/mbzuai-oryx/Video-ChatGPT/tree/main/quantitative_evaluation) | place_holder | place_holder |

### Evaluation Dataset

## 🔥 Video MLLM with Referring and Grounding

