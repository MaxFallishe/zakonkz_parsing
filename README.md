# zakonkz_parsing
Project parsing current news from the site zakon.kz using selenium

## Getting Started

To deploy project on Windows download a copy of the repository and install all the dependencies indicated in the file requirements.txt, when deploying a project to Linux, you may have to resolve conflicts with the web driver 

## Additional Information

### Project Structure and Folder Assignment

File name                              | File content
---------------------------------------|----------------------
chrome_folder                          | contains chrome_driver for selenium to work correctly
excel_template                         | contains a template for data scrawled from zakon.kz
.Idea and venv                         | are designed to run the project correctly through PyCharm IDLE
requirements.txt                       | required dependencies
Example of the resulting Excel file    | as an example of successful program execution contains an Excel table with received data from zakon.kz on 07/04/20 (16:05 Nur-Sultan)


### Column values for the excel table

Column name            | Column value
-----------------------|---------------------------
article_header         | Article title
current_news_date      | Date of publication of the article in the format YYYY-MM-DD
article_comments_count | The number of comments on the article
article_text_content   | Article text
article_comments       | The text of all comments on the article (no separation between comments)


### Features of working with the site zakon.kz

1. The test task states that you need to get only today's news from zakon.kz/news,
however, at certain points in time, mainly after 12 am and the next 10 - 15 hours,
The zakon.kz/news page also contains news from the last day. Sorting is used as a solution.
today's news from yesterday.

2. The number of comments, as well as the comments themselves, are loaded on the pages of individual articles only when
uniform scrolling from top to bottom, moving down the page does not load the comment block. How the solution was used
Unlimited, uniform scrolling with interruption while loading a block of comments.
3. A certain number of articles zakon.kz is on the old (alternative) version of the site, which is why
parsing is provided in the program code from both the current and alternative versions of the site.
4. The "Bypass by IP" function is implemented and tested using free proxy from the site http://spys.one/,
however, the code is commented out due to inconsistent connection with free proxies.
5. With frequent test requests from the proxy server, no attempt was made from the service side
block the parser, or provide it with incorrect data.





