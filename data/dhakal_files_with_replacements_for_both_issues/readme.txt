The 136M KEYSTROKES Dataset
===================================
http://userinterfaces.aalto.fi/136Mkeystrokes

This is the 136M Keystrokes dataset. 
It contains keystroke data of over 168000 users typing 15 sentences each. The data was collected via an online typing test published at a free typing speed assessment webpage. 

More details about the study and its procedure can be found in the paper:

Vivek Dhakal, Anna Maria Feit, Per Ola Kristensson, Antti Oulasvirta
Observations on Typing from 136 Million Keystrokes. 
In Proceedings of the 2018 CHI Conference on Human Factors in Computing Systems (CHI ’18).

If you have questions, please contact Antti Oulasvirta:
antti.oulasvirta@aalto.fi

----------------------------------
LICENSE AND ATTRIBUTION
----------------------------------

You are free to use this data for non-commercial use in your own research or projects with attribution to the authors. 

Please cite: 

Vivek Dhakal, Anna Maria Feit, Per Ola Kristensson, Antti Oulasvirta
Observations on Typing from 136 Million Keystrokes. 
In Proceedings of the 2018 CHI Conference on Human Factors in Computing Systems, ACM, 2018.

@inproceedings{dhakal2018observations,
author = {Dhakal, Vivek and Feit, Anna and Kristensson, Per Ola and Oulasvirta, Antti},
booktitle = {Proceedings of the 2018 CHI Conference on Human Factors in Computing Systems (CHI '18)},
title = {{Observations on Typing from 136 Million Keystrokes}},
year = {2018}
publisher = {ACM}
doi = {https://doi.org/10.1145/3173574.3174220}
keywords = {text entry, modern typing behavior, large-scale study}
}

----------------------------------
CONTENT
----------------------------------
  
- <number>_keystrokes.txt: 
	the keystroke-by-keystroke log for all test sentences attempted by the user ID = <number>.

- metadata_participants.txt:
	demographic data of users and aggregate statistics such as speed and errors
	
----------------------------------
EXPLANATION OF DATA COLUMNS
----------------------------------

- <number>_keystrokes.txt: 
PARTICIPANT_ID			Unique ID of participant
TEST_SECTION_ID			Unique ID of the presented sentence
SENTENCE				Sentence shown to the user
USER_INPUT				Sentence typed by the user after pressing Enter or Next button
KEYSTROKE_ID			Unique ID of the keypress 
PRESS_TIME				Timestamp of the key down event (in ms) 
RELEASE_TIME			Timestamp of the key release event (in ms) 
LETTER					The typed letter
KEYCODE					The javascript keycode of the pressed key


- metadata_participants.txt:
The field/column names are described as follows (see paper for details):
PARTICIPANT_ID			Unique ID of participant
AGE				
GENDER
HAS_TAKEN_TYPING_COURSE	Whether the participant has taken a typing course (1) or not (0)
COUNTRY			
KEYBOARD_LAYOUT			QWERTY, AZERTY or QWERTZ layout of keyboard used
NATIVE_LANGUAGE		
FINGERS					Choice between 1-2, 3-4, 5-6, 7-8 and 9-10 fingers used for typing
TIME_SPENT_TYPING		Number of hours spent typing everyday
KEYBOARD_TYPE			Full (desktop), laptop, small physical (e.g on phone) or touch keyboard
ERROR_RATE(%)			Uncorrected error rate
AVG_WPM_15				Words per minute averaged over the 15 typed sentences
AVG_IKI					Average inter-key interval 
ECPC					Error Corrections per Character
KSPC					Keystrokes per Character
AVG_KEYPRESS			Average Keypress duration
ROR						Rollover ratio



Note: For some users, Keystrokes are not logged or not displayed correctly. The corresponding javascript keycode is used instead.

