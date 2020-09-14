## MSc Project for Information Technology+ (COMPSCI5018P)
### MSc Software Development (2019-2020) 
#### University of Glasgow

Source-code for the research paper 'Deep learning architectures for speech emotion recognition'.

Abstract:
	* "This paper seeks to evaluate machine learning methodology in the task of speech emotion recognition (SER) by utilising a signal processing approach. This is done with aim of assessing user behaviour during the use of online voice communication."

	* "We use dimensional models of emotion, put forward by empirical research to gain nuanced information about sampled emotion data, disseminating greater insight into user voice communication activity."

	* "This paper focuses on the extraction and use of Mel-frequency cepstral coefficients (MFCC) as feature vectors for feed forward neural network architectures." 

	* "Experiments conducted show evidence that the methodology proposed in this paper is partially effective on unseen, dissimilar in structure real-world data, which has proven to be a hurdle to deployment of solutions in the area of automatic speech recognition (ASR) and SER. These findings provide a framework to enable more precise, automated user handling."

Files:
	speech_emotion_recognition.ipynb - main notebook
		- PyTorch MLP model
		- sklearn mlp, randomforest baseline examples

	augment_data.ipynb - data augmentation batch scripts
		- white noise
		- background noise, simulated chatter
		- overdrive
		- reverb

Datasets used to train and validate model:
	+ RAVDESS
	+ CREMA-D

Datasets used only to test model performance:
	+ SAVEE
	+ TESS

Usage:
	+ Download datasets listed above
	+ Run requirements.txt (NOTE: if using collab, portaudio install will be required)
	+ (not required) Use augment_data notebook to generate additional augmented sets (rewrite of output and input directories will be required)
	+ (not required) Use speech_emotion_recognition notebook to train, validate and test model
	+ To simply generate results and plots, skip to and run cells in the 'Testing' section of speech_emotion_recognition.ipynb, this will load the provided 'best model' state.
