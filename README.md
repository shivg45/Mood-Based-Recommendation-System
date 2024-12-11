This system is intended to suggest a particular set of yoga routines based on the user's mood. 
The user's mood is identified through sentiment analysis of their input, and the system then maps this mood to a predefined
set of yoga poses that suit the identified mood.
Below is a breakdown of the approach, data preprocessing, model architecture, and next steps.
1. Approach:

In short, the aim is to build a system that recommends yoga routine based on the sentiment of the input given by the user. 
How it works: Mood Detection. From here, he inputs a description of his mood, such as "I feel happy." 
The system uses TextBlob to analyze this input for the aspect of polarity and subjectivity of the text.



2. Data Preprocessing:
Before diving into model architecture, let's discuss how the data is preprocessed for sentiment analysis:

Input Text: User enters a free-text description of their mood.
Sentiment Analysis: Input text is processed by utilizing the TextBlob library in order to determine the polarity of the given text. TextBlob offers two relevant metrics:
Polarity: Value ranging from -1 to 1 where -1 represents negative polarity, and 1 represents positive polarity; the value is 0 when the text has a neutral polarity.
Subjectivity: A value between 0 and 1, where 0 is very objective and 1 is very subjective.
Mood Categorization: The input falls under one of six moods based on the polarity value:
Joyful: Polarity > 0.5
Relaxed: 0.2 < Polarity <= 0.5
Neutral: 0 < Polarity <= 0.2
Sad: -0.2 <= Polarity < 0
Anxious: -0.5 <= Polarity < -0.2
Angry: Polarity < -0.5
    
    
3. Result:
The output of the system will depend on the input of the user:

If the user describes feeling joyful, for example, "I am feeling great!", the system will identify the mood as joyful and
recommend poses like Sun Salutations and Dancer's Pose.
If the user explains how he feels anxious for example by saying, "I feel overwhelmed", the system will note the mood as
being anxious and provide poses such as Cat-Cow Stretch and Butterfly Pose.

Outcome:
--> How are you feeling today? Describe your mood: angry

Your mood seems to be: Anxious.
Here are some recommended yoga poses for you:
- Cat-Cow Stretch (Marjaryasana-Bitilasana)
- Butterfly Pose (Baddha Konasana)
- Standing Forward Bend (Uttanasana)
