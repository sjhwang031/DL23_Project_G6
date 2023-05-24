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

!pip install gTTS
from gtts import gTTS
from IPython.display import Audio

def tts(text):
  gtts_object = gTTS(text,lang = "en", slow = True) 
  gtts_object.save("myaudio.mp3")
  return Audio("myaudio.mp3")
tts()


# 3. Vocabulary test
Studying and learning difficult vocabulary in the text

import random

vocab_dict = {
    "apple": "a round fruit with red or green skin and white flesh",
    "book": "a written or printed work consisting of pages glued or sewn together along one side and bound in covers",
    "computer": "an electronic device for storing and processing data",
    "dog": "a domesticated carnivorous mammal with a pointed snout, furry coat, and long tail",
    "umbrella": "a device consisting of a circular canopy of cloth on a folding metal frame supported by a central rod, used as protection against rain",
    "television": "an electronic system of transmitting images and sound that are reproduced on screens, chiefly used to broadcast programs for entertainment, information, and education",
    "coffee": "a drink made from the roasted and ground bean-like seeds of a tropical shrub",
    "chair": "a separate seat for one person, typically with a back and four legs",
    "pen": "an instrument for writing or drawing with ink",
    "phone": "a device that can make and receive calls over a telephone line or wireless connection"
}

def quiz(num_questions):
    score = 0
    questions = random.sample(list(vocab_dict.items()), num_questions)
    for word, definition in questions:
        print("What is the word for this definition? '{}'".format(definition))
        answer = input("Answer: ")
        if answer.lower() == word.lower():
            print("Correct!")
            score += 1
        else:
            print("Incorrect. The correct answer is '{}'.".format(word))
        print()
    print("Quiz complete. You scored {}/{} points.".format(score, num_questions))

if __name__ == '__main__':
    num_questions = int(input("How many questions would you like to play? "))
    quiz(num_questions)
    
# 4. Solving the problems
Read the text and solve the problem

# 5. Watching grammar video
Watching videos related to grammar in the text

Videos = "1. Grammar" #@param = ["1. Grammar", "2. ", "3. "]

nums = Videos.split(".")
num = nums[0]
num = int(num)-1

video_id = ["link","",""]
myvideo = video_id[num]
YouTubeVideo(myvideo, width = 800, height = 600)
# 6. Self-log and review
Write a self-log and get evaluation or feedback on the class

[Self log link](https://forms.gle/)
