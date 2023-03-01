# Neural Network Example
3학년 2학기 인공지능 실습

neural network example using Back Propagation. you can change number of hidden units , number of epochs by using TrainNN(num_hiddens, eps, momentum, num_epochs). 

## Digits(digit.npz)
contains 6 sets(train2, train3, valid2, valid3, test2, test3) of  16x 16 greyscale images in vector format. (the images contain centered, handwritten 2's and 3's, scanned from postal envelopes.)

 * train : 300 examples of each digit(stored as 256 x 300 matrices)
 * valid : 100 examples of each digit
 * test : 200 examples of each digit

## How to run
```shell
pip install numpy
pip install matplotlib
python nn.py
```

## Result Analysis

### Number of Epochs

![img](/analysis-image/epoch-analysis-1.png) ![img](/analysis-image/epoch-analysis-2.png)

Epochs 이 많아지면 train 은 점점 수렴하지만 Validation 은 오히려 좋지 않아지는 overfitting 이 일어날 수 있다. 결과로 볼 수 있듯이 3000 에 가까워지자 Validation 이 증가하고 있다. 이는 콘솔 log 를 보면 알 수 있는데 2800 이 되자 Validation 의 Cross Entropy 가 감소를 멈추고 증가하고 있음을 알 수 있다. 따라서 적정 Epochs 수는 2800 이다.

### Number of Hidden units
![img](/analysis-image/hidden-unit-analysis-1.png)

Hidden unit 의 수가 적을수록 감소가 느리다는 것을 알 수 있다.

![img](/analysis-image/hidden-unit-analysis-2.png)

특히 시작점에서 눈에 띄게 드러나는데 hidden unit 이 많은 경우는 처음부터 entropy 의 감소가 눈에 띄지만 hidden unit 이 적은 2, 5 의 경우는 느리게 감소하고 있다.


![img](/analysis-image/hidden-unit-analysis-3.png)

Epoch 수가 높아져 수렴에 가까워지면 Cross Entropy 는 평행하게 내려가고 있다. Hidden
unit 이 많으면 조금이라도 더 성능이 좋을 것 같지만, hidden unit 이 적은 경우 더 빠른 시간
안에 학습 시킬 수 있으므로 유리할 것이다.