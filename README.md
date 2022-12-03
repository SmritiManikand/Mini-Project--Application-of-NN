# Mini-Project--Application-of-NN

## TEXT TO SPEECH CONVERSION:

## ALGORITHM:

1.Import the necessary packages

2.Initialize the recognizer

3.Function to convert text to speech

4.Using google to recognise audio

## PROGRAM:
```py
import speech_recognition as sr
import pyttsx3
r = sr.Recognizer()
def SpeakText(command):
     
    
    engine = pyttsx3.init()
    engine.say(command)
    engine.runAndWait()
while(1):   
try:
    with sr.Microphone() as source2:
    r.adjust_for_ambient_noise(source2, duration=0.2)
    audio2 = r.listen(source2)
             
 
            MyText = r.recognize_google(audio2)
            MyText = MyText.lower()
 
            print("Did you say ",MyText)
            SpeakText(MyText)
             
    except sr.RequestError as e:
        print("Could not request results; {0}".format(e))
         
    except sr.UnknownValueError:
        print("unknown error occurred")
        ```
## OUTPUT:

## RESULT:
Thus the text to speech conversion is implemented successfully.
