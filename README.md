# RFID scan2db
This isn't really a serious project or anything.
The intent of this software will be to scan 125khz RFID tags, match the scanned tag's number to a name entry in a database, and then write that name to a Google Doc (if at all possible).
That means I've got several steps to work on (or find existing code for).

1: Read data from an RFID tag. (I have a module capable of reading RFID tags on the way, so I'll have to wait for this to arrive before I can do this part).

2: Compare the card data with the data set in the database and 
	a: Card unknown, not in DB: Flash amber LED, LCD: "Unknown Card", put card # in DB, 2 beeps(?), pass last 5 digits of card to spreadsheet
	b: Card known, no name in DB: Flash amber LED, LCD: "No Name", pass last 5 digits of card, "no name" (and date) on to spreadsheet, 3 beeps(?)
	c: Card read error: Flash red LED, LCD: "Card Read Error" (or whatever fits). Play buzzer if installed (haven't decided if I'm doing a buzzer yet).
	d: Card read, matches DB, has name in DB: Solid green LED, LCD: "%name", single beep(?), name & date passed on to spreadsheet.
	
3: Well, that was confusing. I'll clean up my word salad later.