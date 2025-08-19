# Lost-in-Alignment
### Lost in Alignment: A Survey on Cross-lingual Alignment Methods for Contextualised Representation ###
Cross-lingual word representations allow us to analyse word meanings across diverse language settings. It is crucial in aiding cross-lingual knowledge transfer when constructing natural language processing (NLP) models for languages with limited resources. This survey presents a comprehensive classification of cross-lingual contextual embedding models. We assess their data requirements and objective functions, and we introduce a taxonomy for categorising these approaches. Then, we present a comprehensive table containing a set of hierarchical criteria to compare them better, along with information regarding the availability of code and data to enable replication of the research. Furthermore, we delve into the evaluation methodologies employed for cross-lingual embeddings, exploring their practical applications and addressing their current associated challenges.

## WIP ##

## CROSS-LINGUAL ALIGNMENT TAXONOMY ##
<img width="922" height="581" alt="Screenshot 2025-08-19 alle 00 29 44" src="https://github.com/user-attachments/assets/0fcd0cd3-de22-4ac0-98f5-a84e8c16b751" />

- N Monolingual Corpora: It refers to the N monolingual corpora used as input for the embedding model.
- Train N Embeddings: It refers to training N contextualised language models that need to be aligned. NB: numerous authors do not train models but use already existing pre-trained models.
- Anchors Selection: It describes the procedure for selecting anchors, which are reference points to guide the mapping of one embedding into the other or directly create a common space for different corpora. This selection process may involve pairs of words or pairs of sentences. It can also involve a standalone model for pair extraction (e.g., a word alignment method) or an off-the-shelf list of pairs.
- Cross-Lingual Alignment: It refers to a linear or non-linear transformation that maps source embeddings to the target language or to a shared space.
- Train Multilingual Embeddings: It is related to the process of training a contextualised multilingual language model. %that needs adjustment.
- Adjust Multilingual Embeddings: It refers to fine-tuning methods used to adjust an existing multilingual model, creating a more effective cross-lingual language model. The main difference with respect to the cross-lingual alignment box is that in this case, languages are already in the same embedding space, but there is a further modification of it to align them.
- Parallel Corpora: It refers to both the monolingual corpus and its respective corpus translated into another language. These are used as input for the multilingual embedding model.
- Train+Align Multilingual Embeddings: It is related to the process of training a multilingual language model that utilises objective functions during the training phase to represent cross-linguality.

## CLASSIFICATION OF THE MODELS ##
<img width="939" height="724" alt="Screenshot 2025-08-19 alle 00 30 25" src="https://github.com/user-attachments/assets/6d51f045-237d-4122-875e-e56ab6abfb96" />

- Aldarmaki et al. 2019:
 - [paper](https://aclanthology.org/N19-1391/) [code](https://github.com/h-aldarmaki/sent_translation_retrieval)
- Schuster et al. 2019: https://github.com/TalSchuster/CrossLingualContextualEmb
- Wieting et al. 2019: https://github.com/jwieting/simple-and-effective-paraphrastic-similarity
- Wang et al. 2019 - CLBT: https://github.com/WangYuxuan93/CLBT
- Artetxe et al. 2019 - LASER: https://github.com/facebookresearch/LASER
- Cao et al. 2020: paper:
- Wang et al. 2020: paper: https://arxiv.org/abs/1910.04708 code: https://github.com/thespectrewithin/joint_align 
- Wu et al. 2020:
- Chi et al. 2020 - XNLG: 
- Reimers et al. 2020:
- Pan et al. 2021: paper:
- Hu et al. 2021 - AMBER: paper:
- Alqahtani et al. 2021: paper:
- Chi et al. 2021 - infoXLM
- Zhao et al. 2021:
- Goswami et al. 2021 - DuEAM: paper:
- Gritta et al. 2021 - XeroAlign:
- Ulˇcar et al. 2022 - Vecmap/MUSE:
- Ulˇcar et al. 2022 - ELMOGAN:
- Liu et al. 2022 - Bi-SaELMO:
- Tien et al. 2022:
- Feng et al. 2022 - LaBSE: paper:
- Ding et al. 2022:
- Heffernan et al. 2022 - LASER3:
- Hämmerl et al. 2022:
- Efimov et al. 2023:
- Abulkhanov et al. 2023 - LAPCA: paper:
- Tan et al. 2023 - LASER3-CO: paper:
- Li et al. 2023: paper:
- Li et al. 2024 - AFP:
- Vasilyev et al. 2024: paper:
- Jiang et al. 2024 - CLASS:
- Bakos et al. 2025 - AlignFreeze:
- Feng et al. 2025 - IDA:
- Liu et al. 2025:
- Sundar et al. 2025:
- Jha et al. 2025 - vec2vec
- Deng et al. 2025:


## Cite this Article ##
@article{pallucchini2025lost,
  title={Lost in Alignment: A Survey on Cross-lingual Alignment Methods for Contextualised Representation},
  author={Pallucchini, Filippo and Malandri, Lorenzo and Mezzanzanica, Mario and Mercorio, Fabio},
  journal={ACM computing surveys},
  pages={1--37},
  year={2025},
  publisher={ACM New York, NY}
}
