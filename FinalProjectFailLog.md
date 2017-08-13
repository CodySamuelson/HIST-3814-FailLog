# Final Project: An Analysis on Quebec thoughts on Empire using data visualization
## Introduction
Final project time! My goal is to discover to what degree did turn of the 20th century west quebecers regard themselves as part of Empire? To do this, I will use wget to pull clippings from 1901-1911. Then, I will use Open Refine to clean up the text, and then a data visualization program to communicate the frequency the words "London", "Unitied Kingdom", "Great Britain", or "Empire" were mentioned per year. Considering the proposed points offered by professor James Kennedy in his text, _Liberal Nationalisms: Empire, State, and Civil Society in Scotland and Quebec_, many Quebecers did not necessarily see themselves as a part of the British Empire at the turn of the 20th century. As such, revewing the frequency of these key terms can be used as a measure to determine how accurate this point really is. If the words "London", and "Empire" are mentioned frequently in the _Shawville Equity_, then perhaps Quebecers were more invested in the British Empire than many scholars have suggested. In either case, the following analysis and subsequent presentation of data using digital visualisation will offer important insight into self-identity and nationalism in Quebec at the turn of the 20th century. This project will try to prove that, in line with the historical viewpoint, that Quebecers did not necessarily view themsleves as part of the British Empire, which will be outlined using data-visualisation to highlight the lack of frequency in specific key terms. 
## Contextualizing this Project
It is important to note that the data captured or "taken" in this project is not being measured in a comprehensive fashion meant to capture the context behind the key terms. Rather, the thesis an conclusions put forth from this study will merely be used as an interpretation based on the frequency of the key terms int he given timeline. A more in-depth analysis surrounding the context of the key terms would be useful in rounding out this study and used to make more definitive conclusions.

Additionally, there is the ethics standpoint that must be considered before starting this project. It is interesting that such a small and uncontextualized data-set (in this case choosing keywords) and then using the power of visual statistics to make a broad claim (to what degree did turn of the 20th century west quebecers regard themselves as part of Empire) is, quite frankly, scary. We will never know why or why not certain key terms were used, and even if their frequency of use truly reflects their thoughts and feelings of the British Empire. The mere fact that such claims can be made and "proved" using the following data methods presents a strong argument for the need for constant fact-checking and contextualization when data-visualixation is used in an effort to prove or promote a "fact". 

## Getting Started - Organizing Data
- First, I have to re-learn all of this stuff. I made a new account in DHbox, and am re-watching the professor's video on how to use wget.
- Starting to download years 1901 - 1911 one year at a time using this line of code: *'wget http://collections.banq.qc.ca:8008/jrn03/equity/src/1884/ -A .txt -r --no-parent -nd –w 2 --limit-rate=200k'*. I am just changing the *year* each time. Might have to spend the whole day just gathering the required data.
- All done! I checked off all of the files located in my file manager and started to download them. Not sure if this is the most efficient way to do things.
- Ran into a little problem. I opened all of my 1901 txt files in Notepad++ but there are a lot, and they are all seperate. I need to find a way to merge all of the text into a single file covering all of the text in 1901.
- Now that I have each file seperated by year in DHbox, I am having trouble trying to download these files onto my own computer so I can open them in Notepad++.
- Professor suggested to Google 'concatenate text files terminal'. The suggested path is using the following line of code: cat file1.txt file2.txt file3.txt > file4.txt. 'cat' Signals to the terminal that you want to combine the files, with the names of the files being specified. The _output redirection symbol_ (>) is used to create a new file with the combined text, rather than just having it all appear on the terminal.
- Just manually copied and set up the names of files using the same line of code (took a long time, I should find a better way to do this), and about to try it!
- AND IT DID NOT WORK. Instead stated that it cannot find my files........ I tried to google the issue but have not found any answers yet. Reached out on Slack.
- Ok, I tried opening the folder containing all of the text files (1901) using _cd 1901_. However, when I tried to use the cat line of code again, this time it says that I am _denied permission_. 
- Professor suggested using _sudo_ before _cat_. Tried but still did not work.
- Tried combining all files into _> fred.txt_ since that file name didn't exist yet. Did not work.
- Jeffblackadar is helping on Slack. Suggested _sudo bash -c :cat.... >fred.txt"_. Did not work.
- Jeffblackadar suggested trying _$ sudo bash -c "cat *1901*>1901all.txt"_ to simplify the process. Did not work.
- A file called "_fred.txt_" is being created but it is always empty. Neither of us is sure why.
- Turns out I can open all of the files at once in Open Refine! I will import all of the files in a given year, and then export to a cvs file.
- I ended up exporting it into Notepad++ in order to clean the text up. I wanted to find and delete any lines in all of the 1901 txt files that didn't containt the word "_London_". To do this, I Searched and found some help on Stackoverflow. 

1) First, I went to the Search menu > Find... > Select "Mark" Tab. Activate regular expressions. Search for London. Don't forget to check "Bookmark lines" and Press "Mark All". All the rows I wanted to keep got a bookmark
2) Went to Menu "Search - Bookmark - Inverse Bookmark". All of the lines I wanted to delete were then bookmarked. 
3) Finally, went to Menu "Search - Bookmark - Remove Bookmarked lines". This deleted all of the unwanted bokmard lines.
 
 - OK. So now I have a document that containes all of the lines with the word "_London_" that were written in 1901 in the Shawville Equity. Now I'm getting somewhere.
 - I cleaned up the text a bit in Notepad++ just by deleting some blank spaces. Now I will move on to Open Refine to transform into a strong cvs document. I then deleted the all of the content contained in each line except for each date. I now have a list of years, with each year in the table being an instance where the word "London" was used. For example, if I have 202 instances of 1905 in my document, this means that the word "London" appeared 202 times in the 1905 edition of the _Shawville Equity_.
 - Now to duplicate the process for the other years. The final cvs document containing the data can be found _[here]_(https://github.com/CodySamuelson/FinalProjectHIST3814o/blob/master/London(1901-1911).cvs.csv).
## Data Visualization
- Tried to plug data into RAW, but did not respond correctly. Tried creating a header called _Date_ above each of the columns containing years. This did not work.
- Hmmmm, maybe I'll try to put _Date: Year_ in the top of each column. This did not work either.

 
