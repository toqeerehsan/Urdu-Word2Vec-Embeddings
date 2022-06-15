# Urdu Word2Vec Embeddings

Word2Vec embeddings are trained on a plain Urdu corpus of 220 million tokens. The respository contains the trained embeddings with dimenstion size of 100, 200 and 300. Both binary (.bin) and non-binary trained models are included.

**Usage**
```
import gensim
from gensim.models import Word2Vec
```
**Load an existing model**
```
model = gensim.models.Word2Vec.load("Urdu_Word2Vec/urdu_220m_wv_100d", binary=False)
```
**or**
```
model = gensim.models.Word2Vec.load("Urdu_Word2Vec/urdu_220m_wv_100d.bin", binary=True)
```
**Extract a list of similar words against the given word**
```
for i in model.wv.most_similar([u'گھر']): print( i[0])
```
**Vocabulary**
```
vocabulary = model.wv.vocab
```
**Citation**

If you use Urdu Word2Vec embeddings in your research word then please cite the following paper:
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
