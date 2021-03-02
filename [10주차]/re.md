#### 정규표현식 

1. 일대일매칭
2. 12가지 메타문자 `$()*+.?[\^{|` \와 쓰인다.

match vs search 

match는 앞에서부터 search는 어디든서부터 대신 둘다 하나씩만. match object를 반환. 사용하기 힘듦. 

match object 

obj.group() : 일치된 문자열 반환.
obj.span() : 시작위치,끝위치 반환.  
obj.start(), obj.end() : 시작,끝 반환.  

findall 

모든 것을 찾고 리스트로 반환. 사용감 좋다.

[] : or. 딱 하나와 매칭. -(하이픈) 범위. [A-Za-z0-9가-힣] 사용. 
\, ^, -, ] 대괄호 안 semi-메타문자 [a-z-[g-z]] 도 가능.

#### 참고 

https://greeksharifa.github.io/%EC%A0%95%EA%B7%9C%ED%91%9C%ED%98%84%EC%8B%9D(re)/2018/07/21/regex-usage-02-basic/

https://youtu.be/yQ20jZwDjTE