# Large language models for psycholinguistics
### A tutorial notebook

You can find the Colab notebook [here](https://drive.google.com/file/d/1NkIgEsPuNN1uiN4-kM8r-XluBqtBX17V/view?usp=sharing). The present GitHub repo comes with the materials used in the tutorial (images, text)

---

### About
The present notebook is a guide on (mostly) language models. It was developed over the course of two workshops as a learning resource for psychologists, linguists and neuroscientists, and is geared toward that audience (I'm one of them myself! 😺). Lacking extensive commentary, I suggest using the notebook as a playground! Code sections also come with example exercises, followed by possible solutions. The main topics covered are:
*  **representations** in LLMs: extracting and comparing word embeddings, probe the effects of context, compare representations within and across models
*  **prediction** in LLMs: extracting predictability measures, use them to probe the 'knowledge' of models
*  **multimodality**: extract representations from a computer vision models, compare them to those of LLMs, and extract prediction measures from language-vision models

---

### **Acknowledgements**

The notebook was first developed for [WoProc 2024](https://moproc2024.net/) (2h workshop) and was then greatly expanded for the [MEDAL Summer School in Computational Modelling](https://medal.ut.ee/event/medal-summer-school-in-computational-linguistics/) (6h workshop). I am grateful to the organizers of WoProc and MEDAL for the opportunity to carry out my workshops and thus develop these materials, and to the attendees for their feedback. I am thankful to Marco Marelli, Anastasia Galkina and Lance Gamboa for their comments, to Giovanni Cassani and Fritz Günther for sharing valuable materials. Finally, most of what is covered leverages (and is made possible by) the `minicons` library:
<medium>
> Misra, K. (2022). minicons: Enabling flexible behavioral and representational analyses of transformer language models. arXiv preprint arXiv:2203.13112.
</medium>

while workshop materials include the Words in Cotext (WiC) dataset annotated and copyright-free images from the THINGSplus dataset:
<small>
> Pilehvar, M. T., & Camacho-Collados, J. (2018). WiC: the word-in-context dataset for evaluating context-sensitive meaning representations. arXiv preprint arXiv:1808.09121.

> Cassani, G., Günther, F., Attanasio, G., Bianchi, F., & Marelli, M. (2023). Meaning Modulations and Stability in Large Language Models: An Analysis of BERT Embeddings for Psycholinguistic Research.

> Stoinski, L. M., Perkuhn, J., & Hebart, M. N. (2024). THINGSplus: New norms and metadata for the THINGS database of 1854 object concepts and 26,107 natural object images. Behavior Research Methods, 56(3), 1583-1603.
</small>

---

### Examples from the notebook
Extract word embeddings from BERT and inspect how context can modulate their representation. For example, what happens to <ins>fruitless</ins> when we place it in a sentence that points to its typical methaporical meaning ("vain") as opposed to one where its meaning is literal ("without fruits")? 

<p align="center">
  <img src="example_outputs/example_fruitless.png" alt="Colab Demo" width="700"/>
</p>

<br>

Observe the effect of replacing a word with sense-appropriate and sense-inappropriate alternatives using the [WiC annotated dataset](https://osf.io/preprints/psyarxiv/b45ys_v1). Look at the effects of context-word interaction on both embeddings and surprisal:

<p align="center">
  <img src="example_outputs/example_wic.png" alt="Colab Demo" width="700"/>
</p>

<br>

Perform representational similarity analysis to compare how the same concepts are represented across languages (in their correponding monolingual models):

<p align="center">
  <img src="example_outputs/example_RSA_crosslingual.png" alt="Colab Demo" width="650"/>
</p>

<br>

Compare concept representations across modalities in unimodal models, using the AlexNet convolutional neural network to represent images (from the [THINGSplus database](https://link.springer.com/article/10.3758/s13428-023-02110-8)) and BERT-large to represent their captions:

<p align="center">
  <img src="example_outputs/example_RSA_crossmodal.png" alt="Colab Demo" width="700"/>
</p>
