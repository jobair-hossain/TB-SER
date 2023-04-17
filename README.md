NLP pipeline for topic-based SER

In this NLP pipeline, we aim to analyze team conversations by transcribing speech to text, performing sentiment analysis, and conducting topic modeling of the conversation. The pipeline consists of several stages, each employing state-of-the-art machine learning techniques and models illustrates in the figure 1.

![NLP Pipeline](https://user-images.githubusercontent.com/59045223/232633905-26db63aa-f86c-4bc4-8f7f-dd08ec5df84b.png)



1. Speech Input (Recorded Audio of Team Conversation): The first stage involves collecting the recorded audio of the team conversation. This data serves as the primary input for the subsequent stages in the pipeline.

2. Speech to Text (ASR: Whisper): In this stage, the recorded audio is transcribed into text using an Automatic Speech Recognition (ASR) system. OpenAI's Whisper ASR model is employed for this purpose. Whisper is a deep learning-based ASR model trained on a large dataset of multilingual and multitask supervised data collected from the web. It converts the spoken words in the audio to a textual representation, which serves as input for the next stage in the pipeline.

3. Sentiment Analysis (T5, RoBERTa, XLNet): Once the conversation is transcribed into text, sentiment analysis is performed using multiple transformer-based models, such as T5, RoBERTa, and XLNet. These models are pretrained on large-scale language modeling tasks and fine-tuned for sentiment analysis. By applying these models, we can extract various emotions and sentiments, such as happiness, sadness, anger, and positive or negative sentiment, from the team conversation text. The output from this stage provides insights into the emotional dynamics of the conversation.

4. Topic Modeling of Team Conversation (BERTopic): The final stage in the pipeline involves topic modeling to identify the main themes and subjects discussed during the team conversation. BERTopic, a topic modeling technique based on BERT, is used for this purpose. BERTopic leverages BERT's contextualized embeddings to create dense representations of the conversation text. These representations are then clustered using the UMAP algorithm, followed by a clustering algorithm such as HDBSCAN or K-means, to identify coherent topics. The resulting topic clusters provide an overview of the key topics discussed during the team conversation.

By integrating these stages into a cohesive NLP pipeline, we can analyze team conversations by transcribing speech, extracting emotions and sentiments, and identifying the main topics discussed. This comprehensive analysis can provide valuable insights into team dynamics, performance, and collaboration, ultimately supporting more effective team management and decision-making.
