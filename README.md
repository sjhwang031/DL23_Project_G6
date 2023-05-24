# DL23_Project_G6
# 0. Introduction
Target: High school students

Class contents: Textbooks or mock tests

Goal: Effective teaching using digital literacy
# 1. Wordcloud
Watch Wordcloud and get a rough idea of what's coming out of this class

import matplotlib.pyplot as plt
from wordcloud import WordCloud

wordcloud = WordCloud(
    background_color='white',
    width=800,
    height=800,
    max_words=100
).generate()

plt.figure(figsize=(8, 8))
plt.imshow(wordcloud, interpolation='bilinear')
plt.axis('off')
plt.show()

# 2. Shadow Reading
Practice speaking by listening to the voice from tts and following along
# 3. Vocabulary test
Studying and learning difficult vocabulary in the text
# 4. Solving the problems
Read the text and solve the problem
# 5. Watching grammar video
Watching videos related to grammar in the text
# 6. Self-log and review
Write a self-log and get evaluation or feedback on the class
