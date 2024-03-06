# Gemma-PET
Parameter efficient tuning - LoRA

This notebook illustrates how to create a customised text classifier using parameter efficient tuning (PET). Instead of fine-tuning the whole model, PET methods update only a small amount of parameters, which makes it relatively easy and fast to train. It also makes it easier for a model to learn new behaviors with relatively little training data.

This notebook uses the LoRA PET method and the smaller Gemma model (gemma_instruct_2b_en) since that can be run faster and more efficiently.

The colab covers the steps of ingesting data, formatting it for the LLM, training LoRA weights, and then evaluating the results. 
This notebook trains on the ETHOS dataset, a publicly available dataset for detecting hateful speech, built from YouTube and Reddit comments. 
When trained on only 200 examples (1/4 of the dataset) it achieves F1: 0.80 and ROC-AUC: 0.78, slightly above the SOTA currently reported on the 
leaderboard (at the time of writing, 15 Feb 2024). When trained on the full 800 examples, like it achieves an F1 score of 83.74 and a ROC-AUC score of 88.17.
