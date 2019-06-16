# machine-learning-glossary
Machine Learning Glossary because it can get confusing between French and English words 


* Feature = Primitive

* Sample = exemple  = observations = vecteur de features 

* Classe 

* Régression 

* Classification 


# Speaker Diarization

## Steps 

### 4 steps proposed in [(Bredin, 2017)](#bredin2017)

1.	« Voice activity detection » : L’entrée audio est découpée en segments d’un locuteur, et les sections ne contenant pas de voix sont supprimées.  
2.	« Speaker Change Detection » : Ces tours de paroles sont détectés et segmentés.
3.	« Speech Turn Clustering » : Les différents tours de paroles sont regroupés en un « cluster » afin de regrouper ensemble un même locuteur 
4.	« Supervised Speaker Recognition » (optionnelle) : Consiste à identifier le locuteur avec son identité.


## Features 

* i-vectors

* d-vectors 

* i-s-vectors

# References

* <a name="bredin2017"></a>Bredin, H. (2017). pyannote.metrics: A Toolkit for Reproducible Evaluation, Diagnostic, and Error Analysis of Speaker Diarization Systems. Dans Interspeech 2017 (pp. 3587‑3591). ISCA. https://doi.org/10.21437/Interspeech.2017-411
