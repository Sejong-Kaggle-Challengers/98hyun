#### 기초
 
punctuation : 구두점. . , ? ; ! 이런거.   
from tensorflow.keras.preprocessing.text import text_to_word_sequence : keras tokenize 어퍼스트로피 살린다.   
corpus : ?  
stopwords : 불용어 조사, 접미사등 문장에 자주 등장하지만 없어도 괜찮은.  
lemmatization : 표제어 추출. 단어의 개수를 줄이는  
stemming : 어간 추출. 위 둘은 단어의 빈도수를 기반으로 문제를 풀때 사용.

#### 토큰화에서 주의할점.

구두점이나 특수 문자를 단순 제외해서는 안 된다.  
줄임말과 단어 내에 띄어쓰기가 있는 경우.  

from nltk.tokenize import TreebankWordTokenizer

#### 문장의 토큰화

(영어) from nltk.tokenize import sent_tokenize  
(한글) import kss  
https://www.grammarly.com/blog/engineering/how-to-split-sentences/

#### 정규화

대, 소문자 통합 (예외 US us)  
규칙에 기반한 표기가 다른 단어들의 통합 (USA와 US)    
불필요한 단어의 제거   
  
등장 빈도가 적은 단어  
길이가 짧은 단어 (영어평균 6~7, 한글 2~3)  
### 참고 

https://wikidocs.net/21698

https://www.kaggle.com/awesomehidingspot/my-first-kaggle-nlp-notebook

https://www.kaggle.com/skrcode/0-29-public-lb-score-beginner-nlp-tutorial

https://www.kaggle.com/sudalairajkumar/simple-feature-engg-notebook-spooky-author