$$X(\omega)=\int_{-\infty}^{\infty}x(t)e^{-j\omega t}dt$$
$$x(t)=\frac{1}{2\pi}\int_{2\pi}X(\omega)e^{j\omega t}d\omega$$
## Discrete-Time
$$X(\omega)=\sum_{-\infty}^{\infty}x[n]e^{-j\omega n}$$
$$x[n]=\frac{1}{2\pi}\int_{2\pi}X(\omega)e^{j\omega n}d\omega$$

## Discrete Fourier Transform
Digital Signal
$$X[k]=\sum_{n=0}^{N-1}x[n]e^{-j\omega_{k}n}$$
$$x[n]=\frac{1}{N}\sum_{k=0}^{N-1}X[k]e^{j\omega_{k}n}, n=0,1,\ldots,N-1$$

## Power Spectral Density
PSD
$$P[k]=|X[k]|^2$$

## Spectrogram
-   PSD vertically
-   Frequency power over time horizontally
-   ___Time and frequency resolution inversely proportional___
-   Resolution
	-   Frequency
		-   $fs/N$
	-   Time
		-   $N/fs$
-   STFT has fixed resolution depending on window size
	-   Wider window
		-   Better frequency res
		-   Worse time resolution
			-   Can't tell where stuff changes with big window
	-   Can't use too wide
		-   Frequency can change during window
-   20-30ms window of speech usually treated as quasi-stationary
-   Overlapping window
	-   Hop size of 5ms
-   Appending windows can cause discontinuities
	-   Use window function to smooth
		-   Hann

## Fast-Fourier
FFT
-   Faster version of DFT
	-   Three parts
		-   Shuffling
			-   Bit reversal
			-   Shuffle N-dimensional input into N one-dimensional signals
		-   N one-point DFTs
		-   Merge
			-   N one-point DFTs into one N-point DFT
			-   Butterfly merging equations

## Short-Time Fourier Transform
STFT

-   Short-term
-   N-point windowed DFT
	-   Probably use FFT
$$x[k,m]=\sum_{n=0}^{N-1}x[m\delta+n]w(n)e^{-j\omega_kn}$$
-   $\omega$
	-   Discrete angular frequency
-   $m$
	-   Time-frame index
-   $\delta$
	-   Hop size
-   $w(n)$
	-   Window function
	-   Hann
