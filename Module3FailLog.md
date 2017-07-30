# Exercise 1:
- Open Notepad++
- Open copy of "[Diplomatic correspondence of the Republic of Texas](https://archive.org/stream/diplomaticcorre33statgoog/diplomaticcorre33statgoog_djvu.txt)".
- Not sure how to copy full text since it's so long, time to ask Slack. Off to a wonderful start!
- Got an answer! Downloaded and opened the text in Notepad++.
- Except it didn't work - just a bunch of random symbols....
- Ok let's try this again. This time I just copied the index.
## Step 1:
- Open the find tab using *crt+f*. Click on the Replace tab next to it, and check off 'Regular expression'.
- In order to filter out relevant info, type in *(.+\<to\>)* in the Find box, and *~\1* in the Replace box.
## Step 2:
- It worked! Now to remove all of the lines without the tilde. Type *\r\n[^~].+* into the Find box, and leave the Replace box emtpy to delete irrelevant lines.
- This did nothing. Tried *\n[^~].+* as well but it deleted all of my lines with tilde's. Time to go back to Slack...
- Searched on Stackoverflow and it worked!! Used *^[^~]*$* instead. Posted on Slack to help others out. Because I am nice.
## Step 3:
- \n\r was not working, so I went on Stackoverflow again. Turns out Notepad++ has a built-in function that can delete blank lines!
## Step 4:
- Typed *(,)( [0-9]{4})(.+)* in the Find box.
- Then in the Replace box, type in /2 to indicate only wanting to keep the second parentheses (the date).
- This took some time to figure out, had to watch the professor's [video](https://www.youtube.com/embed/yQzfJsyfMNw) for help!
## Step 5:
- Remove box, typed ~, Replace box have nothing.
## Step 6: 
- Type in /to> in the Find box to search for all examples of "to" in the text, Replace with a ",".
## Step 7:
- Type *.+,.+,.+* into the Find box, and change all of the errors in the document! Done and saved :).

# Exercise 2:
- Downloaded _Open Refine_.
- Create project named *m3-exercise2*.
- Open Cluster & Edit column in *Sender*. Slect nearest neighbour method. 
- This is actually fun! Basically run through different options for merging files, using my own discretion at which ones should be merged.
- Complete for both *Sender* and *Recipient*.
- Afterwards, finish cleanup by editing cells, and export the file as a Comma Separated Value!
- Rename as *Source* and *Target*, uncheck *Date* when exporting. Save on Github.
- Dropped into Palladio! Super cool, now only shows Source and Target, automatically removed the Date! Everything is so clean and easy to read.

# Going further with Open Refine
- I'll do my best to actually try to go further. Had more fun than I thought I would.
- Welp, can't figure out how to add the extension. Asked in Slack for help!
