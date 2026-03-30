# Data

### 1. A collection of named entities from sources on Yugoslav nonalignment
These are pilot datasets created from a small corpus of Yugoslav archival and print sources concerning the activities of the Socialist Alliance of the Working People of Yugoslavia in the 1950s. They serve as partial basis for our inquiry on the life of Veljko Vlahović 

The workflow was composed of the following steps:

1. [A BERT-like language model fine-tuned for Slavic languages](https://ner.musiclab.si) was used to conduct a pilot named-entity extraction on this corpus, of which a detailed description can be found in the repository.
2. The data in a JSON file was then normalized with a Python script that uses DeepSeek's API to trace/guess the canonical forms of entities. Separate CSVs were extracted.
3. Using DeepSeek was efficient time-wise, but due to the well-known risk of hallucination the data had to be checked manually and cleaned on OpenRefine. OR also allowed for data reconciliation with Wikidata's base and data enrichment.
4. The result were two datasets, repectively of **organizations** and **persons** involved in the foreign relations of the Yugoslav communist regime.
