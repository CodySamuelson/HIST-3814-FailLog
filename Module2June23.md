# Exercise 1:
- Searched Samuelson in this database
- Forgot how to use the nano text editor - time to learn!
- To start using nano, make sure you're in the command line on your DHbox
- After you're logged in, type nano filename.md
- Add all of the information and data locations from my search using the link functions: [words](link)
- Saves the file in Markdown format, and added to my Github repository

# Exercise 2:
- Read the Ian Milligan tutorial on wget, and watch the professor take it step-by-step on helpful-videos
- Remember this line of code when using wget: wget -m -w 2 --limit-rate=20k http://WebsiteName.ca
- I successfully downloaded one file and saved in my Github repository 
- Tried using the following line of code to complete full exercise 2: wget http://collections.banq.qc.ca:8008/jrn03/equity/src/ -A "*188*".txt -nc -r --no-parent -nd - w 2 --limit-rate=20
- After 2 hours it was still not done downloading.... had to cancel and clear
- Will come back to this later and try changing the limit-rate to 40 or something
- Heard back from a colleague on Slack, will set the upload speed to 250
- Still did not work, it did not stop downloading years

# Exercise 3:
- Very difficult to understand. Got some help over Slack, but still having a hard time. Will come back to this later.

# Exercise 4:
- Install jq into DHbox with: sudo apt-get install jq -y
- Notice error message in the program, need to work around this
-After I go into nano and create file - canadiana.sh, I tried to change the permissions to run Milligan's program using hmod 755 canadiana.sh
- Unfortunately this did not work either..... the result being: -bash: hmod: command not found
- Kept trying different options and asked for help on Slack but no response. Will have to ask the professor on Wednesday
