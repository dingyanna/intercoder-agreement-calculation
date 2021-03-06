# intercoder-agreement-calculation

## Table of Contents
### Examples
  
  1. [Cohen's Kappa](#1)
  2. [weighted Kappa](#2)
  3. [multi-label Kappa](#3)
  4. [Krippendorff's Alpha](#4)
  5. [percentage agreement](#5)
  6. [Scott's Pi](#6)
  7. [Fleiss' Kappa](#7)


<a name="ex"></a>
## Examples

<a name="1"></a>
### 1. calculate Cohen's Kappa
usage:
```console
python3 cohen_kappa.py [-h] <data-file>
```
```console
$ python3 cohen_kappa.py ./data/data0.csv
Cohen's Kappa: 0.6899266046058918
```


<a name="2"></a>
### 2. calculate weighted Kappa
usage:
```console
python3 weighted_kappa.py [-h] <data-file> <weights-file>
```   
```console
$ python3 weighted_kappa.py ./data/data1.csv ./data/weights1.txt
Weighted Kappa: 0.7490712511745773
```

```console
$ python3 weighted_kappa.py ./data/data2.csv ./data/weights2.txt
Weighted Kappa: 0.2902183212395829
```



<a name="3"></a>
### 3. calculate Kappa with multiple labels
usage:
```console
python3 multilabel_kappa.py [-h] <data-file>
``` 
```console
$ python3 multilabel_kappa.py ./data/data3.csv
Weighted Kappa: 0.7234810951760119
```




<a name="4"></a>
### 4. calculate Krippendorff's Alpha
usage:
```console
python3 krippendorff_alpha.py [-h] [-w WEIGHTS] {nominal,ordinal} data
```            
```console
$ python3 krippendorff_alpha.py nominal ./data/data1.csv 
Krippendorff's alpha for nominal metric: 0.6722775059943613
```
```console
$ python3 krippendorff_alpha.py ordinal ./data/data2.csv -w ./data/weights2.txt
Krippendorff's alpha for ordinal metric: 0.3136278980049674
```




<a name="5"></a>
### 5. calculate percentage agreement
usage:
```console
python3 percentage_agreement.py [-h] {weighted,unweighted} data weights
```                                                                                                  
```console
$ python3 percentage_agreement.py unweighted ./data/data1.csv ./data/weights1.txt
Percentage Agreement: 0.8070866141732284
```
```console
$ python3 percentage_agreement.py unweighted ./data/data2.csv ./data/weights2.txt 
Percentage Agreement: 0.39
```
```console
$ python3 percentage_agreement.py weighted ./data/data1.csv ./data/weights1.txt
Weighted Percentage Agreement: 0.9247594050743658
```
```console
$ python3 percentage_agreement.py weighted ./data/data2.csv ./data/weights2.txt
Weighted Percentage Agreement: 0.72
```



<a name="6"></a>
### 6. calculate Scott's Pi
```console
python3 scott_pi.py [-h] [-w WEIGHTS] data
```
```console
$ python3 scott_pi.py ./data/data1.csv  
Scott's Pi for nominal metric: 0.6720637639154207
```
```console
$ python3 scott_pi.py ./data/data2.csv
Scott's Pi for nominal metric: 0.21741884529188435
```
```console
$ python3 scott_pi.py -w ./data/weights1.txt ./data/data1.csv
ScoScott's Pi for ordinal metric: 0.7495375634891718
```
```console
$ python3 scott_pi.py -w ./data/weights2.txt ./data/data2.csv 
Scott's Pi for ordinal metric: 0.28940209848442794
```


<a name="7"></a>
### 7. calculate Fleiss' Kappa
usage:
```console
python3 fleiss_kappa.py [-h] [-w WEIGHTS] data categories
```
```console
$ python3 fleiss_kappa.py ./data/data1.csv ./data/categories1.txt
Fleiss' Kappa for nominal metric: 0.6720623237921253
```
```console
$ python3 fleiss_kappa.py ./data/data2.csv ./data/categories2.txt
Fleiss' Kappa for nominal metric: 0.21741884529188435
```

```console
$ python3 fleiss_kappa.py -w ./data/weights1.txt ./data/data1.csv ./data/categories1.txt
Fleiss' Kappa for ordinal metric: 0.7484205260779706
```
```console
$ python3 fleiss_kappa.py -w ./data/weights2.txt ./data/data2.csv ./data/categories2.txt
Fleiss' Kappa for ordinal metric: 0.28940209848442794
```


