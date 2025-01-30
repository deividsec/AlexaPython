import pyttsx3

engine = pyttsx3.init()

voices = engine.getProperty('voices')

for voice in voices:
    if 'brazil' in voice.name.lower() or 'portuguese' in voice.name.lower():
        engine.setProperty('voice', voice.id)
        break

text = "Digite o texto que você deseja que a IA fale" 

rate = engine.getProperty('rate')

engine.setProperty('rate', rate - 10) 

volume = engine.getProperty('volume')
engine.setProperty('volume', min(volume + 0.25, 1.0))   

engine.say(text)
engine.runAndWait()
