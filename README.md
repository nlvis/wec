## Words of Estimative Correlation
### Supplementary Material

Analysis-related figures are generated from the 5 notebooks.
To re-run the processing, the CoreNLP server must be running.
Otherwise, it is enough to jump directly to *wec-analysis* and go from there. NLTK will likely require downloading many of its files separately.

**S1: study 1**  
**S2: study 2**

**Included files**:  
- *Notebooks*:  
    - **S1**: wec-process (NLP steps), wec-analysis (also include NLP methods), wec-visual (most paper figures come from here, plus others), tsne  
    - **S2**: wec-s2  
- *Raw data*:  
    - **S1**: WEC-160.xslx  
 	- **S2**: weca-120.xslx  
- *Pickled processed data (so that wec-process can also be skipped, and the second one allows jumping directly to wec-visual)*:
    - WECdf.pkl
    - WECdf-categorised.pkl
- *Lexicons*:
    - lex-adjective.csv
    - lex-adverb.csv
    - lex-noun.csv
    - lex-verb.csv
- *Scales*:
    - dirscale.csv
    - dis_scale.csv
    - magscale.csv
    - pscale.csv
    - regscale.csv

**Key libraries required**

- Pandas
- Numpy
- Altair
- nltk
- tabulate (optional)
- gensim (for the pre-processing of the intensity order, only used with sklearn in tsne.ipynb)
- sklearn (for tsne.ipynb -- not required for the bulk of the analysis)

**Required Server for Processing**
- CoreNLP server: https://stanfordnlp.github.io/CoreNLP/

**Required extra file**
- Intensity-ordered word embeddings, downloaded from  [1], converted using gensim: 
    ```
    from gensim.scripts.glove2word2vec import glove2word2vec 
    
    glove2word2vec("glove_vectors_syn_ant.txt", "w2v_synant.txt")
    ```


    
[1] J.-K. Kim, M.-C. de Marneffe, and E. Fosler-Lussier, “Adjusting Word Embeddings with Semantic Intensity Orders,” pp. 62–69, 2016.
