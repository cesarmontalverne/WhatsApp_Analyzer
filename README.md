# WhatsApp_Analyzer

## Introduction
Whatsapp is the most famous messaging app platform in Latin America and Europe. Due to the nature of online conversations, people have a lot of flexibility regarding when they are going to respond. The myriad of tools WhatsApp offers include text, audio, image, video, documents, video calls, audio calls, and stickers which also allows for countless different ways to respond. 

Over the last two decades, humankind has seen enormous advancements in technology, which lead each one of us to be able to have access to more information than any of our ancestors would have ever imagined. However, it's also true that there has never been a time where more data had been gathered from each one of us, and used either by big corporations or the government in several ways - not always in our favor. I think this is a great opportunity to own my data and see what conclusions I can come up with. Given this inspiration, I decided to create this project to analyze the response rate and time I respond to my friends and vice versa. 

## Objectives
- Create a predictive model for the next action will in a conversation.
- Create pertinent graphical visualizations for my conversations.
- Create a deterministic script, that could apply to any conversation without change.

## Challenges
-          How to organize the data in a meaningful way?
       o   Texts are sent in bursts: One person sends a few texts in a row and another answers a few texts in a row. This type of double texting may complicate the analysis. I thought it was more meaningful to group them together into bursts. Instead of predicting the next text, I predict when the next burst is. As the target variable I use the initial time of the following burst.
-          How to extrapolate data from text?
       o   That’s where feature engineering and NLP came into play. The first thing I did was creating a minimum version of the model. Then I added day of the week, time of the day, whether it was morning, number of words on the current text and etc. Then I created an exponential moving average(EMA) of those values, including also an EMA of the previous target values. Finally, I used some sentiment analysis and TF-IDF on the actual textual data to further improve the model.
-          How to deal with privacy?
       o   I was submitting my project to a professor and had to present it for the whole class. Naturally, privacy was a big issue. I created different files: one for data cleaning, one for model creations and one only for the presentation. This not only made my work more organized and easier to follow, but also allowed me to save the minimum amount of data necessary into an RData file for the final project.

