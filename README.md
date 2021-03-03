# DSG
Directional Skip-Gram: Explicitly Distinguishing Left and Right Context for Word Embeddings

To build the code, simply run:

make

The command to build word embeddings is exactly the same as in the original version, except that we removed the argument -cbow and replaced it with the argument -type:

./dsg -train input_file -output embedding_file -type 0 -size 50 -window 5 -negative 10 -hs 0 -sample 1e-4 -threads 1 -binary 1 -iter 5

The -type argument is a integer that defines the architecture to use. These are the possible parameters:  
0 - dsg: the model proposed in this paper;
1 - simple ssg: the comparative model adopted from the original structured SG model (https://github.com/wlin12/wang2vec).


If you use functionalities in this code, please support us by citing our paper:

@InProceedings{Song:2018:naacl,
author    = {Yan Song and Shuming Shi and Jing Li and Haisong Zhang},
title     = "{Directional Skip-Gram: Explicitly Distinguishing Left and Right Context for Word Embeddings}",
booktitle = {Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies},
year      = {2018},
publisher = {Association for Computational Linguistics},
address   = {New Orleans, Louisiana, USA}
}

Many thanks!
