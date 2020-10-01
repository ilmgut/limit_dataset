# Dataset for the paper "LiMiT: The Literal Motion in Text Dataset".

LiMiT Dataset described in the paper: "LiMiT: The Literal Motion in Text Dataset", Findings of EMNLP, 2020.

The limit dataset of ~24K sentences that describe literal motion (~14K sentences), and sentences not describing motion or other type of motion (e.g. fictive motion). Senteces were extracted from electronic books categorized as fiction or novels, and a portion from the [NetActivity Captions Dataset](https://cs.stanford.edu/people/ranjaykrishna/densevid/).

## Labels

Sentences in the LiMiT dataset have two labels: A "motion" label, indicates whether the sentence is literal motion i.e. describes the movement of a physical entity or not; A "motion_entity", has the tokens in the sentence that belong to physical entities in motion. Motion entity labels include, for each entity, the index in the sentence for the first char of the entity tokens.

## Data Format

The data folder contains two files: `train.json` and `test.json`.

Both JSON have the same following structure:

```
{
    {
    // int, ID for sentence
    0:
        {
        // string, sentence text
        "sentence": "The boy jumps over the ball.",

        // string, motion label, "yes" for literal motion, and "no" for no motion or other motion types.
        "motion": "yes",

        // string, entities in motion
        "motion_entity": "boy:5",
        }},
    {1:
        {"sentence": ...
        }
    },...
}


```

## Citation

TBA
