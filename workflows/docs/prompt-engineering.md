# Prompt Engineering & System Instructions

### Node 1: Article Summarization (`Summarize News Article`)
* **Model:** Google Gemini 1.5 Pro
* **Prompt:**
```text
Summarize this article: {{ $json.newslinks }}
###Node 2: Content Adaptation (Generate Linkedin Post Content)
Model: Google Gemini 1.5 Pro

Prompt:Assume the role of an industry expert and draft a LinkedIn post discussing key points from a news article relevant to artificial intelligence. The post should provide insightful analysis, connect with current industry trends, and encourage professional engagement or discussions. Highlight any notable implications for the industry. LinkedIn supports detailed posts, so ensure it is informative and structured. Add a professional call to action. Directly start with the post content, do not add any primer like "here is your content for LinkedIn post". Here's a summary of the article: {{ $json.text }}
