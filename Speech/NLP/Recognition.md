1. Automatic Speech Recognition
	- Spoken words to machine-readable form
2. Natural language understanding
	- High level cognitive interpretation
		- Structure
		- Meaning
		- Intention

# Automatic Speech Recognition
## Applications
- Business/desktop apps
	- Dictation
	- Voice commands
- Voice enabled services/apps
	- Siri
- Home automation
- Game & Entertainment
- Education
- Speech therapy/Rehab
- Hearing assistance
	- Live CC

## Challenges
- Speaker dependency
	- Accent
	- Emotion
- Vocab size
	- Slang
- Isolated words vs Continuous speech
	- Hard to segment continuous speech
- Language constraints & Knowledge sources
	- Training source is critical
- Acoustic ambiguity
	- Similar sounding speech
- Noise robustness
	- Background noise
	- Reverberation

# Speech Diarisation
- Who speaks when?
- Split stream into homogenous segments for identity
- Structure stream into speaker turns
- Provide speaker identity
- Combination of
	- Speaker segmentation
		- Speaker changes in stream
	- Speaker clustering
		- Grouping segments together on basis of characteristics
- Gaussian mixture model
	- HMM
- Bottom-up
	- More popular
	- Succession of clusters
	- Merge redundant clusters
		- Remaining belong to speakers
- Top-down
	- Single cluster
	- Iteratively split until speaker clusters