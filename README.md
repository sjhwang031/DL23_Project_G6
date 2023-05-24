# DL23_Project_G6
# 0. Introduction
Target: High school students

Class contents: Textbooks or mock tests

Goal: Effective teaching using digital literacy
# Class contents
1.We do know that the ability to question, whether verbally or through other means, is one of the things that separates us from lower primates. Paul Harris, an education professor at Harvard University who has studied questioning in children, observes, "Unlike other primates, we humans are designed so that the young look to the old for cultural information." He sees this as an important "evolutionary divide" - that from an early age, even before speech, humans will use some form of questioning to try to gain information. A child may pick up a kiwi fruit and indicate, through a look or gesture directed at a nearby adult, a desire to know more. Chimpanzees don't do this; they may "ask" for a treat through signaling, but it's a simple request for food, as opposed to an information-seeking question. So then, one of the primary drivers of questioning is an awareness of what we don't know - which is a form of higher awareness that separates not only man from monkey but also the smart and curious person from the dullard who doesn't know or care. Good questioners tend to be aware of, and quite comfortable with, their own ignorance (Richard Saul Wurman, the founder of the TED Conferences, has been known to brag, "I know more about my ignorance than you know about yours"). But they constantly examine that vast ignorance using the question flashlight - or, if you prefer, they attack it with the question spade.

*primate: 영장류 **brag: 호언장당하다 ***spade: 삽

2.Humans are motivated, at least in part, by empathy and concern for the welfare of others. We donate blood for strangers, contribute to charity, and punish violators of social norms. Chimpanzees are, together with bonobos, our closest relatives, and they similarly engage in cooperative hunting, comfort victims of aggression, and perform other collective activities. Would they show concern for the welfare of unrelated, familiar chimps if the benefits were at no cost to themselves? Researcher Joan Silk and her collaborators conducted an experiment with chimps that had lived together for fifteen years or more. Eighteen chimps were studied, from two different populations with different life histories and exposures to experiments. Pairs of chimps faced each other in opposing enclosures or sat side by side, and could see and hear each other. One chimp, the actor, was given the choice to pull one of two handles: if the actor pulled the "nice" handle, both the actor and the other chimp got food, and exactly the same portion. If the actor pulled the "nasty" handle, only the actor received food, and the other chimp got nothing. In a control test, only the actor was present. Which handle did the chimps pull? When no other chimp was present, the actors chose both options about equally frequently. The chimps didn't care, and why should they? Yet even when a second chimp arrived, the chimps didn't choose the "nice" option more often. Although they could clearly see the other one displaying desperate begging gestures, or happily eating the food when it was dispensed, the chimps showed no sign of empathy. It should be noted that they showed no spitefulness either. What mattered to the actors more than the other chimp was whether the handle for the nice option was placed on their right or left side. They had a much stronger preference for the right side than for the happiness of their partner. Chimps simply did not seem to care about the welfare of unrelated group members.

*enclosure: 올타리 안, 담장 안 **dispense: 제공하다, 나눠 주다 ***spitefulness: 악의
# 1. Wordcloud

**Watch Wordcloud and get a rough idea of what's coming out of this class**

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
**Practice speaking by listening to the voice from tts and following along**

!pip install gTTS
from gtts import gTTS
from IPython.display import Audio

def tts(text):
  gtts_object = gTTS(text,lang = "en", slow = True) 
  gtts_object.save("myaudio.mp3")
  return Audio("myaudio.mp3")
tts()


# 3. Vocabulary test
**Studying and learning difficult vocabulary in the text**

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
**Read the text and solve the problem**

Quiz

quiz_numbers = "3" #@param = [1, 2, 3, 4, 5]
qn = int(quiz_numbers)

if qn == 1:
  myQ = input("text ")
  if myQ == "answer":
    txt = "That's correct! The answer is answer."
  else:
    txt = "Your answer %s is incorrect. Try again!"%myQ

elif qn == 2:
  myQ = input("text ")
  if myQ == "answer":
    txt = "You're right! The answer is answer."
  else:
    txt = "Your answer %s is incorrect. Try again!"%myQ

elif qn == 3:
  myQ = input("text ")
  if myQ == "answer":
    txt = "Good job! The answer is answer."
  else:
    txt = "Your answer %s is incorrect. Try again!"%myQ

elif qn == 4:
  myQ = input("text ")
  if myQ == "answer":
    txt = "Congratulations! The answer is answer."
  else:
    txt = "Your answer %s is incorrect. Try again!"%myQ

elif qn == 5:
  myQ = input("text ")
  if myQ == "answer":
    txt = "Wow, you're great! The answer is answer."
  else:
    txt = "Your answer %s is incorrect. Try again!"%myQ

etts(txt)

Audio("E-audio.mp3", autoplay = True)

# 5. Watching grammar video
**Watching videos related to grammar in the text**

Videos = "1. Grammar" #@param = ["1. Grammar", "2. ", "3. "]

nums = Videos.split(".")
num = nums[0]
num = int(num)-1

video_id = ["link","",""]
myvideo = video_id[num]
YouTubeVideo(myvideo, width = 800, height = 600)
# 6. Self-log and review
**Write a self-log and get evaluation or feedback on the class**

[Self log link](https://forms.gle/)
