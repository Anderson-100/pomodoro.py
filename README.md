# pomodoro.py

A simple Pomodoro timer, built in Python. <br>
<br>
To use it, simply download the files and run one of the following commands:
- **Default Mode:** ```python3 pomodoro.py```: *(default theme, 20 minutes work / 5 minutes break / 15 minutes extended break)* 
- **Personalized Modes:** 
  -  ```python3 pomodoro.py {theme or custom setting}```
  -  ```python3 pomodoro.py {work_time} {break_time}```
  -  ```python3 pomodoro.py {work_time} {break_time} {extended_break_time}```
  -  ```python3 pomodoro.py {theme} {work_time} {break_time} {extended_break_time}```

This program runs in a never-ending loop; use `^C` to end it.
(The extended break occurs on every third iteration of the timer.)

**Requires:** 
- [Python 3](https://www.python.org/), due to the implementation of f-strings.
- [playsound](https://pypi.org/project/playsound/) library to play audio.
- [PyObjC](https://pyobjc.readthedocs.io/en/latest/) for playsound to work.

## Custom Settings
Tired of typing out your custom time intervals every time? Now, you can save your unique settings and access them quickly, anytime! 

To create a new custom setting, create a txt file in the `custom_settings` folder and type your desired theme, work time, break time, and extended break time, each on a separate line. Then, the next time you start the timer, just type the name of the file (without the `.txt`) after `python3 pomodoro.py` to use your custom mode! Three examples are given in the folder for reference.

## Themes
Currently, the available themes are:
- `among_us`: Sound effects from the popular 2018 video game Among Us.
- `hype`: *MLG air horn* at the end of the work section, *Bruh Sound Effect #2* at the end of the break.
- `andersons_special`: Combines the emergency meeting sound from `among_us` with the bruh sound effect from `hype`.

**Want to add your own theme?** ***Here's how:***
1. Create a folder within `pomodoro_audio` with the name of your theme.
2. Add 2 audio files (`.wav` format) into the folder. Name one `work_done.wav` and the other `break_done.wav`.
3. Include your theme in the command-line argument the next time you run the program!

## What is Pomodoro?
Pomodoro is a popular studying and productivity technique that combines timed work sessions with breaks in between. For example, one popular configuration is 20-minute block of work with 5-minute breaks in between, although many people will have their own personal preference (including [Animedoro](https://youtu.be/bUjGZJIgse0)).

## Update Log

### 2022-01-06
New year, new features!
Now, you can save your favorite custom settings for quick access. Check the **Custom Settings** section above to see how it works.

### 2021-09-26
Restructured code to make formatting more elegant. Added two new themes: `hype` and `andersons_special`. Also added an extended break that occurs on every third iteration and edited the input arguments to account for that.

### 2021-08-16
Initial commit. Users can choose between the default 20/5 or personalize the time using command-line arguments. Currently uses sound effects from the popular 2018 game Among Us, although I am planning on implementing more themes.
