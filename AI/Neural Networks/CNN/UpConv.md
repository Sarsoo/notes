- Fractionally strided convolution
- Transposed [Convolution](../../../Signal%20Proc/Convolution.md)
	- Like a deep interpolation
- Convolution with a fractional input stride
- Up-sampling is convolution 'in reverse'
	- Not an actual inverse convolution
- For scaling up by a factor of $f$
	- Consider as a [Convolution](../../../Signal%20Proc/Convolution.md) of stride $1/f$
- Could specify kernel
	- Or learn
- Can have multiple upconv layers
	- Separated by [ReLu](../Activation%20Functions.md#ReLu)
	- For non-linear up-sampling conv
	- Interpolation is linear

![upconv](../../../img/upconv.png)

# Convolution Matrix
Normal

![upconv-matrix](../../../img/upconv-matrix.png)

- Equivalent operation with a flattened input
	- Row per kernel location
- Many-to-one operation

![upconv-matrix-result](../../../img/upconv-matrix-result.png)

[Understanding transposed convolutions](https://www.machinecurve.com/index.php/2019/09/29/understanding-transposed-convolutions/)

## Transposed
![upconv-transposed-matrix](../../../img/upconv-transposed-matrix.png)
- One-to-many

![upconv-matrix-transposed-result](../../../img/upconv-matrix-transposed-result.png)