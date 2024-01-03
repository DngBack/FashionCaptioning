# **Automate Fashion Image Captioning using BLIP-2** # 

## Problems Description 

Given the clothes image provide a short caption that describes the item. In general, in image captioning datasets (e.g., COCO, Fliker), the descriptions of fashion items have three unique features, which makes the automatic generation of captions a challenging task. First, fashion captioning needs to describe the attributes of an item, while image captioning generally narrates the objects and their relations in the image.
e.g. image where the model is wearing a shirt, the general caption model describes such images as "male wearing a white shirt". This is incorrect since we want the model to describe the item. In this application, it is much more important to have a performant to caption the image than an interpretable model.

## Solution 

Using BLIP-2 to solve this problems

## Requirements

Refer requirements.txt

## Dataset 

FAshion CAptioning Dataset (FACAD), the fashion captioning dataset consisting of over 993K images.

Properties of FACAD dataset:

Diverse fashion images of all four seasons, ages (kids and adults), categories (clothing, shoes, bag, accessories, etc.), angles of a human body (front, back, side, etc.).
It tackles the captioning problem for fashion items.
FACAD contains fine-grained descriptions of attributes of fashion-related items, while MS COCO narrates the objects and their relations in general images. FACAD has longer captions (21 words per sentence on average) compared with the 10.4 words per sentence of the MS COCO caption dataset
Expression style of FACAD is enchanting, while that of MS COCO is plain without rich expressions. e.g. words like "pearly", "so-simple yet so-chic", and "retro flair" are more attractive than the plain MS COCO descriptions, like "person in a dress".

## Technique


## Metric

Most commonly used metric for image caption task, that is used to measuring the quality of an predict text based on reference texts are:

1. <b>B</b>i<b>l</b>ingual <b>E</b>valuation <b>U</b>nderstudy (<i>Bleu</i>) Score: a concept build on precision.

        Bleu = Number of correct predicted words / Number of total predicted words

2. <b>R</b>ecall-<b>O</b>riented <b>U</b>nderstudy for <b>G</b>isting <b>E</b>valuation (<i>ROUGE</i>) Score: a set of metrics, rather than just one. ROUGE metric return recall, precision and f1-score. In our project have use F1-Rouge score. It's concept build on recall.

        Recall-N-gram = Number of correct predicted n-grams / Number of total target N-grams

        Precision-N-gram = Number of correct predicted n-grams / Number of total predict N-grams

        F1-Score = 2* ((Recall-N-gram * Precision-N-gram) / (Recall-N-gram + Precision-N-gram))


Both these score are build on concept of N-gram. In n-gram the value of n, is group n words and these words will always be in order. For this project have consider the value on n = 2. </br>
Because caption of the fashion item are the attributes, it does not matter in which order the model predits those attributes words.