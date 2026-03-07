---
title: Super Resolution
tags:
  - ai
  - ai/media
---
- Auto-encoders
	- Get same image back
- Up-sample blurry small image classically
	- Bi-cubic
	- Encode-decode to deep sharpen
- No ground truth
	- [Unsupervised](../../../Learning.md#Un-Supervised)?
- Decoder stage
	- Identical architecture to encoder
![super-res](../../../../img/super-res.png)
- Is actually contractive/up sampling
![superres-results](../../../../img/superres-results.png)