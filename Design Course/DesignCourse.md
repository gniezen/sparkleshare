# Gaps

* Sharing a calendar between two people, where one prefers an electronic version, and the other prefers a conventional paper version
* A tool to adjust the radiator valve that's just out of reach behind my wardrobe cabinet
Remembering to take my staff card to work each morning, e.g. use RFID scanner to check if I have it on me
* A frame for hanging two portraits next to each other, where there is only one screw on the wall
* An ambient device that motivates me to go to the gym
* A case or enclosure for my Raspberry Pi to use as media centre
* A wall hook design for hanging jackets, without having to drill holes in the wall
* Measuring my electricity/gas usage by detecting the number of revolutions per minute of the meter
* Motivating the cat to use her scratch pole
* Setting up a workbench with tools for soldering, cardboard modelling etc. in a small study

Gap: Sharing a calendar between two people, where one prefers an electronic version, and the other prefers a conventional paper version

My fiancé prefers a conventional paper calendar, while I prefer to schedule my appointments on my computer and sync it to my various devices. I have discussed this issue with some of my friends and colleagues, and it turns out they experience similar issues. I have experience in both hardware and software design, so I believe I can come up with a design and prototype for this problem in the allocated time. I'm looking forward to taking a more design-centred approach to addressing the gap, while still using my programming and electronics skills.

# The 5 why's
*In what way may I*

- bridge the digital and the real world
- increase communication between partners
- keep partners up to date on events
* share a calendar between two people, where one prefers an electronic version, and the other prefers a conventional paper version
- build a device that can be updated both electronically and using handwriting


# User needs

_The calendar allows for writing by hand and recognises my handwriting_
The calendar recognises my handwriting
The calendar can be written on
The calendar has a storage place for my pen
The calendar has enough space for all my events

_The calendar can be synchronised easily with my devices_
The calendar automatically synchronises with my mobile phone
The calendar synchronises with my computer
The calendar can recognise and synchronise handwritten entries 
The calendar can be synchronised with other calendars in the house
The calendar can be synchronised between multiple households
The calendar can show event requests from friends

_The calendar fits into my life_
The calendar is affordable
! The calendar does not need to be recharged often
The calendar can be stuck to the fridge
The calendar can be read in bright daylight
The calendar's form fits in the kitchen
The calendar can be cleaned easily
The calendar is unobtrusive
! The calendar should show when somebody else is entering an event

_The calendar can be customised to my liking_
The calendar is available in different colours
The calendar's cover can be customised or swopped out for another one
! The calendar shows maps or pictures of event locations

_The calendar has clock features_
The calendar shows the whole month's events at a glance
The calendar shows the current date and time

_The calendar is easy to use_
The calendar can show events more than a year in advance
The calendar works with all mobile devices
The calendar automatically resolves event conflicts


Problem statement: 

Sharing a calendar between two people, where one prefers an electronic version, and the other prefers a conventional paper version.

Primary needs:

The calendar allows for writing by hand and recognises my handwriting
The calendar can be synchronised easily with my devices
The calendar fits into my life
The calendar can be customised to my liking
The calendar is easy to use
The calendar has clock features, like the current date/time


User feedback:

- The writing area needs to be larger
- The current month should be indicated
- The calendar itself could be a bit bigger (cost-dependent)


## Week 6
Please note: Due to the complexity of the project, a single comprehensive prototype is not yet feasible. As the form factor and functionality of the device was evaluated and finalised during the previous weeks, various components still needed to be evaluated, as shown below.

#Output: E-Ink Display
As the calendar should be easy to read in bright daylight and not have to be recharged often, an e-ink display must be used. For the e-ink display, I want to reuse the display from an Amazon Kindle.  Due to economies of scale, the Kindle e-reader itself (£69) is comparable in price to buying a separate e-ink display component (around £50 on eBay), and easier to use in a prototype.

For the calendar rendered on the display, my first attempt was to use an existing (JQuery-based) calendar plugin. Unfortunately, as it is not optimised for an e-ink display, the text is too difficult to read and it does not render properly, as shown here:

<insert figure>
	
In my second attempt I mocked up my own calendar, with very simple lines and minimalistic icons:

<insert figure>
	
User feedback indicates that the second version is definitely preferable.	

#Input: Handwritten text entry

To mimic the feeling of writing on paper, a stylus-based touch screen is required. This excludes capacitive-type touch screens, like those used in the iPhone. Various resistive-type touch screens were tested, including the ones in the Nokia N900, Nintendo DSi and a palmOne Tungsten E2:

<insert figure>

User feedback indicates that even though the Tungsten E2 has a very small text input area, it is still usable - considering you will only be able to write one letter at a time (to ensure accurate handwriting recognition). It might also be feasible to use the Nintendo DSi touch screen in the prototype, as these can be purchased from Sparkfun: https://www.sparkfun.com/products/8977


