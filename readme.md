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