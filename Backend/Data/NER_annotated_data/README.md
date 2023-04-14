# Folder contents

1. <b>ChatGPT/</b> : This folder consists of a dataset generated by ChatGPT. The raw dataset is chatgpt.txt. However, the indexes generated by ChatGPT are wrong and thus, manual labelling was required. After cleaning chatgpt.txt and only retaining the sentences without the wrong indexes, we get chatgpt_sentences.txt. After manually labelling the sentences in chatgpt_sentences.txt, a new labelled dataset, annotations.json is created. Since spaCy requires the annotations to be in a specific .spacy format, we transform annotations.json into annotations.spacy, which is what gets fed into the model during training.
2. <b>GitHub/ & StackOverflow/</b> : This folder consists of an open-source dataset (J. Tabassum, M. Maddela, W. Xu, A. Ritter, 2020) which has labelled text data for training NER models. As the names of the folders suggest, the data originated from Github and StackOverflow forums. <b>NOTE: The datasets within these directories were not used in the final model in the end, though earlier iterations of model building heavily revolved around using them during the training process.</b>
3. <b>Job_Mod_Descriptions/</b> : This folder was originally intended to consist of manually labelled text data for job descriptions and module descriptions. However, due to time constraints, we only managed to label the module descriptions. Future improvements could be made to include labelled job descriptions to train the NER model as well. Within this folder, we see four files. mod_desc-unlabelled.txt consists of the raw unlabelled module description dataset. After labelling, we get mod_annotations_1_to_70.json (first 70 modules) and mod_annotations_71_to_150.json (next 80 modules). Similar as before, since spaCy requires the annotations to be in a specific .spacy format, we combined and transform these two JSON files into mod_annotations.spacy, which is what gets fed into the model during training.