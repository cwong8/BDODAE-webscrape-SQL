# BDODAE-webscrape-SQL

Webscraping the website bdodae.com using Python / Selenium and writing the results into a MySQL database for later use. This is eventually going to be combined with BDO-Optimization once the project is finished.

# My experience

This website was very messy with its coding. There were hidden tables containing the values that I wanted to access and store in a database, but the only way to make those tables visible was to click on them. To do this, I used Selenium WebDriver and emulated the clicks on each box, before scraping. A big problem I faced was when I wanted to close the current tables because sending an ENTER key in the values box would refresh the page, thus killing the connection (i.e. the page became "stale"). To work around this, I found an element that was clickable and not a hyperlink or altered the page past the current row being scraped. This worked for a while before the loop would self-block itself by clicking too fast. So, I had to add delays between clicks and an expected condition to check for visibility of hidden tables. Once that was done, the code ran smoothly and one table of my database was done, with many more to come in the future.
