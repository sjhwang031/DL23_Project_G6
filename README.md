# 👨‍🏫Lessons for the improvement of high school 3rd grade students' reading skills
# Step 1
🎧[Click here to watch preview video](https://youtu.be/STtZdbJCZwc)
# Step 2
📕[Click here to start main lesson](https://github.com/sjhwang031/DL23_Project_G6/blob/main/DL23_Project_G6.ipynb)
# 🙋Learners 
This online course is suitable for High school 3rd grade students 
# 🎯Goal
Improvement of high school 3rd grade students' reading skills by using digital tools
# 📖Class contents
1.We do know that the ability to question, whether verbally or through other means, is one of the things that separates us from lower primates. Paul Harris, an education professor at Harvard University who has studied questioning in children, observes, "Unlike other primates, we humans are designed so that the young look to the old for cultural information." He sees this as an important "evolutionary divide" - that from an early age, even before speech, humans will use some form of questioning to try to gain information. A child may pick up a kiwi fruit and indicate, through a look or gesture directed at a nearby adult, a desire to know more. Chimpanzees don't do this; they may "ask" for a treat through signaling, but it's a simple request for food, as opposed to an information-seeking question. So then, one of the primary drivers of questioning is an awareness of what we don't know - which is a form of higher awareness that separates not only man from monkey but also the smart and curious person from the dullard who doesn't know or care. Good questioners tend to be aware of, and quite comfortable with, their own ignorance (Richard Saul Wurman, the founder of the TED Conferences, has been known to brag, "I know more about my ignorance than you know about yours"). But they constantly examine that vast ignorance using the question flashlight - or, if you prefer, they attack it with the question spade.

*primate: 영장류 **brag: 호언장담하다 ***spade: 삽

2.Humans are motivated, at least in part, by empathy and concern for the welfare of others. We donate blood for strangers, contribute to charity, and punish violators of social norms. Chimpanzees are, together with bonobos, our closest relatives, and they similarly engage in cooperative hunting, comfort victims of aggression, and perform other collective activities. Would they show concern for the welfare of unrelated, familiar chimps if the benefits were at no cost to themselves? Researcher Joan Silk and her collaborators conducted an experiment with chimps that had lived together for fifteen years or more. Eighteen chimps were studied, from two different populations with different life histories and exposures to experiments. Pairs of chimps faced each other in opposing enclosures or sat side by side, and could see and hear each other. One chimp, the actor, was given the choice to pull one of two handles: if the actor pulled the "nice" handle, both the actor and the other chimp got food, and exactly the same portion. If the actor pulled the "nasty" handle, only the actor received food, and the other chimp got nothing. In a control test, only the actor was present. Which handle did the chimps pull? When no other chimp was present, the actors chose both options about equally frequently. The chimps didn't care, and why should they? Yet even when a second chimp arrived, the chimps didn't choose the "nice" option more often. Although they could clearly see the other one displaying desperate begging gestures, or happily eating the food when it was dispensed, the chimps showed no sign of empathy. It should be noted that they showed no spitefulness either. What mattered to the actors more than the other chimp was whether the handle for the nice option was placed on their right or left side. They had a much stronger preference for the right side than for the happiness of their partner. Chimps simply did not seem to care about the welfare of unrelated group members.

*enclosure: 올타리 안, 담장 안 **dispense: 제공하다, 나눠 주다 ***spitefulness: 악의

# 💭1. Wordcloud

**The word cloud gives you a glimpse of the main topics covered in the class. It visually represents the frequency and prominence of different words or phrases, providing a quick overview of the key concepts you can expect to encounter. Analyzing the word cloud helps you get an initial understanding of the subject matter and mentally prepare for the class.**

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

# 🎤2. Shadow Reading
**Practicing speaking by listening to TTS audio and following along helps improve pronunciation, intonation, and speaking skills. It exposes you to native-like accents, allows for repetition, and enhances listening comprehension. Actively engage by repeating words and phrases, imitating the speaker's rhythm, and trying shadowing. Consistent practice with TTS can boost fluency and confidence in speaking.**

!pip install gTTS
from gtts import gTTS
from IPython.display import Audio

def tts(text):
  gtts_object = gTTS(text,lang = "en", slow = True) 
  gtts_object.save("myaudio.mp3")
  return Audio("myaudio.mp3")
tts()


# 📝3. Vocabulary test
**By learning difficult vocabulary in advance through quizzes, it reduces the burden of reading the text and helps understanding**

import random

vocab_dict = {
    "apple": "a round fruit with red or green skin and white flesh",}

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
    
# 💡4. Solving the problems
**To identify the understanding of the text, solve the problem and check the contents that learners did not understand**

Quiz

quiz_numbers = "3" #@param = [1, 2, 3, 4, 5]
qn = int(quiz_numbers)

if qn == 1:
  myQ = input("text ")
  if myQ == "answer":
    txt = "That's correct! The answer is answer."
  else:
    txt = "Your answer %s is incorrect. Try again!"%myQ

etts(txt)

Audio("E-audio.mp3", autoplay = True)

# 👀5. Watching grammar video
**Watch grammar videos related to the text to improve understanding. Pay attention to explanations, examples, and visuals. Take notes and apply the grammar rules to the text. Supplement with additional resources as needed. Videos provide dynamic explanations for better comprehension.**

Videos = "1. Grammar" #@param = ["1. Grammar", "2. ", "3. "]

nums = Videos.split(".")
num = nums[0]
num = int(num)-1

video_id = ["link","",""]
myvideo = video_id[num]
YouTubeVideo(myvideo, width = 800, height = 600)
# 💯6. Self-log and review
**Write a self-log and get evaluation or feedback on the class**

⭐[Self log link]⭐
(https://docs.google.com/forms/d/1pD0EDTGgGtazjJxkJ9eZkTeYfostJy84R3HgUOBCmOo/edit)
