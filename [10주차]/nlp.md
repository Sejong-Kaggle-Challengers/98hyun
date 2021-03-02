#### 기초
 
punctuation : 구두점. . , ? ; ! 이런거.   
from tensorflow.keras.preprocessing.text import text_to_word_sequence : keras tokenize 어퍼스트로피 살린다.   
corpus : ?  
stopwords : 불용어 조사, 접미사등 문장에 자주 등장하지만 없어도 괜찮은.  
lemmatization : 표제어 추출. 단어의 개수를 줄이는  
stemming : 어간 추출. 위 둘은 단어의 빈도수를 기반으로 문제를 풀때 사용.  
bow(bag of word) : 나누고 단어 등장 횟수 카운트하는거. sklearn CountVectorizer 로 가능.  

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

#### tf-idf 

tf : 단어빈도. 많이 등장하면 중요한 단어.  
df : 문서빈도. 많이 등장하면 흔한 단어. idf는 역수값.  
tf-idf : 통계적 수치들을 곱한 값.  

#### 나이브 베이즈

조건부 독립 : [참고](https://velog.io/@otter275/%EC%A1%B0%EA%B1%B4%EB%B6%80-%EB%8F%85%EB%A6%BD%EA%B3%BC-%EB%AC%B4%EC%A1%B0%EA%B1%B4%EB%B6%80-%EB%8F%85%EB%A6%BD%EC%9D%98-%EA%B4%80%EA%B3%84)

나이브 가정 : 모든 개별 변수가 조건부 독립이다.  

#### 그 외 용어

ETA : Estimated Time of Arrival 뭔가 마치는 예상 시간  

#### xgb로 접근 했을 때의 feature extraction
| feature_name | description |
|---------------|------------------|
|num_words | 구두점뺀 단어들의 수. |  
|mean_word_len | 단어 길이의 평균 |
|num_unique_words| unique한 단어의 수.|
|num_chars| text의 길이|
|num_stopwords| stopwords의 수.|
|num_punctuations | punctuations의 수. |
|num_words_upper| 대문자수 비율|
|num_words_title| 단어의 앞이 대문자인 수 비율|
|chars_between_comma| , 사이의 단어(문장)길이의 평균|
|symbols_unknowns| 이상한 단어 비율 |
|noun,adj,verbs,| 동사,부사,동사 이런거.|
|sentiment| 감성분석? (사전에 정의되어있는듯하다.)|
|single_frac| 1인칭,3인칭 그런 비율|
|plural_frac| 2인칭 그런 비율|
|first_word_len| 첫번째 단어의 글자수 비율?|
|last_word_len| 마지막 단어의 글자수 비율|
|ease| 어떤 점수가 나온다. |
|get_persons|여러 nltk의 방법들이 나오는데 정확히 어떤 역할을 하는지 모름.|
|sent2vec| fasttext를 이용한 예측값 변수|

#### 블렌딩

예측값을 변수로 활용하는것. 대신 validation set의 예측을 사용.  
스태킹이랑 다른점은 스태킹은 train set의 예측만을 사용.   
쉽게말해 다른 모델들의 예측값만을 활용해 새로운 모델을 따는 방법.    
블렌딩은 기존의 변수들과 함께 여러모델들의 예측값들을 변수로 활용하여 예측하는 방법.  


#### 참고 

https://wikidocs.net/21698

https://www.kaggle.com/jhotor/spooky-classification-albert