# Machine Learning Glossary
Machine Learning Glossary because it can get confusing between French and English words 


* Feature = Primitive

* Sample = exemple  = observations = vecteur de features 

* Classe 

* Régression 

* Classification 

# Speaker Recognition 
* **Definition**: is the task of recognizing the identify of a speaker through his voice. Considering the restrictions on the spoken text, speaker recognition can be classified into two categories, text-dependent and text-independent. [(Wang, Qian, & Yu, 2017)](#wang-qian2017)

* **State of the art history**
  * Gaussian Mixture Model-Universal Background Model with a maximum a posteriori (GMM-UBM-MAP) dominated for a long time since proposed in [(Reynolds, Quatieri, & Dunn, 2000)](#reynolds2000)


# Speaker Diarization

## Steps 

### 4 steps proposed in [(Bredin, 2017)](#bredin2017)

1. Voice activity detection, Speech Activity Detection (VAD or SAD) : L’entrée audio est découpée en segments d’un locuteur, et les sections ne contenant pas de voix sont supprimées.  
2. Speaker Change Detection (SCD) : Ces tours de paroles sont détectés et segmentés.
3. Speech Turn Clustering : Les différents tours de paroles sont regroupés en un « cluster » afin de regrouper ensemble un même locuteur 
4. Supervised Speaker Recognition (optionnelle) : Consiste à identifier le locuteur avec son identité.

### 4 steps proposed in [(Wang, Downey, Wan, Mansfield, & Moreno, 2017)](#wang2017)
1.	Speech Segmentation : Cette étape est équivalente à celle du « voice activity detection » proposée précédemment, découpant l’audio en segments contenant la voix d’un locuteur. 
2.	Audio Embedding Extraction » : Les « features » sont extraites des segments audio. 
3.	Clustering : Les segments audio sont regroupés pour pouvoir former des « cluster » identifiant les tours de parole pour un même locuteur. 
4.	Resegmentation (optionnelle) : Les résultats du « cluster » précédent sont améliorés pour pouvoir produire le résultat final pour la « diarization ». 


## Features 

Read [(Wang, Qian, & Yu, 2017)](#wang-qian2017) to understand what properties are encoded in the speaker embeddings i, d, s, and i-s.

* i-vectors : *Can encode the speaker identity to a large extent. GMM-UBM modelling on phonemes enables i-vector to encode the speech content, but the order of words cannot be encoded. Encode channel information.* 

* d-vectors : Neural networks based audio embeddings 

* s-vectors : *RNN/LSTM based sequence-vector. Refers to sequence-vector or summary-vector. Performs well on embedding the speech content and word order. Encode channel information.* (Wang, 2017)

* i-s-vectors : Proposed in [(Wang, Qian, & Yu, 2017)](#wang-qian2017)

## General Definitions 

* Embeddings : An embedding is a relatively low-dimensional space into which you can translate high-dimensional vectors. Embeddings make it easier to do machine learning on large inputs like sparse vectors representing words. Ideally, an embedding captures some of the semantics of the input by placing semantically similar inputs close together in the embedding space. ([Source](https://developers.google.com/machine-learning/crash-course/embeddings/video-lecture)) 

* Speaker Embeddings (Speaker Representation) : Used as features for a model.
  * i-vectors, d-vectors, s-vectors, i-s-vectors ...

* Audio embeddings : Captures in a low-dimensional space information in the audio

* Speaker Turn Embeddings 

* Enrollments 

* Trials 

* Affinity matrix 

* Similarity matrix 

* Utterances 

* Segments 

* Clustering methods 
  * Hierarchical Clustering
    * Agglomerative (Bottom-Up)
    * Divisive (Top-Down)
  * Affinity Propagation 

## Metrics 

* Diarization Error Rate (DER) 
  * Miss Rate: Also include errors coming from overlapping speech in the case of miss-detecting speakers [5].
  * False alarm rate: Also include errors coming from overlapping speech in the case of over-detecting speakers [5].
  * Speaker Error Rate:

* (EER)

# References

1. <a name="bredin2017"></a>Bredin, H. (2017). pyannote.metrics: A Toolkit for Reproducible Evaluation, Diagnostic, and Error Analysis of Speaker Diarization Systems. Dans Interspeech 2017 (pp. 3587‑3591). ISCA. https://doi.org/10.21437/Interspeech.2017-411

2. <a name="wang2017"></a>Wang, Q., Downey, C., Wan, L., Mansfield, P. A., & Moreno, I. L. (2017). Speaker Diarization with LSTM. arXiv:1710.10468 [cs, eess, stat]. Repéré à http://arxiv.org/abs/1710.10468

3. <a name="wang-qian2017"></a> Wang, S., Qian, Y., & Yu, K. (2017). What Does the Speaker Embedding Encode? Dans INTERSPEECH. https://doi.org/10.21437/Interspeech.2017-1125

4. <a name="reynolds2000"></a> Reynolds, D. A., Quatieri, T. F., & Dunn, R. B. (2000). Speaker verification using Adapted Gaussian mixture models. Dans Digital Signal Processing (p. 2000).

[5] Delgado Flores, H. (2015). Fast Cross-Session Speaker Diarization. Universitat Autonoma De Barcelona, Barcelone. Repéré à https://www.tdx.cat/bitstream/handle/10803/309290/hdf1de1.pdf?sequence=1&isAllowed=y


# Resources 

* [Google Machine Learning Glossary](https://developers.google.com/machine-learning/glossary/)
