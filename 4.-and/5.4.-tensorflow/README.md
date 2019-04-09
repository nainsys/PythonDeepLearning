# 5.4.    Keras를 사용한 학습

가장 유명한 딥러닝 라이브러리는 텐서플로와 케라스를 들수 있습니다. 이번 챕터에서는 케라스의 사용법을 설명하겠습니다.

다음은 간단한 XOR 문제를 학습하는 코드를 비교한 것인데 함수 사용에 있어서 큰 차이가 있음을 알 수 있습니다.

source: [https://gist.github.com/cburgdorf/e2fb46e5ad61ed7b9a29029c5cc30134](https://gist.github.com/cburgdorf/e2fb46e5ad61ed7b9a29029c5cc30134)

[**xor\_keras.py**](https://gist.github.com/cburgdorf/e2fb46e5ad61ed7b9a29029c5cc30134#file-xor_keras-py)

```python
import numpy as np
from keras.models import Sequential
from keras.layers.core import Activation, Dense
training_data = np.array([[0,0],[0,1],[1,0],[1,1]], "float32")
target_data = np.array([[0],[1],[1],[0]], "float32")
model = Sequential()
model.add(Dense(32, input_dim=2, activation='relu'))
model.add(Dense(1, activation='sigmoid'))
model.compile(loss='mean_squared_error', optimizer='adam', metrics=['binary_accuracy'])
model.fit(training_data, target_data, nb_epoch=1000, verbose=2)
print model.predict(training_data)
```

[**xor\_tensorflow.py**](https://gist.github.com/cburgdorf/e2fb46e5ad61ed7b9a29029c5cc30134#file-xor_tensorflow-py)

```python
import tensorflow as tf   
input_data = [[0., 0.], [0., 1.], [1., 0.], [1., 1.]]  # XOR input
output_data = [[0.], [1.], [1.], [0.]]  # XOR output
n_input = tf.placeholder(tf.float32, shape=[None, 2], name="n_input")
n_output = tf.placeholder(tf.float32, shape=[None, 1], name="n_output")
hidden_nodes = 5
b_hidden = tf.Variable(tf.random_normal([hidden_nodes]), name="hidden_bias")
W_hidden = tf.Variable(tf.random_normal([2, hidden_nodes]), name="hidden_weights")
hidden = tf.sigmoid(tf.matmul(n_input, W_hidden) + b_hidden)
W_output = tf.Variable(tf.random_normal([hidden_nodes, 1]), name="output_weights")  # output layer's weight matrix
output = tf.sigmoid(tf.matmul(hidden, W_output))  # calc output layer's activation
cross_entropy = tf.square(n_output - output)  # simpler, but also works
loss = tf.reduce_mean(cross_entropy)  # mean the cross_entropy
optimizer = tf.train.AdamOptimizer(0.01)  # take a gradient descent for optimizing with a "stepsize" of 0.1
train = optimizer.minimize(loss)  # let the optimizer train
init = tf.initialize_all_variables()
sess = tf.Session()  # create the session and therefore the graph
sess.run(init)  # initialize all variables 
for epoch in xrange(0, 2001):
    # run the training operation
    cvalues = sess.run([train, loss, W_hidden, b_hidden, W_output],
                       feed_dict={n_input: input_data, n_output: output_data})
    if epoch % 200 == 0:
        print("")
        print("step: {:>3}".format(epoch))
        print("loss: {}".format(cvalues[1]))
print("")
print("input: {} | output: {}".format(input_data[0], sess.run(output, feed_dict={n_input: [input_data[0]]})))
print("input: {} | output: {}".format(input_data[1], sess.run(output, feed_dict={n_input: [input_data[1]]})))
print("input: {} | output: {}".format(input_data[2], sess.run(output, feed_dict={n_input: [input_data[2]]})))
print("input: {} | output: {}".format(input_data[3], sess.run(output, feed_dict={n_input: [input_data[3]]})))
```

케라스는 model 인스턴스를 생성하고 그 위에 add로 하나씩 레이어를 쌓습니다. 그리고 compile로 오차계산\(loss\)과 학습방법\(optimizer\)을 결정하고, 마지막으로 fit을 사용해 데이터를 입력하여 학습을 시작합니다.

이에 반해서 텐서플로는 신경망의 가중치\(w\)와 편향\(b\) 변수를 직접 선언하고 tf.matmul로 행렬계산을 하는 코드를 작성해야 합니다. 특히 행렬의 입력과 출력의 개수를 정확히 맞춰줘야 하는데 케라스는 이런 과정을 자동으로 수행합니다.

확실히 케라스가 좀 더 직관적이고 사용하기가 간단합니다. 하지만 텐서플로는 구글이라는 브랜드 파워가 있고 사용자가 훨씬 많아서 예제를 찾거나 질문하기가 수월하다는 장점이 있습니다. 자신의 사용 목적에 따라서 어떤 라이브러리를 사용할 지 결정하는 게 좋을 것 같습니다.



