<h2>Submission 2</h2>

Some changes were
- Deeper Generator model
- Dropout in Discriminator
- Smaller value for leaky ReLU
- One sided label smoothing for d_loss 

Things to improve: 
- Use placeholder for keep_prob instead. See this [link](https://stackoverflow.com/questions/44971349/how-to-turn-off-dropout-for-testing-in-tensorflow).
- Implement Xavier Initialization. [tf.contrib.layers.conv2d](https://www.tensorflow.org/api_docs/python/tf/contrib/layers/conv2d) has these input arguments:
```
conv2d(
    inputs,
    num_outputs,
    kernel_size,
    stride=1,
    padding='SAME',
    data_format=None,
    rate=1,
    activation_fn=tf.nn.relu,
    normalizer_fn=None,
    normalizer_params=None,
    weights_initializer=initializers.xavier_initializer(),
    weights_regularizer=None,
    biases_initializer=tf.zeros_initializer(),
    biases_regularizer=None,
    reuse=None,
    variables_collections=None,
    outputs_collections=None,
    trainable=True,
    scope=None
)
```
Thus by setting weights_initializer=initializers.xavier_initializer() I should be able to initialize the conv layers with Xavier initializer.
