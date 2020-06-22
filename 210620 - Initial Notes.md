21/06/2020 - Initial Notes/Response

* Data sets. For an ML approach to work, you'd need data, and potentially might need (transcribed) speech from gaming and a lot of it, because the language and acoustics are quite distinctive from existing datasets or models e.g. conversational speech, newsreaders.

	Regarding the dataset - my initial thoughts are to potentially use professional level play voice comms for a specific game title, and then classify via comparison to casual play with additional/undesirable chatter. This gives us a potential 'ideal' scenario. I think getting access to this audio should be relatively straightforward however may have some ethical/right of use implications. Currently considering alternatives as this may not be achievable.

* Evaluation. You would have to be able to approach the question of whether the system was successful. That might be via offline testing, but that doesn't quite get to the wider goals of improving in-game experience -- but that might be hard to test. 

	Hard to test user experience without a significant amount of playtest time, as well as requiring actual implementation of the system. 

* Technical complexity/interfacing. If you intend to integrate this into an existing voice system (e.g. patching it into Discord), this may be challenging, but I have to say I don't have much experience here and it could be trivial if something like plug-in support exists. 

	Approach problem solving initially, implementation if there is time.

* Training time. Voice systems can be very computationally demanding to train. We have some limited GPU cluster access that might support that, but it is very contended. There are other options, like Google Colab, but if your project required extensive training time that could be a problem.

	collab can be quite difficult to work with regarding timeouts, what I will likely do is train via the free version of collab and then potentially evaluate using the free trial of google cloud - assuming the GPU cluster at the uni would require an on campus connection

* ML. I don't know what your level of experience is here. Using off-the-shelf modules is fine if you don't have significant experience, but there are risks attached to fixing things when they go awry if you don't feel confident in this area. It is a great opportunity to learn though!

	pre-trained model such as the Google keras/pytorch audio set and then put my own dataset to use thereafter.

* Latency. Many ML models have impressive results but are being run offline, or with latency that would be unacceptable in gaming (think how long Siri or Alexa take to respond to speech). This is going to be a major design point of your project, and is a really interesting thing to work on, but you should be aware that that is where I see challenges.

	Main solution issues to implementation, however proof of concept useful.


Anyway, the idea is sensible and sound; do have a think about those challenges before our meeting. I also have a few thoughts that occur to me that may or may not be interesting:
* Is there a role for players to express their interest in phrases/content/topics (e.g. I'm guarding an important base, I really want to hear team-mates talking about that, less interested in battle raging elsewhere)? Some form of selective filtering driven by users?
	
	Currently some games have separate voice channels to mitigate this when many players are active on a server. In a smaller competitive setting filtering would be useful to clean up chatter as proposed - i.e. i want to hear key phrases such as ‘pushing short A’, ‘holding this angle’. We do not want to hear players complaining after their death for example.

* Is there a role for the results of the classification to be represented in other ways beyond muting/highlighting the audio stream? Visual indicators might be interesting, though could be hard to integrate with existing games.

	Some games have opted for a system of ‘pinging’, highlighting objects on minimap or HUD -  making competition less reliant on voice communications, however isn’t as quick to be understood by other players (they will hear ping noise and see location on map, but it may not be completely clear what the context of this communication is, can also be abused/spammed).


Main issues: 
Generative system vs filtering system?
* Generate phrases based on input vs filtering existing communications
Dataset:
* Difficult to give an ideal model, ‘pro’ communication often filled with irrelevant chatter also.
* A/B style data not possible.
* Data should match specific phrases, depending on game/map/situation (creates the filtering threshold.)


What is and what is not relevant:
* Some chatter may be useful (why did we lose that previous round).
* Clear boundaries to distinguish may be difficult and up to the dataset to decide?
* We may want to only apply this selective model on poor communicators and leave trusted players in fully open discourse. (See https://blog.counter-strike.net/index.php/2020/02/28450/ - Squelching the noise, using trust factor style ratings to set default mute state).

Points of interest:
	Would be ideal to have a generative element, i.e. the model generates audio for non-communicators (additional scope, uses the same training).
	
	Improve clarity of poor microphones (negated by generative approach).


Other relevant articles:


https://www.pcgamer.com/uk/20000-toxic-csgo-players-banned-in-six-weeks-by-faceit-and-googles-new-chat-ai/


https://towardsdatascience.com/how-to-apply-machine-learning-and-deep-learning-methods-to-audio-analysis-615e286fcbbc


https://www.comet.ml/site/


https://www.theverge.com/2019/10/14/20913323/microsoft-xbox-live-content-filters-messages-party-chat-moderation


Academic papers:


https://arxiv.org/ftp/arxiv/papers/1708/1708.07524.pdf - Supervised Speech Separation Based on Deep Learning: An Overview
