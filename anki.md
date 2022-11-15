# Guide to setting up Anki  

_Updated: 14th November 2022_
  
Hello. If you are reading this you are likely a student in 黄老师's Chinese class.

## What is Anki?  
Put simply, Anki is a flashcard app. How Anki differs from manual flashcards that you write physcially is that Anki is [Spaced Repetition Software](https://en.wikipedia.org/wiki/Spaced_repetition) (SRS). SRS is essentially an algorithm that spaces out flashcards so that they appear just as you are about to forget the content. There is a lot of literature and research on how SRS works, so if you would like to read more on it click the link above to read through the wikipedia page on it.  
  
## Why Anki?  
Anki is very popular with language learners, hobbyists and medical students to help them retain information. Language learners tend to like Anki/SRS because it allows them to learn and retain vocabulary a lot easier than with manual repetition/physical flashcards.  
  
Anki is (mostly) free software. It is available for free on Windows, macOS, Linux and Android, although there is a 25USD fee for the app on iOS devices. 
  
Anki has a [huge library of flashcard decks](https://ankiweb.net/shared/decks/) for a wide range of topics from Mandarin, English and Korean to Chemistry, Medicine and Physics.

```
While there is a huge library of pre-made decks, most anki language learners recommend creating 
your own decks and adding your own cards. 
Especially if you are following a course/cirriculum. It is easy to lose track of what you need to learn.
```
  
Anki is very versatile software and can be customised to suit the needs of the user. Because of this, it can be a little intimidating for first time users because there are so many options and ways to customise Anki that it can be overwhelming. 

```
I haven't gone too deep into the customisation side of Anki, I have only set up Anki to how I like to use it.
You may find after using it for a little while that you would like things to work differently 
and Anki allows for that.
```

## What you need
To follow this guide, you need either -  

* A computer running Windows 7 or later, or a Linux operating system of your choice; or
* An Apple Mac device running macOS 10.13.4 or later;
  
## Getting Anki  
Anki is available from the [Anki website](https://apps.ankiweb.net/), the Apple [App Store](https://apps.apple.com/us/app/ankimobile-flashcards/id373493387) (iOS) and the Google [Play Store](https://play.google.com/store/apps/details?id=com.ichi2.anki&pli=1) (Android).  

```
I really recommend setting this up and creating your first deck on a computer first. 
Creating flashcards is a **lot** easier on a physical keyboard and computer than it is on a mobile device. 
When creating cards, the Chinese Support addon only works on computers.
Once you have created the card, you can review it on mobile devices. 
If you only have a mobile device, I will discuss more about this in a (near) future update.
```
  
This guide will show how to setup Anki on macOS, but the instructions are the similar for Windows and Linux users. 
  
Navigate to the anki website using the following link - https://apps.ankiweb.net/. Scroll down to the bottom of the page, select the operating system you're using (Windows, macOS or Linux) and download the previous stable release (2.1.49). We need this version because later on we will install the Chinese Support Addon.  
  
## Starting Anki
When you start Anki for the first time, you will be presented with the main page (which should be empty) and the options to Get Shared, Create a Deck or Import a File. (Don't worry if your window doesn't look like mine. The heatmap is an addon.)

![](/img/1-anki-main-page.png)

First we're going to install the [Chinese Support Addon](https://ankiweb.net/shared/info/1128979221) as this will make creating flashcards a lot easier.  
  
Open the addons page by clicking the tools option in the toolbar. Then select **Get Add-ons..**

![](/img/2-addons.png)  
  
Navigate to the [Chinese Support Redux v0.14.2](https://ankiweb.net/shared/info/1128979221) page in your web browser and paste the code __1128979221__ from the bottom of the page into the `Code:` box in Anki.  
  
It will then begin installing the addon. It may take a little while, the addon is about 60MB in size. You will have to restart anki when the addon is installed.  
  
## Minor addon bug - 14th November 2022  
There is a small bug in the Chinese Support Redux addon that prevents audiofiles being automatically generated. There is no word on when this will be fixed, but we can fix it manually.

On Windows, navigate to the following folder -

`C:\Users\YOUR_USER_NAME\AppData\Roaming\Anki2\addons21\1128979221`

On macOS, navigate to the following folder (you will need to reveal "hidden files". Use `Press the “Command” + “Shift” + “.” (period) keys at the same time.` to reveal Hidden files in finder. They will appear translucent) -

`YOUR_USER_NAME/Library/Application Support/Anki2/1128979221`

Open the file `tts.py` in notepad (Windows) or textedit (macOS).

Scroll down to the line(s) where: 

    def get_google(self):
        tts = gTTS(self.text, lang=self.lang, tld='cn')

and replace the word `cn` with `com` - 

    def get_google(self):
        tts = gTTS(self.text, lang=self.lang, tld='com')

and save the file (make sure it is still called `tts.py`).
  
Once the addon is installed, we can begin creating a **deck** and creating a **preset**.
  
## Setting up a Deck.  
On the main Anki page, at the bottom click "Create Deck". You can call it whatever you like.  
When you have created your new deck, click the cog icon on the right of it in the list and select **options**.  

At the top of the screen where it says "Default (used by X decks), click the down arrow to the right of the **Save** button and select **Add Preset**.  

![](/img/3-preset-options.png)
  
## Deck Presets  

Deck presets are one of things that sets Anki apart from other SRS apps as well as physical flashcards. There is a huge debate and [hundreds of videos](https://www.youtube.com/results?search_query=anki+setup) on how to set Anki up optimally for a wide range of uses (Mostly languages and Medical Students). The general consensus is that **the default settings are __okay__ but can be improved** which is what we're going to do.  
  
When I started out with Anki I initially used [Dr Conan Liu's video](https://www.youtube.com/watch?v=1XaJjbCSXT0) (Warning: It's 30 minutes long, but it explains all the technical stuff about Anki, including research and evidence), so that is what we're going to use here. If you're interested in why the settings are what they are, then please check out Dr Liu's video at the link above. He explains things like what learning steps, graduating intervals, starting east, interval modifiers etc are.  
  
To keep this guide brief, we're just going to copy Dr Liu's settings. You may find that after a while (or some research) that you would like to try out different settings. Go for it! Dr Liu's guide is set up for how he gets the most out of Anki. I used it as a rough guide and it seems comfortable for me with a few minor tweaks. You may watch another video and find you prefer different settings. These are not strict rules for using Anki, only slight improvements on the default settings.  
  
### Daily Limits
___New Cards/Day:___

	You can set this to what you are comfortable with. I personally only like to learn 10-15 new characters a day.

__Maximum Reviews Per Day:__ 
	
	Many users recommend setting this to 9999. 
	The minimum you should set this to is **10 times** the amount you have set new cards/day. 
	You may find if you miss a few days or a week or so of Anki that the review count piles up
	and you may be put off doing your reviews. 
	**DO NOT RESET THE DECK**. Instead, reduce the amount of reviews down to 
	10 times the amount of new cards. **Recommended: 9999**.  
  
Follow the rest of the settings in the next picture -

![](/img/4-actual-settings.png)  

	Thanks to Dr Conan Liu for the above settings.

Make sure you save the preset to the new deck we have created.
## Creating Cards  
  
Now that we've set up a preset, we can set up the Deck.

![](/img/5-new-deck.png)

At the top of the screen, click **Add**. The Chinese support addon has created some card styles for us. Click the button next to Type and make sure **Chinese (Basic)** is selected.

![](/img/6-create-new-card.png)

Make sure to click the 汉字 button at the top.

In the Hanzi box, fill out the Hanzi/汉字 you want to add to the deck. Then press TAB on your keyboard. The fields should automatically populate and an audio file will be generated and attached to the card. Click add.   

```  
The autofill only works with Hanzi/汉字. 
If you mess up you will have to close the window and reopen the Add Card window again.
```

![](/img/7-filled-card.png)

Your new card is now added to the deck and is ready to review!

## Reviewing Cards

The key thing to remember when reviewing cards is that it's ok to get the answer wrong. Don't cheat, don't skip, if you do not remember the card, **click the AGAIN button**. If you do remember the card, **click the GOOD button**. 

```
The big rule here is **Do not click the HARD button**. 
The short reason is that clicking the hard button messes with the card intervals 
(time between when you will see the card again). 
If you want to know the long reason then please watch Dr Liu's video linked 
in the Deck Presets section.
```

![](/img/8-reviewing-cards.png)

Click study now. You will be presented with your first card.  
  
![](/img/9-front-card.png)

This is the **front** of a basic Front/Back card.   

Look at the word, try to recall the answer, then click **Show Answer**

![](/img/10-back-card.png)

When you click show answer, you will be shown the **back** of the card, and will be presented with options.

I will repeat again - if you did not remember the card, **click the AGAIN button**. If you did remember the card, **click the GOOD button**. The big rule here is **Do not click the HARD button**. The short reason is that clicking the hard button messes with the card interval. If you want to know the long reason then please watch Dr Liu's video linked in the __Deck Presets__ section.

By default, the Chinese Support Addon sets up the cards to be English on the front and then  汉字, Pinyin,  + English Definition on the back.   
  
	I personally prefer 汉字 on the front and English, 汉字, Pinyin, Definition on the back. 
	I will cover modifying cards in a (near) future update.

Once you have learned/reviewed all of the cards successfully, that's it! You will be prompted to learn more cards again tomorrow. **Make sure to check for and complete your reviews EVERY DAY**. The beauty of anki is that when you have it synced to your mobile device you can do your reviews anywhere. On the train, in the bathroom, waiting in a queue, eating food etc. Doing reviews every day is really important to keep your review count down. It is also important to review every day because otherwise the interval settings are messed up.

## Notes
I will update this guide further and simplify things because I appreciate this is a lot of information to take in for what should be a simple flashcard app. I also need to cover basic modifying card styles and different card types. I will also cover Syncing decks to ankiweb and using them on mobile devices.
## Thanks
Many thanks to Dr Conan Liu for his videos on Anki and Anki settings.
## Improving this Guide.  
This guide is [Open Source](https://en.wikipedia.org/wiki/Open_source) and I actively encourage people to critique or submit improvements. If you wish to contribute to this guide, please make a pull request in the repository.

  

