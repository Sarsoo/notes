---
onenote-id: 0-c8e7cc162db901b624fb010b9b61796f!1-D084F068F621FF9!3707
---
Inverse Fourier transform of the log of the Fourier
 
- Separate source and filter

![Exported image](../../../../img/OneNote/Cepstrum%20image%20c248b1c3449a4d50.png)

Complex
 
- Sort of like time
	- Log means it's not the same
		- Non-linear operation
 ![msu 1](../../../../img/OneNote/Cepstrum%20image%20570b99b4ef069cbd.png)  
![ccT DFT I i2mn](../../../../img/OneNote/Cepstrum%20image%200cd4b1bed6f20f5d.png)

- Phase unwrapped

Real
 
- More common
- Magnitude discards phase
 ![3 s ul1](../../../../img/OneNote/Cepstrum%20image%20a699a310b9eb2864.png)  

- Even and real numbers going into inverse Fourier
	- Only cosines
		- Symmetric
	- Can replace with discrete cosine transform

Cepstral analysis Liftering

- Homomorphic decomposition
 ![Amplitude dB](../../../../img/OneNote/Cepstrum%20image%20b11e59432f7a5324.png)

- Low-pass liftering for formant identification
 ![14 40 0.2 0.1 0.1 0.2 10 10 Quefrency ms Frequency...](../../../../img/OneNote/Cepstrum%20image%20b7fc0c065a5ea9ad.png)

- Band-pass liftering for periodicity
	- Fundamental frequency
	- Strength of harmonics
 
- Green curve is offset
	- Lost phase information

Mel-Frequency
 
- Non-linear warping of frequency scale
- Closer matching human perception
	- Critical bands
- Reducing effect of pitch
 ![fHz fMel 1127 In 1 700](../../../../img/OneNote/Cepstrum%20image%202b2461fb34d4e9b4.png)  
![AAAAAAAAAA gain](../../../../img/OneNote/Cepstrum%20image%20028dec66eb99eb9a.png)  

Mel-Frequency Cepstral Coefficients
 ![Machine generated alternative text sn DFT In . csv...](../../../../img/OneNote/Cepstrum%20image%2099e0500110a4711c.png)

- Middle of real cepstrum
	- Real because of mag op
- Bins contributions from bands
	- Compression operation

Frequency Response of Coefficients
 ![0 2 dxe dxe zH](../../../../img/OneNote/Cepstrum%20image%2076c7f5d513797671.png)

- z=ejw yields filter frequency response

Perceptual Linear Prediction  
PLP
 ![sn Sk 13 x cm cc](../../../../img/OneNote/Cepstrum%20image%2037a2da3dd6e97d89.png)  

- Similar to mel
- Different filter bank
	- Trapezoid
	- Closer to perception & critical bands
	- Bark scale
- Second filter is for loudness perception
- Cube root is closer to perception of hair cells
- Convert linear prediction coefficients into cepstral ones
	- For HMMs
	- Like diagonal variance
		- Not cross-correlated

![Shortterm spectrum 1. Binning 2. Frequency weighti...](../../../../img/OneNote/Cepstrum%20image%20ec95f671a3042be8.png)  
![1. 2. Shortterm spectrum apply Hamming window comp...](../../../../img/OneNote/Cepstrum%20image%207a52306059d77d96.png)  
![5. Inverse FT a IDCT b IDFT information concentrat...](../../../../img/OneNote/Cepstrum%20image%203ce5b0ff4de9ec36.png)

Amplitude Features
 
- Can use 0th cepstral coefficient
 ![Exported image](../../../../img/OneNote/Cepstrum%20image%20911860b97cd5e44e.png)  

Dynamic Features
 
- Look to change in coefficients
	- Really good for consonants
		- Transients
	- Noise rejection
 ![Db 1 Db](../../../../img/OneNote/Cepstrum%20image%2098a24eb9f0bfeac2.png)  
![Ck tl Ckt Cktl](../../../../img/OneNote/Cepstrum%20image%201d0249acf4a3e825.png)  

- Can take second gradient for acceleration
	- Delta delta

Feature
 ![Machine generated alternative text AAI AA2 . AAI 2...](../../../../img/OneNote/Cepstrum%20image%20133bafe790a24cc8.png)  

1. Cepstral coefficients (12)
	1. Append log energy (+1 = 13)
2. Delta
3. Delta delta
 
- 13 * 3 = 39-D feature
	- Standard
	- Use 10ms windows

_Cepstral Deconvolution_

Phase Unwrapping
 
- Convolution theorem use phase within range +-pi

![Exported image](../../../../img/OneNote/Cepstrum%20image%208b1c40645b1dfb85.png)

- Smooth phase spectrum by adding integers of 2pi
 ![3.5 2.5 1.5 0.5 0.5 wrapped phase unwrapped phase ...](../../../../img/OneNote/Cepstrum%20image%207a773d9c97eaf7ec.png)  

Homomorphic
 
- Can split into cascade of 3 homomorphic systems
	- F, log, inverse F

Bark Scale
 
_"...a frequency scale on which equal distances correspond with perceptually equal distances. Above about 500 Hz this scale is more or less equal to a logarithmic frequency axis. Below 500 Hz the Bark scale becomes more and more linear."_
 \> From \<[https://en.wikipedia.org/wiki/Bark_scale](https://en.wikipedia.org/wiki/Bark_scale)\>     
![Exported image](../../../../img/OneNote/Cepstrum%20image%2027b3ffb550effc04.png)  

[Cepstrum Numpy](https://flothesof.github.io/cepstrum-pitch-tracking.html)  
[Cesptrum - John Cook](https://www.johndcook.com/blog/2016/05/18/cepstrum-quefrency-and-pitch/)

[Fourier Transform](../../../../../../Signal%20Proc/Fourier%20Transform.md)

_Assuming the amplitude scale is arbitrary_

