![[deep-digit-classification.png]]

# Loss Function
Objective Function

- [[Back-Propagation]]
- Difference between predicted and target outputs
![[deep-loss-function.png]]

- Test accuracy worse than train accuracy = overfitting
- [[MLP|Dense]] = [[MLP|fully connected]]
- Automates feature engineering

![[ml-dl.png]]

These are the two essential characteristics of how deep learning learns from data: the incremental, layer-by-layer way in which increasingly complex representations are developed, and the fact that these intermediate incremental representations are learned jointly, each layer being updated to follow both the representational needs of the layer above and the needs of the layer below. Together, these two properties have made deep learning vastly more successful than previous approaches to machine learning.

# Steps
Structure defining
Compilation
- Loss function
	- Metric of difference between output and target
- Optimiser
	- How network will update
- Metrics to monitor
	- Testing and training
Data preprocess
- Reshape input frame into linear array
- Categorically encode labels
Fit
Predict
Evaluate

# Data Structure
- [[Tensor]] flow = channels last
	- (samples, height, width, channels)
- Vector data
	- 2D [[tensor]]s of shape (samples, features)   
- Time series data or sequence data
	- 3D [[tensor]]s of shape (samples, timesteps, features)   
- Images
	- 4D [[tensor]]s of shape (samples, height, width, channels) or (samples, channels, height, Width)
- Video
	- 5D [[tensor]]s of shape (samples, frames, height, width, channels) or (samples, frames, channels , height, width)

![[photo-tensor.png]]
![[matrix-dot-product.png]]