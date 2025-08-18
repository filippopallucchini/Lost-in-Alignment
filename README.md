# Lost-in-Alignment
Lost in Alignment: A Survey on Cross-lingual Alignment Methods for Contextualised Representation

## WIP ##

## CROSS-LINGUAL ALIGNMENT TAXONOMY ##

<img width="519" height="321" alt="Screenshot 2025-08-19 alle 00 22 50" src="https://github.com/user-attachments/assets/1a5eedf1-4ec9-4a5a-ac00-cfbea4e31a95" />

- N Monolingual Corpora: It refers to the N monolingual corpora used as input for the embedding model.
- Train N Embeddings: It refers to training N contextualised language models that need to be aligned. NB: numerous authors do not train models but use already existing pre-trained models.
- Anchors Selection: It describes the procedure for selecting anchors, which are reference points to guide the mapping of one embedding into the other or directly create a common space for different corpora. This selection process may involve pairs of words or pairs of sentences. It can also involve a standalone model for pair extraction (e.g., a word alignment method) or an off-the-shelf list of pairs.
- Cross-Lingual Alignment: It refers to a linear or non-linear transformation that maps source embeddings to the target language or to a shared space.
- Train Multilingual Embeddings: It is related to the process of training a contextualised multilingual language model. %that needs adjustment.
- Adjust Multilingual Embeddings: It refers to fine-tuning methods used to adjust an existing multilingual model, creating a more effective cross-lingual language model. The main difference with respect to the cross-lingual alignment box is that in this case, languages are already in the same embedding space, but there is a further modification of it to align them.
- Parallel Corpora: It refers to both the monolingual corpus and its respective corpus translated into another language. These are used as input for the multilingual embedding model.
- Train+Align Multilingual Embeddings: It is related to the process of training a multilingual language model that utilises objective functions during the training phase to represent cross-linguality.

## CLASSIFICATION OF THE MODELS ##

<img width="669" height="522" alt="Screenshot 2025-08-19 alle 00 23 32" src="https://github.com/user-attachments/assets/06b69a9b-3371-4f1c-b4fb-0dd06426e137" />
