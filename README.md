# Urdu Word2Vec Embeddings

Word2Vec embeddings are trained on a plain Urdu corpus of 220 million tokens. The respository contains the trained embeddings with dimenstion size of 100, 200 and 300. The vocabulary size is 125,622. 

**Download**

Urdu Word2Vec 100 Dimensions [urdu_220m_wv_100d.bin](https://drive.google.com/file/d/1fD-fmS2-CUWtKrly-GzSahCnAbZzgdhr/view?usp=sharing)</br>
Urdu Word2Vec 200 Dimensions [urdu_220m_wv_200d.bin](https://drive.google.com/file/d/1n5IxP-pl3u8Wd1lwZCHtZtCOkFnesAFX/view?usp=sharing)</br>
Urdu Word2Vec 300 Dimensions [urdu_220m_wv_300d.bin](https://drive.google.com/file/d/1laonsl3fx9YP-mCQdM2382qkjQalLFCH/view?usp=sharing)

**Usage**
```
import gensim
from gensim.models import Word2Vec
```
**Load a pre-trained model**
```
model = gensim.models.Word2Vec.load("urdu_220m_wv_100d.bin", binary=True)
```
**Extract a list of similar words against the given word**
```
for i in model.wv.most_similar([u'گھر']): print( i[0])
```
**Vocabulary**
```
vocabulary = model.wv.vocab # Vocabulary size is 125,622
```
**Citation**

If you use Urdu Word2Vec embeddings in your research then please cite the following paper:
```
@article{ehsan2021improving,
  title={Improving Phrase Chunking by using Contextualized Word Embeddings for a Morphologically Rich Language},
  author={Ehsan, Toqeer and Khalid, Javairia and Ambreen, Saadia and Mustafa, Asad and Hussain, Sarmad},
  journal={Arabian Journal for Science and Engineering},
  pages={1--19},
  year={2021},
  publisher={Springer}
}
```
