# image-caption-analysis


This project is a comparative study of Image caption generation model . This experiment aims to provide:
- A detailed breakdown of the architectures and mechanisms of ViT-GPT2, BLIP, and GIT.
- A quantitative and qualitative analysis of their performance.
- Insights into the strengths, limitations, and suitability of each model for real-world applications.


The dataset utilized for this study consists of 600 images, sourced exclusively from open-access platforms to ensure accessibility and reproducibility. Each image was meticulously self-annotated with high-quality captions to create a reliable ground truth for evaluating the models' performance.

<b><u>Dataset Composition </u></b>

To ensure diversity and robustness, the dataset spans multiple categories:
- <b>Animals:</b> Includes various species in diverse settings, such as wildlife, pets, and zoos.
- <b>Humans:</b> Depicts people in natural environments, performing activities, and interacting with objects.
- <b>Architecture:</b> Captures man-made structures, including buildings, bridges, and urban landscapes.
- <b>Natural Formations and Nature:</b> Covers landscapes, forests, mountains, rivers, and other natural scenes.
- <b>Everyday Objects:</b> Features commonly found objects, such as tools, household items, and vehicles.

<u>Sample Image:</u>
<!-- ![Sample Image](/sample_image/cat9_img1.jpeg) -->
<img src="/sample_image/cat9_img1.jpeg" width="128">

<b>Custom Annotation</b> - Man attempting a slam dunk <br>
<b>vit-gpt2</b> - a woman jumping in the air to catch a frisbee<br>
<b>blip-conditional</b> - a photography of a basketball player jumping to the basket<br>
<b>blip-unconditional</b> - a man jumping in the air with a basketball<br>
<b>git</b> - a young man playing basketball in a gym.<br>

The models that were used for caption generation are:
1. [vit-gpt2](https://huggingface.co/nlpconnect/vit-gpt2-image-captioning)
2. [blip-conditional by Salesforce](https://huggingface.co/Salesforce/blip-image-captioning-base)
3. [blip-unconditional by Salesforce](https://huggingface.co/Salesforce/blip-image-captioning-base)
4. [git by Micrsoft](https://huggingface.co/microsoft/git-base)



The folder <code>captions</code> in the repository contains all groundtruth captions as well as the model generated captions. 



The annotations can be viewed in this [sheet](https://docs.google.com/spreadsheets/d/18qtOlw3fx2U0tpsXaBPplqvpL3YJEQoUMMsRXHYoeHU/edit?usp=sharing) or in <code>all_captions.csv</code> file. 

We used three metrics for our comparative study:
1. METEOR
2. BLEU-1
3. BLEU-2


The results are calculated in <code>score.ipynb</code> notebook.The table and the graphs obtained from the study is shown below:

| Model                    | METEOR | BLEU-1 | BLEU-2 |
|--------------------------|--------|--------|--------|
| ViT-GPT2                 | 0.1644 | 0.1845 | 0.0816 |
| GIT                      | 0.2207 | 0.2301 | 0.117  |
| BLIP (Conditional)       | 0.2418 | 0.2357 | 0.1246 |
| BLIP (Unconditional)     | 0.2426 | 0.2555 | 0.1327 |


---
<b>Combined METEOR for models tested</b>
---

![METEOR1](/results/Combined-meteor/combined-meteor-1.png)
![METEOR2](/results/Combined-meteor/combined-meteor-2.png)
![METEOR3](/results/Combined-meteor/combined-meteor-3.png)

---
<b>Combined BLEU-1 for models tested</b>
---
![BLEU1-1](/results/Combined-bleu1/combined-bleu1-1.png)
![BLEU1-2](/results/Combined-bleu1/combined-bleu1-2.png)
![BLEU1-3](/results/Combined-bleu1/combined-bleu1-3.png)

---
<b>Combined BLEU-2 for models tested</b>
---
![BLEU2-1](/results/Combined-bleu-2/combined-bleu2-1.png)
![BLEU2-2](/results/Combined-bleu-2/combined-bleu2-2.png)
![BLEU2-3](/results/Combined-bleu-2/combined-bleu2-3.png)

---