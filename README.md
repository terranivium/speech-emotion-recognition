## MSc Software Development (2019-2020) 
### University of Glasgow

Source-code for the research paper 'Deep learning for robust dimensional characterisation of affect in speech'.

#### Paper abstract:
	* "This paper seeks to evaluate machine learning methodology 
	in the task of speech emotion recognition (SER) by utilising a 
	signal processing approach. This is done with aim of assessing
	user behaviour during the use of online voice communication."

	* "We use dimensional models of emotion, put forward by empirical
	research to gain nuanced information about sampled emotion data,
	disseminating greater insight into user voice communication activity."

	* "This paper focuses on the extraction and use of Mel-frequency 
	cepstral coefficients (MFCC) as feature vectors for feed 
	forward neural network architectures." 

	* "Experiments conducted show evidence that the methodology 
	proposed in this paper is partially effective on unseen, 
	dissimilar in structure real-world data, which has proven 
	to be a hurdle to deployment of solutions in the area of 
	automatic speech recognition (ASR) and SER. These findings 
	provide a framework to enable more precise, automated user handling."

#### Files:
	'speech_emotion_recognition.ipynb' - main notebook
		- PyTorch (MLP) model

	'augment_data.ipynb' - data augmentation batch scripts
		- white noise
		- simulated chatter, background noise
		- overdrive
		- reverb

#### Datasets used to train, validate and test model:
	+ RAVDESS
	+ CREMA-D

#### Datasets used only to emulate wild test performance:
	+ TESS

#### Usage guide:
	+ To simply generate results and plots, 
	skip to and run cells in 'Testing' section of 'speech_emotion_recognition.ipynb', 
	this will load the provided 'best model' state.
