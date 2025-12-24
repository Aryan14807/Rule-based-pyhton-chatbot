# Rule-based-pyhton-chatbot
python project- rule based ai chatbot assistant


#Rule based AI python chatbot

import datetime
import time

name= input("Swagat hai,Enter your name : ")
presentHour= datetime.datetime.now().hour

if 5<= presentHour <=11:
      print("Good Morning,",name)
elif 11<= presentHour <=17:
      print("Good Afternoon,",name)
elif 17<= presentHour <=20:
      print("Good Evening,",name)
else:
      print("Good Night",name)   



print("Namste! welcome to mini chatbot")
print("You can ask me basic question, Type 'bye' to exist from the mini  bot")

# Chatbot Memory Creation [dictionary of responses ]

responses = {
    "hello": "Hi,welcome. How can Ihelp you? ",
    "how are you":"I am very fine. Thank you",
    "who are you":"I am a Smart AI chatbot",
    "motivate me":"keep going.Every bug of your project makes you a better developer",
    "happy":"Great to hear that",
    "What are fuctions":"fuctions are the key words by which a certain task is performed",
    "how can i help to you": "i am can help you in various ways,suggest anything you want",
}


#Fuction to get response of chatbot

def getResponseofbot(userQuestion):
    userQuestion= userQuestion.lower() 
    for eachkey in responses:
        if eachkey in userQuestion:
            return responses[eachkey]
        
    return "I am not able to tell you that yet. i am still in learning mode"





#take user input

while True:
            
            userInput= input("please ask your question:")
            reply=getResponseofbot(userInput)
            print("Bot response:", reply)

            if "bye" in userInput.lower():
                break
        

