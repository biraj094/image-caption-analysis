# image-caption-analysis


This project is a comparative study of Image caption generation model . For the purpose of this project 600 custom images were selected and annotated. That was the grouth truth for the experiment. 

<u>Sample Image:</u>
<!-- ![Sample Image](/sample_image/cat9_img1.jpeg) -->
<img src="/sample_image/cat9_img1.jpeg" width="48">

<b>Custom Annotation</b> - Man attempting a slam dunk <br>
<b>vit</b> - a woman jumping in the air to catch a frisbee<br>
<b>blip</b> - a photography of a basketball player jumping to the basket<br>
<b>blip</b> - a man jumping in the air with a basketball<br>
<b>git</b> - a young man playing basketball in a gym.<br>

The models that were used for caption generation are:
1. [vit-gpt2](https://huggingface.co/nlpconnect/vit-gpt2-image-captioning)
2. [blip-conditional by Salesforce](https://huggingface.co/Salesforce/blip-image-captioning-base)
3. [blip-unconditional by Salesforce](https://huggingface.co/Salesforce/blip-image-captioning-base)
4. [git by Micrsoft](https://huggingface.co/microsoft/git-base)



The folder <code>captions</code> in the repository contains all groundtruth captions as well as the model generated captions. 

The annotations can be viewed in this [sheet](https://docs.google.com/spreadsheets/d/18qtOlw3fx2U0tpsXaBPplqvpL3YJEQoUMMsRXHYoeHU/edit?usp=sharing) as well. 


We used three metrics for our comparative study:
1. METEOR
2. BLEU-1
3. BLEU-2


The results are shown below:

<b>Combined METEOR for models tested</b>

![METEOR1](/results/Combined-meteor/combined-meteor-1.png)
![METEOR2](/results/Combined-meteor/combined-meteor-2.png)
![METEOR3](/results/Combined-meteor/combined-meteor-3.png)

---

<b>Combined BLEU-1 for models tested</b>

![BLEU1-1](/results/Combined-bleu1/combined-bleu1-1.png)
![BLEU1-2](/results/Combined-bleu1/combined-bleu1-2.png)
![BLEU1-3](/results/Combined-bleu1/combined-bleu1-3.png)

---

<b>Combined BLEU-2 for models tested</b>

![BLEU2-1](/results/Combined-bleu-2/combined-bleu2-1.png)
![BLEU2-2](/results/Combined-bleu-2/combined-bleu2-2.png)
![BLEU2-3](/results/Combined-bleu-2/combined-bleu2-3.png)

---