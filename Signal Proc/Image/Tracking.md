# Challenges
- Clutter
	- Distractors
- Occlusion
	- Hidden by other objects

- Objects appearance can evolve
	- Rotation, scale, camera viewpoint
- Take new template every n frames
- Take new template when confidence falls below threshold

# Background Tracking
- Static camera
	- Capture clean shots of background
- Object present
	- Average enough footage
- Background image - current video frame = difference image
	- Threshold for binary mask

# Nearest Neighbour Tracking
- Decide component with closest centroid using previous centroid
- Not good for occlusion
	- Will snap to next candidate

# Blob Tracking
- Build colour model of object
	- Eigenmodel
- Mask of pixels that match object
- Use centroid as location over time
- Pick connected component with centroid closest to previous location
- Good for distinctive colours
	- Not for practical situations though

# Template Tracking
- Sample distinctive patch from image
- Search all positions in video for patch
- Use cross-correlation
- Illumination changes
	- Brightness is uniform shift of greyscale values up or down
	- Correlated to the mean pixel value
	- Subtract means in template and frame to give invariance
	- Normalised cross-correlation