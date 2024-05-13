# Sentiment Analysis and Personalized Messaging for Clinical Trial Recruitment

## Project Overview

This project aims to automate the identification of potential clinical trial participants by analyzing sentiments expressed on Reddit, and generating personalized messages to engage users based on their interests and sentiments towards clinical trials.

### Objectives:
- Scrape relevant discussions from Reddit.
- Perform sentiment analysis on these discussions.
- Generate personalized engagement messages based on the analysis.

### Installation

Clone the repository:

git clone https://github.com/yourgithubusername/clinical-trial-recruitment.git

Run the notebook

This notebook installs all necessary libraries directly within the notebook. 

## Methodology

### Data Collection
- Data is scraped from Reddit using PRAW (Python Reddit API Wrapper), focusing on subreddits related to health conditions relevant to clinical trials.

### Sentiment Analysis
- Sentiments are analyzed using the Hugging Face `transformers` library, identifying user sentiments towards clinical trials.

### Message Generation
- Based on the sentiment analysis results, personalized messages are generated using the GPT-2 model to engage potential participants.

## Challenges Faced
- Handling rate limits and data scraping restrictions from Reddit.
- Ensuring accuracy in sentiment analysis and relevance in message generation.
- Limited Access to OpenAI's Paid API. I did not have access to it for this project. I opted to use the GPT-2 model provided by Hugging Face's Transformers library, which is open-source and free. While it may not offer the same level of sophistication as some of OpenAI's GPT-3, it still provides robust capabilities for generating human-like text.
- PRAW (Python Reddit API Wrapper) restricts scraping to public subreddits only. Many relevant discussions in restricted subreddits were inaccessible, limiting the scope of data collection. I focused on scraping a broad array of public subreddits related to health conditions to maximize the volume and diversity of data. Additionally, I implemented error handling to gracefully skip over any restricted content without interrupting the scraping process.
- The messages generated by the GPT-2 model often lacked specific relevance to the nuanced context of clinical trials. Despite being grammatically correct and coherent, the messages sometimes diverged from the intended focus or failed to directly address the specifics of the user's sentiments about clinical trials.
- GPT-2, while robust, is not fine-tuned for medical or clinical contexts by default. As a result, the nuances of engaging potential clinical trial participants were not always adequately captured. The model would occasionally produce content that, while related to the health domain, did not align precisely with the clinical trial narratives or the specific details that might be critical in a real-world clinical trial recruitment context.

## Ethical Considerations

- Ensured compliance with Reddit's API usage terms.
- Implemented data handling practices to respect user privacy and confidentiality.
- Messages are designed to be informative and empowering, avoiding manipulation.
- The project only accesses and analyzes publicly available data. It does not attempt to bypass any privacy settings or access protected or private information.

## Future Work

- Enhance the model's ability to understand deeper nuances in medical discussions.
- Expand the scraping to more platforms to gather broader insights.
- Implement A/B testing to refine message effectiveness.

## Conclusion

This project represents a significant step towards leveraging AI in enhancing patient recruitment for clinical trials, with a strong ethical framework and innovative use of technology.

