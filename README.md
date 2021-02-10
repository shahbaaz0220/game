#notification of health

import pyttsx3

engine=pyttsx3.init('sapi5')
voices=engine.getProperty('voices')
print(voices[1].id)
engine.setProperty('voice',voices[1].id)
def speak(audio):
    engine.say(audio)
    engine.runAndWait()
def tab():
    import time
    import datetime
    from plyer import notification

    if __name__ == '__main__':
        while True:
            hour = int(datetime.datetime.now().hour)
            if hour <= 0 and hour > 12:
                speak("good motning iam your health assistant")
            elif hour >= 12 and hour <18:
                speak("good afternoon iam your health assistant")
            else:
                speak("good evening iam your health assistant")
            speak("you have high blood sugars, and Type 2 diabetes is not going to kill you. But you just have to take medicines right, and you will be fine for the rest of ypur life")
            speak("its time to take tablets")
            speak("take GP.5 1 tablet now")
            notification.notify(
                title='drink',
                message='take GP.5 1 tablet now ',

                
                timeout=2
            )
            speak('eat GP.5 1 tablet now ')
            #in rime.sleep() we can set after every 6 hours i.e..after every 21,600 second it will show notification
            time.sleep(1)
            break



def speak(audio):
    engine.say(audio)
    engine.runAndWait()



if __name__ == '__main__':
         tab()
