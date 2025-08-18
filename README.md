# Lost-in-Alignment
Lost in Alignment: A Survey on Cross-lingual Alignment Methods for Contextualised Representation

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

- Aldarmaki et al. 2019: https://github.com/h-aldarmaki/sent_translation_retrieval
- Schuster et al. 2019: https://github.com/TalSchuster/CrossLingualContextualEmb
- Wieting et al. 2019: https://github.com/jwieting/simple-and-effective-paraphrastic-similarity
- Wang et al. 2019 - CLBT: https://github.com/WangYuxuan93/CLBT
- Artetxe et al. 2019 - LASER: https://github.com/facebookresearch/LASER
- Cao et al. 2020: 
