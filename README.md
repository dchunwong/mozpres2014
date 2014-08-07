#Plain slides and notes. View index.html for presentation!

## ヾ(@^▽^@)ノ
#Summer of WebQA
## Testing, Dashboards, and Labs. Oh My!
Note:
Hi my name's Dylan and I:

- am a WebQA intern this Summer
- am presenting Summer of WebQA: Testing, Dashboards and Labs. Oh My!
- will tell you about my experiences as an intern working at mozilla

-----

##What Did I do?  (・ヘ・)?
- Fix failing tests and add new ones to for Mozilla's websites and B2G.
- Buildout the on-device testing QA Lab in MV.
- Make a quick dashboard for Jenkins B2G tests.
- Talked to bots.

Note:
I touched a lot of things this summer. I worked on:

- Improving and adding tests to Mozilla websites (Sumo, Amo, mcom, mozillians)
- Doing the same for Boot 2 Gecko (Firefox OS, troubleshooting on-device issues)
- Making a dashboard to track test health on Jenkins B2G tests. (Continuous Integration)
- Talked to bots

I worked on more than just testing websites like I expected. 

------

## (⌐■_■)
# Improving Mozilla's website tests
Note:
Improving tests means:

- Fixing tests when they break (locator change to timing issues)
- Investigating Failures
- Adding more tests to cover new pages

------

## (=^･w･^)
#Let's fix *All*
#the failing tests!
### I don't know how to fix this ._.
Note:
I was pretty excited and nervous to start but ran into some roadblocks.

------

#Challenges
- Not used to existing codebase
- Some things deeply abstracted away
- My own human error

Note:

- I had contributed a little before, but sometimes I ran into trouble where I wasn't sure what the test itself was doing. For example a compromise made at the time due to constraints I wasn't aware of.
- Sometimes I needed to dig deeper into py.test, but some tools abstracted variables away and I had trouble figuring out scope or where things came from.
- I made a lot of typos. And a lot of them slipped through and were pushed. Double checking is important! But it was also due to issues that I couldn't solve on my own due to my inexperience. Flashing devices etc.

------

#(・ヘ・)
#What'd I learn?

Note: 
I learned:

- There aren't any stupid questions. Don't be afraid to ask on IRC. People just want to help! I inherently have anxiety online, and I was originally intimidated to ask questions that I thought might be too basic, but that's the whole point of the internship right?
- Take a lot of opinions on the way. Getting reviews incrementally can let you do things right the first time.
- One and Done. Get all the info you need so you can do a task and not need to revisit it.

------

#B2G QA Lab Buildout
<img src="images/labup.jpg" style="height: 500px"></img>

Note:
My other large project was building out the lab here in MV where:

- on-device testing is conducted for Firefox OS
- functional and performance tests are run
- Automated and run by Jenkins
- Phones are upside down, will explain later

------

#I flashed phones.
<img src="images/phone.jpg" style="height: 500px"></img>

------

#*A LOT* of phones.
<img src="images/phones.jpg" style="height: 500px"></img>

Note:
Devices needed to be flashed with lates base images from vendors but some issues:

- Needed to be put into fastboot
- Needed to wait for tests to finish
- Newer scripts fixed this
- adb issues

------

<img src="images/labold.jpg" style="height: 500px"></img>
This is the old setup, still currently used for marketplace tests, but has since expanded. One device per mac.

------

<img src="images/labbig.jpg"></img>
- 26 flame devices, half and half, with 20 others on standby waiting to be setup.
- upside down due to space constraints. Fixing it.
- Tests actually failed
- Two devices per mac mini.
- Needed to juggle flashing ubuntu. Network boot.

------

<img src="images/ammeter.jpg" style="height: 500px"></img>
##Future

Note:
Future:

- ammeters for power management
- more than two devices per mac mini
- an intermediate system to handle flashing of devices
- reporting to treeherder (TBPL replacement)
- JS tests.

------

##(๑☆‿ ☆#)ᕗ
#Tracking B2G Failures with a dashboard.

Note: 
My final project was worked on as a longterm project. A dashboard to track the health of Jenkins B2G Tests

------

#Goal
##Easily view test health over time 

Note:
We want to easily see how tests are doing. If a test fails, is it intermittent? Or is it due to the update etc.

Jenkins has this but cumbersome. (Demo?)

------

## (∩´﹏`∩)
#DEMO
## W.I.P.
[Code Link](http://github.com/dchunwong/scraping)

------

##[≡]〆(・∀・＠)
#Q&A
# \#interns
Note:
##Dashboard

- Currently caches dictionaries used for visualization and shelves file
- Will implement database
- Would redo with angular rather than jquery, but libraries.
- Want to add devices to data too, but more scraping
- Quick lookup test health.

##Lab

- Made a script to standardize setup
- Puppet and other options are being looked into.
- Network install took too long to setup with deadline

##Testing

- Handled some issues, but mostly Jenkins and bugzilla

------

# Will there be plans to include what device a job was run on?

Note: 
Yes, I want to add the ability to see what device a job ran on to determine device issues.

------

# Will you include device health itself also? e.g. see how a particular device is doing across tests.

Note:
Yes, that is anotter good point for adding different views not available in Jenkins.

------

# Will the ammeters be as precise as the current perf tests that report to TBPL?

Note:
I don't have enough information to answer that question.

------

## ＼（＠￣∇￣＠）／
#Thanks Mozilla!
