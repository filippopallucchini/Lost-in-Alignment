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

- Aldarmaki et al. 2019 --> [[paper](https://aclanthology.org/N19-1391/)] [[code](https://github.com/h-aldarmaki/sent_translation_retrieval)]
- Schuster et al. 2019 --> [[paper](https://aclanthology.org/N19-1162/)] [[code](https://github.com/TalSchuster/CrossLingualContextualEmb)]
- Wieting et al. 2019 --> [[paper](https://aclanthology.org/P19-1453/)] [[code](https://github.com/jwieting/simple-and-effective-paraphrastic-similarity)]
- Wang et al. 2019 - CLBT --> [[paper](https://aclanthology.org/D19-1575/)] [[code](https://github.com/WangYuxuan93/CLBT)]
- Artetxe et al. 2019 - LASER --> [paper](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00288/43523/Massively-Multilingual-Sentence-Embeddings-for) [code](https://github.com/facebookresearch/LASER)]
- Cao et al. 2020 --> [paper](https://iclr.cc/virtual_2020/poster_r1xCMyBtPS.html)
- Wang et al. 2020 --> [paper](https://iclr.cc/virtual_2020/poster_S1l-C0NtwS.html) [code](https://github.com/thespectrewithin/joint_align)
- Wu et al. 2020 [paper](https://aclanthology.org/2020.emnlp-main.362/) [code](https://github.com/shijie-wu/crosslingual-nlp/tree/master/example/contrastive-alignment)
- Chi et al. 2020 - XNLG --> [paper](https://ojs.aaai.org/index.php/AAAI/article/view/6256) [code](https://github.com/CZWin32768/XNLG)
- Reimers et al. 2020: [paper](https://aclanthology.org/2020.emnlp-main.365/) [code](https://github.com/UKPLab/sentence-transformers/blob/master/examples/sentence_transformer/training/multilingual/README.md)
- Pan et al. 2021: paper --> [paper](https://aclanthology.org/2021.naacl-main.20/?utm_campaign=%E6%AF%8E%E9%80%B1%20NLP%20%E8%AB%96%E6%96%87&utm_medium=email&utm_source=Revue%20newsletter)
- Hu et al. 2021 - AMBER --> [paper](https://aclanthology.org/2021.naacl-main.284/) [code](https://github.com/JunjieHu/amber)
- Alqahtani et al. 2021 --> [paper](https://aclanthology.org/2021.findings-emnlp.329/) 
- Chi et al. 2021 - infoXLM --> [paper](https://aclanthology.org/2021.naacl-main.280/?utm_campaign=%E6%AF%8E%E9%80%B1%20NLP%20%E8%AB%96%E6%96%87&utm_medium=email&utm_source=Revue%20newsletter) [code](https://github.com/microsoft/unilm/tree/master/infoxlm)
- Zhao et al. 2021 --> [paper](https://aclanthology.org/2021.starsem-1.22/) [code](https://github.com/AIPHES/Language-Agnostic-Contextualized-Encoders)
- Goswami et al. 2021 - DuEAM --> [paper](https://aclanthology.org/2021.emnlp-main.716/) []()
- Gritta et al. 2021 - XeroAlign --> [paper](https://aclanthology.org/2021.findings-acl.32/)
- Ulˇcar et al. 2022 - Vecmap/MUSE --> [paper](https://link.springer.com/article/10.1007/s00521-022-07164-x) 
- Ulˇcar et al. 2022 - ELMOGAN --> [paper](https://link.springer.com/article/10.1007/s00521-022-07164-x) [code](https://github.com/TalSchuster/CrossLingualContextualEmb)
- Liu et al. 2022 - Bi-SaELMO --> [paper](https://aclanthology.org/2022.coling-1.386/) [code](https://github.com/ntunlp/multisense_embedding_alignment)
- Tien et al. 2022 --> [paper](https://aclanthology.org/2022.acl-long.595/) [code](https://github.com/cctien/bimultialign)
- Feng et al. 2022 - LaBSE --> [paper](https://aclanthology.org/2022.acl-long.62/)
- Ding et al. 2022 - EAR --> [paper](https://aclanthology.org/2022.coling-1.385/) [code](https://github.com/KB-Ding/EAR)
- Heffernan et al. 2022 - LASER3 --> [paper](https://aclanthology.org/2022.findings-emnlp.154/) [code](https://github.com/facebookresearch/fairseq/tree/nllb/examples/nllb/laser_distillation)
- Hämmerl et al. 2022 --> [paper](https://aclanthology.org/2022.findings-acl.182/) [code](https://github.com/KathyHaem/combining-static-contextual)
- Efimov et al. 2023 --> [paper](https://link.springer.com/chapter/10.1007/978-3-031-28241-6_4) [code](https://github.com/pefimov/cross-lingual-adjustment)
- Abulkhanov et al. 2023 - LAPCA --> [paper](https://dl.acm.org/doi/abs/10.1145/3539618.3592006?casa_token=YIC1V5Gr9mcAAAAA:lJ7ojquwwOUxUrPZtjmGdt6yaVI-ZEVw6GWJ1FlK_20wi9k1ldO00bAWus7xWM548KdPPNAA8j3J) 
- Tan et al. 2023 - LASER3-CO --> [paper](https://aclanthology.org/2023.eacl-main.108/)
- Li et al. 2023 --> [paper](https://virtual2023.aclweb.org/paper_P2288.html)
- Li et al. 2024 - AFP --> [paper](https://aclanthology.org/2024.naacl-long.445/) [code](https://github.com/chongli17/CrossLingualAlignment)
- Vasilyev et al. 2024 --> [paper](https://aclanthology.org/2024.findings-acl.486/)
- Jiang et al. 2024 - CLASS --> [paper](https://aclanthology.org/2024.emnlp-main.770/) [code](https://github.com/Fantabulous-J/CLASS)
- Bakos et al. 2025 - AlignFreeze --> [paper](https://aclanthology.org/2025.naacl-short.48/) [code](https://github.com/posos-tech/multilingual-alignment-and-transfer/tree/main/scripts/2025_naacl)
- Feng et al. 2025 - IDA --> [paper](https://aclanthology.org/2025.coling-main.138/)
- Liu et al. 2025 --> [paper](https://aclanthology.org/2025.acl-long.778/) [code](https://github.com/dannigt/mid-align)
- Sundar et al. 2025 --> [paper](https://aclanthology.org/2025.acl-long.118/) 
- Jha et al. 2025 - vec2vec --> [paper](https://arxiv.org/abs/2505.12540) [code](https://github.com/rjha18/vec2vec/)
- Deng et al. 2025 --> [paper](https://arxiv.org/abs/2502.11401) [code](https://github.com/TrustedLLM/AutoRegEmbed)


## Cite this Article ##
@article{pallucchini2025lost,
  title={Lost in Alignment: A Survey on Cross-lingual Alignment Methods for Contextualised Representation},
  author={Pallucchini, Filippo and Malandri, Lorenzo and Mezzanzanica, Mario and Mercorio, Fabio},
  journal={ACM computing surveys},
  pages={1--37},
  year={2025},
  publisher={ACM New York, NY}
}
