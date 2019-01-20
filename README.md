## What
Play a specific song as your alarm clock using Spotify

## How
1. Turn on the [IFTTT recipe](https://ifttt.com/recipes/283707-spotify-alarm-clock), or create a new applet in IFTTT that sends you an email with #wakeup in the email body at the your wakeup time.

2. Create a rule in your mail client with the following properties:
- Message content contains #wakeup
- Actions: Delete Message, Run AppleScript(as below)

3. Create an AppleScript with the following lines:
'''
tell application "Spotify" to activate
delay 5
tell application "System Events"
	key code 37 using command down
	delay 2
	keystroke "<name and artist of the song>"
	delay 10
	repeat 3 times
		key code 48
	end repeat
	delay 2
	key code 76
	delay 2
	key code 36
end tell
'''

## Note
Make sure you have Spotify on your device.
You have to keep your device on and connected to Internet to make sure the AppleScript runs successfully.


## Thoughts
It was fun learning AppleScript - the level of automation enabled by it is amazing.

*This is inspired by and forked from https://gist.github.com/anonymous/784de37358b27f5c7071*
