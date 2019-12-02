# D2T
 Text generation from structured data
 
## This is the project for automatically generating text summary given NBA game box-score.

## Requirements
1. Python 3.6
2. PyTorch 0.2


## Data set
We use Rotowire dataset for training as in Challenges in Data-to-Document Generation (Wiseman, Shieber, Rush; EMNLP 2017). This dataset consists of (human-written) NBA basketball game summaries aligned with their corresponding box- and line-scores.

## Basic Usage
Data:
Rotowire data Can be found in folder Data/ rotowire.tar.bz2

To Extract:

filename='rotowire.tar.bz2'

import tarfile

tar= tarfile.open(filename,mode='r')

tar.extractall()

tar.close()


## Train
In train/ directory is the part of data2text generation. The files are for this part include:
* dataprepare.py -- word2index map class, storing the vocabulary and relations
* model.py -- The file that contains the implementation of several encoder, decoder and embedding model class
* preprocessing.py -- mainly for read of parse the data
* train.py -- the file that defines the training processes
* util.py -- utility functions for time, showing etc.
* setting.py -- store the hyper-parameter, file location etc.
* train1.py- Contains model_initialization

Some pre-trained model files could be found [here](https://drive.google.com/drive/folders/12qjIVSknhQkjaHZn77HauvZDA0CfAVwG/). 

To Evaluate: 

* small_evaluate.py – Generating some text

Some output files can be found [here]( https://drive.google.com/drive/folders/16ECazJxJbOEaVjrAXVrQ53VkigftQkFY?usp=sharing/). 

* Jupyter Notebook- Result_run.ipynb

## References: Thanks to the dataset and code from Wiseman et. al.s
Data Source: https://github.com/harvardnlp/boxscore-data
https://github.com/harvardnlp/data2text
Papers Referred: 
- Matulík, M. (2019). Natural Language Generation From Structured Data. [ebook] Prague. Available at: https://dspace.cvut.cz/bitstream/handle/10467/77082/F3-DP-2018-Matulik-Martin-natural_language_generation_from_structured_data.pdf?sequence=-1&isAllowed=y
- Shieber, S. (2019). [online] Eecs.harvard.edu. Available at: http://www.eecs.harvard.edu/~shieber/Biblio/shieber-cv.pdf   [Accessed 11 Oct. 2019].
- Cao, J., Gong, J. and Zhang, P. (2019). Open-Domain Table-to-Text Generation based on Seq2seq. [online] Semanticscholar.org. Available at: https://www.semanticscholar.org/paper/Open-Domain-Table-to-Text-Generation-based-on-Cao-Gong/c5e95459c2cc5c25789e76abeefebd52fda8190e
- Arxiv.org. (2019). [online] Available at: https://arxiv.org/pdf/1711.09724.pdf
- Aclweb.org. (2019). [online] Available at: https://www.aclweb.org/anthology/W08-1104.pdf
- Aclweb.org. (2019). [online] Available at: https://www.aclweb.org/anthology/W14-4401.pdf 



