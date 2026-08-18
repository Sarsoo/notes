---
onenote-id: 0-95ce6262339806ad0eebd01772655904!1-D084F068F621FF9!3714
---
Eager
 
- Not run as graphs
- Run in python
	- With python data structures

```python
# Fetch and format the mnist data
(mnist_images, mnist_labels), _ = tf.keras.datasets.mnist.load_data()

dataset = tf.data.Dataset.from_tensor_slices(
	(tf.cast(mnist_images[...,tf.newaxis]/255, tf.float32), 
	tf.cast(mnist_labels, tf.int64)))

dataset = dataset.shuffle(1000).batch(32)
```

```python
# Build the model
mnist_model = tf.keras.Sequential([
	tf.keras.layers.Conv2D(16,[3,3], activation='relu’,
							input_shape=(None, None, 1)),
	tf.keras.layers.Conv2D(16,[3,3], activation='relu’),
	tf.keras.layers.GlobalAveragePooling2D(),
	tf.keras.layers.Dense(10)
])
```

```python
for images, labels in dataset.take(1):
	print("Logits: ", mnist_model(images[0:1]).numpy())
```

```python
optimizer = tf.keras.optimizers.Adam()
loss_object = tf.keras.losses.SparseCategoricalCrossentropy(from_logits=True)

loss_history = []
```

```python
def train_step(images, labels):
	with tf.GradientTape() as tape:
		logits = mnist_model(images, training=True)
		
		# Add asserts to check the shape of the output.
		tf.debugging.assert_equal(logits.shape, (32, 10))
		
		loss_value = loss_object(labels, logits)
		
	loss_history.append(1oss_value.numpy().mean())
	grads = tape.gradient(loss_value, mnist_model.trainable_variables)
	optimizer.apply_gradients(zip(grads, mnist_model.trainable_variables))
```

```python
def train(epochs):
	for epoch in range(epochs):
		for (batch, (images, labels)) in enumerate(dataset):
			train_step(images, labels)
		print (‘Epoch {} finished’.format(epoch))
```

```python
class Linear(tf.keras.Model) :
	def __init__(self):
		super(Linear, self).__init__()
		self.W = tf.Variable(5., name='weight' )
		self.B = tf.Variable(19., name='bias')
	def call(self, inputs) :
		return inputs * self.W + self.B


# A toy dataset of points around 3 * x +2
NUM_EXAMPLES = 2000

training_inputs = tf.random.normal([NUM_EXAMPLES])
noise = tf.random.normal ([NUM_EXAMPLES])
training_outputs = training_inputs * 3 + 2 + noise

# The loss function to be optimized
def loss(model, inputs, targets):
	error = model(inputs) - targets
	return tf.reduce_mean(tf.square(error))

def grad(model, inputs, targets):
	with tf.GradientTape() as tape:
		loss_value = loss(model, inputs, targets)
	return tape.gradient(loss_value, [model.W, model.B])
```

```python
model = Linear()
optimizer = tf.keras.optimizers.SGD(learning_rate=0.01)

print("Initial loss: {:.3f}".format(loss(model, training_inputs, training_outputs)))

steps = 300
for i in range(steps):
	grads = grad(model, training_inputs, training_outputs)
	optimizer apply_gradients(zip(grads, [model.W, model.B]))
	if 1% 20 == 0:
		print("Loss at step {:@3d}: {:.3f}".format(i, loss(model, training_inputs, training_outputs)))
```

hidden_nodes = [2, 8, 16]  
epochs = [1, 2, 4, 8]
 
Eagerly = false  
8.33 s ± 608 ms per loop (mean ± std. dev. of 7 runs, 1 loop each)
 
Eagerly=true  
8.31 s ± 18.3 ms per loop (mean ± std. dev. of 7 runs, 1 loop each)

hidden_nodes = [2, 8, 16, 24, 32]  
epochs = [1, 2, 4, 8, 16, 32, 64, 100, 150, 200]
 
Eagerly = false  
3min 20s ± 7.8 s per loop (mean ± std. dev. of 7 runs, 2 loops each)
 
Eagerly=true
 
[How to Use The Pre-Trained VGG Model to Classify Objects in Photographs](https://machinelearningmastery.com/use-pre-trained-vgg-model-classify-objects-photographs/)