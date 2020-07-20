# Meeting 13/07/2020 - 11:30 am

##	-	Discussed plotting and analysing datasets
		+	can be useful prior to augmentation to ensure no data processed incorrectly.

##	-	Discussed reduction in dimensionality
		+	Potential to move away from standard classification (see papers sent from supervisor) - 
		
			- UPDATE 15/07/2020, becomes a regression problem given solution context, research effective discretisation!

			See the dimensional models section of the Wikipedia page for an overview: https://en.wikipedia.org/wiki/Emotion_classification

			The circumplex model is the widely used arousal-valence axis: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2367156/ (this is the classic map of emotions in this space: https://media.springernature.com/lw685/springer-static/image/art%3A10.1007%2Fs00779-017-1072-7/MediaObjects/779_2017_1072_Fig2_HTML.gif)

			The PAD model one slightly more complex model, but would be more useful for your intended domain: https://link.springer.com/article/10.1007/BF02686918

##	-	Discussed in more detail augmentation of datasets to provide better real-world findings:
		+	SNR (i.e. adding white noise)
			
		+	background noise (i.e. overlaying other voices, mechanical noise, etc.)
		
		+	reverberation (decay time/wet level)
		
		+	distortion (clipping/nonlinear effects/mic emulation)
		
		+	codec compression (different bitrates, simulated cutouts)

##	-	Useful post regarding approaches to training NNs: https://karpathy.github.io/2019/04/25/recipe/
