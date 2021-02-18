### baseline 

dacon이 올려놓은 lstm 

### baseline + batchnormalization , dropout

일단, val_loss 가 0.5에서 멈췄다. 코드공유에서 data가 적기 때문에 과적합이 일어날수있다고 했다.  
batchnormalization 과 dropout을 사용해봤지만, 소용없었다.

### data augment + conv1d + lstm

같은 코드가 나와서 공부했다.  

data augment 후, conv1d layer를 통해 filter를 늘렸고, 마지막에 lstm 을 합쳐놓음으로써 시계열 특성또한 살려봤다.  