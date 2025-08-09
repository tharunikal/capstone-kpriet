

# part 1 -VUA Metaphor Corpus Augmented Dataset

## Overview
This dataset is a word sense augmentation of the **VU Amsterdam Metaphor Corpus (VUA)**, enriched with
pre-processed versions for metaphor detection research. It includes multiple dataset variants:

- **VUA-18**: Preprocessed version from Leong et al. (2018)
- **VUA-20**: Preprocessed version from Leong et al. (2020)
- **VUAverb**: Focuses exclusively on verb metaphors
- **VUA-MPD-All**: Subset focusing on words available in WordNet
- **VUA-MPD-Conv**: Subset focusing on conventional metaphors (Maudslay & Teufel, 2022)

Each variant contains **train** and **test** splits.

## File Structure
```
data/
    VUA18/
        train.tsv
        test.tsv
    VUA18_pos/
        adj/test.tsv
        adv/test.tsv
        noun/test.tsv
        verb/test.tsv
    VUA20/
        train.tsv
        test.tsv
    VUA_MPD/
        all/train.tsv
        all/test.tsv
        conv/train.tsv
        conv/test.tsv
    VUAverb/
        train.tsv
        test.tsv
    ...
```

## TSV Columns
Each TSV file contains the following columns:

| Column       | Description |
|--------------|-------------|
| **index**    | Document and sentence fragment ID |
| **label**    | `1` = metaphorical usage, `0` = literal usage |
| **sentence** | Full sentence containing the target word |
| **POS**      | Coarse Part-Of-Speech tag (e.g., ADJ, VERB) |
| **FGPOS**    | Fine-grained POS tag (e.g., JJS, NNP) |
| **w_index**  | Position index of the target word in the sentence |
| **target**   | The word being evaluated for metaphorical usage |
| **word_sense** | WordNet word sense description |
| **definition** | Dictionary-style definition of the target word |

## Usage
This dataset can be used for **metaphor detection** and related NLP tasks such as:
- Binary classification of metaphor vs. literal usage
- POS-based metaphor analysis
- Integration with WordNet for semantic tasks

### Example Row
```
index: a1e-fragment01 1
label: 1
sentence: Latest corporate unbundler reveals laid-back approach
POS: VERB
FGPOS: VBZ
w_index: 3
target: reveals
word_sense: make visible
definition: To uncover; to show and display that which was hidden.
```

## Preprocessing Notes
- Sentences are already tokenized and POS-tagged.
- Target words are provided with position indices.
- Word sense and definitions come from WordNet.
- Additional preprocessing is required for transformer-based models (e.g., wrapping target words with special tokens `[TGT]` and `[/TGT]`).



# capstone-kpriet

# drive link 
https://drive.google.com/drive/folders/103pE0BXemnF5a9oehfxlio6Jb7JKGM3B?usp=sharing


