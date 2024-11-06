Backup of https://upriseri.com/DeleteTweets.js

# Instructions

## One-Time Setup Instructions

1. [Download](../../raw/refs/heads/main/DeleteTweets.js) the open source “Delete Tweets” javascript file to your computer (right click the link and click Save).
2. Open the file using a text editor, such as Notepad (Windows) or TextEdit (Mac). The file will have a bunch of javascript code and if you’re not a developer, it will look foreign to you. Don’t worry. The next steps are easy.
3. Keep that file open in your text editor, but go back to your browser, visit your Twitter profile page, and open up Developer Tools. In Chrome, just hit the F12 key to do this. On Mac’s with Safari, it’s Option-Command-C. Now you will see more stuff you probably don’t understand. No worries. Let’s continue. By the way, these steps 1-8 you only have to do once. When you want to bulk delete tweets again in the future, it’s much easier.
4. With Developer Tools open in your browser, click the tab at the top that says “Network”. Below that you’ll likely see the word “All” highlighted. To the right, find and click the link that says Fetch/XHR or just XHR.
5. Now, there is a column called “Name” with a bunch of events popping in and out. If you don’t see anything, reload the page by tapping the F5 key. Now, click any event that starts with “client_event”.
6. On the right, find the line that says “Authorization” and has a huge code to the right that may start with “Bearer”. Highlight and copy that entire code (CTRL-C, or Command-C)
7. Go back to that file you opened in your text editor. At the top, paste the code you just copied between the quotes where you see “PASTE YOUR AUTH CODE HERE”. Go back to your browser and a few lines down from Authorization, find X-Client-Transaction-Id. Copy that code and paste it to the text file a few lines down where you see “PASTE YOUR X-CLIENT TRANS ID HERE”.
8. Almost done. In the text file, towards the top where you see “PASTE YOUR X-CLIENT-UUID HERE”, paste this between the quotes: 2f0m9a61-39aa-8edc-8222-81140d2f4d9b (you can actually make up any code you want here, but this one works).
9. Last one. Again, in the text file a few lines down from the last entry, find “YOURTWITTERHANDLEHERE” and put your actual Twitter (X) handle between the quotes (eg. joe_shmoe123987). That’s it. Setup is done. You won’t have to do these steps again.

## Each Time Instructions

1. The “hard” part is done. Now, you decide the range of tweets to delete. A little way down the text file, find the lines that start “after_date” and “before_date”. This is the range of tweets to delete. Starting values are already entered for you. Follow the same format. So if the “after_date” is 2023-01-01 it will not delete any tweets before that date. Those will be saved. If the “before_date” is 2023-06-01 it will not delete any tweets after that date. Everything between those dates will get shitcanned. Once you’ve set your dates copy the **entire** text file (CTRL-A or Command-A to highlight and then CTRL-C or Command-C)
2. Go back to your browser and go to your Twitter profile page. If you want just your own original tweets deleted stay here, if you want retweets and replies deleted, click on your Replies tab.
3. Bring up Developer Tools again (F12 in Chrome, Option-Command-C in Safari). Click the Console tab at the top. You should see an arrow prompt in the bottom window. Paste the entire text file you just copied there. Hit enter. Let it run. Depending on how many tweets you have to delete it could take awhile. Consider deleting in batches, a few months or a year at a time.
4. Once it is finished the bottom line will say “DELETION COMPLETE (if error happened before this may be not true)”.
5. The next time you want to delete tweets, just edit the dates in the file, copy and paste it into the Console window in your browser’s Developer Tools and hit enter.
