# Named-Entity-Linking-Latin-DAAL-2024

Repository for data Named Entity Linking for Latin for Data-driven Approaches to Ancient Languages (DAAL) 2024.

# Gold data

The folder Gold_data contains the following two manually annotated texts with all person entities linked to _Paulys Realencyclopädie der classischen Altertumswissenschaft_ (_RE_):
- Tacitus, _Historiae_ 1 ([LASLA edition](https://www.lasla.uliege.be/cms/c_8570411/fr/lasla-textes-latins)), every token is associated to its token and lemma URIs as found in the [LiLa Knowledge Base](https://lila-erc.eu/query/). The full version of the LASLA annotated text with the linking to the LiLa Knowledge Base is available here: https://zenodo.org/doi/10.5281/zenodo.5961377.
- Ammianus Marcellinus, _Res Gestae_ XIV ([LTA edition](https://lta.bbaw.de/text/show/24819722_ammianus_marcellinus_res_gestae)), automatically transformed from XML to CSV and appended Token_URIs

Entities were annotated and linked by Evelien de Graaf and Margherita Fantoli.

# Name dictionaries
The name dictionary created from the _RE_ as described in the paper is available here in two formats:
- **Standard name dictionary**:
  
| Key (name)   | Value (re_id)               |
|--------------|-----------------------------|
| Iulius       | Iulius 1 (RE-Iulius_1)      |
|              | ...                         |
|              | Iulius 16 (RE-Iulius_16) etc. |
| C. Iulius    | Iulius 16 (RE-Iulius_16)    |
| Gaius Iulius | Iulius 16 (RE-Iulius_16)    |

- ID-dictionary

| Key (re_id)  | Value (potential surface forms) |
|--------------|---------------------------------|
| RE-Iulius_1  | Iulius                          |
|              | Iunius                          |
| RE-Iulius_16 | C. Iulius                       |
|              | Caius Iulius                    |
|              | Caius                           |
|              | Iulius                          |

# Fuzzy matching
The Jupyter notebook (Fuzzy matching - Latin NEL.ipynb) contains an explanation and illustration of the Fuzzy-matching process used in the paper. It contains a detailed description of the use of RapidFuzz for fuzzy matching and the exact code for the multi-token layer.

The full pipeline illustration can be found below.



![NEL_pipepline_illustration_hor](https://github.com/evelien-degraaf/Named-Entity-Linking-Latin-DAAL-2024/assets/127041405/4e18af09-0f96-4a4c-8004-23f173631839)
