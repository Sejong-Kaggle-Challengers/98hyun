### baseline 

dacon이 올려놓은 lstm 

### baseline + batchnormalization , dropout

일단, val_loss 가 0.5에서 멈췄다. 코드공유에서 data가 적기 때문에 과적합이 일어날수있다고 했다.  
batchnormalization 과 dropout을 사용해봤지만, 소용없었다.

### data augment + conv1d + lstm

같은 코드가 나와서 공부했다.  

data augment 후, conv1d layer를 통해 filter를 늘렸고, 마지막에 lstm 을 합쳐놓음으로써 시계열 특성또한 살려봤다.  

### activation change + full connection layers 

activation을 relu에서 elu로 바꿔봤다. elu가 잘 먹힌다고 들었고, 값 중에 마이너스도 있기때문에 minus또한 gradient로 약하게나마 넘기기 위해서이다. 이렇게 이해한게 맞나 싶다. 

또, dense층을 늘려 dropout으로 일반화를 시도 했다. 성능은 조금 좋아졌다. 