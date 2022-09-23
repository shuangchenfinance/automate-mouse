# automate-mouse
Goal: To automate mouse and keyboard on repetitive tasks.
Author: Shuang Chen (chenshuangjiayou@gmail.com)
Date: Sep 23, 2022.

This example is to download ESG scores for each Chinese stock in iFinD database.

Code highlights:
1. to customize for your own monitor, use
http://www.brenz.net/snippets/xy.asp#:~:text=Cursor%20X%20%26%20Y%20Coordinates%20plus,with%20the%20'z'%20accesskey.
to update the cursor X & Y coordinates.
2. pymouse sets double click as default, which can be problematic. 
I recommend using pyautogui for a single click.
3. the scroll command is to simulate the wheel on the mouse, so you can scroll
the page up or down. It's also useful for drop-down options.
4. the software can respond at different speeds for different stocks, 
time.sleep() is to give the software enough response time.

Before running the code:
1. manually download for one stock in order to let iFinD remember the download
path and that ESG score is the first information the user wants to check.
2. make sure your iFinD screen is on the stock list page,
and the first stock you want to download is at the top of the stock list.

During running the code:
1. check the program regularly because the screen can be disrupted by pop-up emails, news, etc.
2. this code is designed for stocks with an ESG score history longer than 5 years.
For some stocks, the ESG score history is too short and the code may not capture it properly.
The only consequence is that ESG scores for these stocks are not downloaded at all. 
Because it's difficult to evaluate the length of ESG score history ex-ante,
I recommend adjusting the code and downloading again for these stocks ex-post.
