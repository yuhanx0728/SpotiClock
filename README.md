# SpotiClock

Spotify Alarm - Play a specific song as your alarm clock using Spotify

Utilizing [IFTT recipe](https://ifttt.com/recipes/283707-spotify-alarm-clock)
In your mail client:

Create a rule in your mail client with the following properties
- Message content contains #wakeup
- Actions: Delete Message, Run AppleScript

Create an AppleScript with the following statements.
```
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
```

Voila!
