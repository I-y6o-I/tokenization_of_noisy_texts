# BLN600
Human transcriptions of 600 images selected from the British Library Newspapers parts 1 & 2 dataset.

**To discourage automated web-scraping for AI training purposes, BLN600 is released as a password protected ZIP archive. The password is `BLN600`.**

## Changelog
- Version 1 - Initial release.
- Version 2 - Document ID corrections for the 1861-06-30 and 1871-06-11 issues of Lloyd's Weekly Newspaper.

## Directory Layout
- `Images/` - cropped images downloaded from the BLN platform in mixed JPG and TIFF format - indexed by GALE document ID
- `Ground Truth/` - human transcriptions of the images - indexed by GALE document ID to match up with images
- `OCR Text/` - GALE's OCR transcriptions of the images - indexed by GALE document ID to match up with images
- metadata.json - structured document data linking document ID with publication information, article count, and non crime counts

## Document IDs
Documents within the GALE BLN system are indexed by a "document ID"---a 10 digit number, prefixed with a 1 or 2 letter collection ID. Two versions of this ID appear to exist - a short form without the collection ID that data has been returned from GALE with, and a longer form with the collection ID that **must** be used when searching the platform site. For example, the 1834-07-07 issue of the Morning Chronicle has been returned from GALE as document ID `3207163457`, in order to find this document again in the BLN online platform, you will need the longer form `BA3207163457`. The two types are bridged in `metadata.json`. 

## Errors
Care has been taken to ensure the ground truth is high quality through multiple error detection, image comparison, and error correction passes, however errors may still remain. BLN600 claims a high, but not 100% accuracy rate. If you have noticed an error in the ground truth, please report it to one of the authors.

## Access, usage, and modification terms and license
Express permission was sought from and granted by GALE on behalf of the company and the British Library partners, and communicated to the authors electronically, for the release of the OCR text of 600 individual excerpts from the British Library Newspapers corpus parts 1 and 2, under a non-commercial use-only license (CC BY-NC-ND 4.0), publicly accessible with no additional access stipulations.

This research was funded by a UKRI EPSRC PhD studentship (1st author) and by The University of Sheffield's Centre for Machine Intelligence (2nd author).

BLN600 by Callum Booth, Alan Thomas, and Robert Gaizauskas is licensed under Attribution-NonCommercial-NoDerivatives 4.0 International. To view a copy of this license, visit http://creativecommons.org/licenses/by-nc-nd/4.0/

## Paper Citation
Callum William Booth, Alan Thomas, and Robert Gaizauskas. 2024. BLN600: A Parallel Corpus of Machine/Human Transcribed Nineteenth Century Newspaper Texts. In Proceedings of the 2024 Joint International Conference on Computational Linguistics, Language Resources and Evaluation (LREC-COLING 2024), pages 2440–2446, Torino, Italia. ELRA and ICCL.

```
@inproceedings{booth-etal-2024-bln600,
    title = "{BLN}600: A Parallel Corpus of Machine/Human Transcribed Nineteenth Century Newspaper Texts",
    author = "Booth, Callum William  and
      Thomas, Alan  and
      Gaizauskas, Robert",
    editor = "Calzolari, Nicoletta  and
      Kan, Min-Yen  and
      Hoste, Veronique  and
      Lenci, Alessandro  and
      Sakti, Sakriani  and
      Xue, Nianwen",
    booktitle = "Proceedings of the 2024 Joint International Conference on Computational Linguistics, Language Resources and Evaluation (LREC-COLING 2024)",
    month = may,
    year = "2024",
    address = "Torino, Italia",
    publisher = "ELRA and ICCL",
    url = "https://aclanthology.org/2024.lrec-main.219",
    pages = "2440--2446",
    abstract = "We present a publicly available corpus of nineteenth-century newspaper text focused on crime in London, derived from the Gale British Library Newspapers corpus parts 1 and 2. The corpus comprises 600 newspaper excerpts and for each excerpt contains the original source image, the machine transcription of that image as found in the BLN and a gold standard manual transcription that we have created. We envisage the corpus will be helpful for the training and development of OCR and post-OCR correction methodologies for historical newspaper machine transcription{---}for which there is currently a dearth of publicly available resources. In this paper, we discuss the rationale behind gathering such a corpus, the methodology used to select, process, and align the data, and the corpus{'} potential utility for historians and digital humanities researchers{---}particularly within the realms of neural machine translation-based post-OCR correction approaches, and other natural language processing tasks that are critically affected by erroneous OCR.",
}
```