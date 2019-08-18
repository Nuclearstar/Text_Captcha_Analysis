# Text_Captcha_Analysis

This is an implementation of System_Programming_Project in python.

## SYSTEM IMPLEMENTATION

The lexer parsing of text captcha is done in 4 diﬀerent phases. 

- First phase is ’Fetching’ wherein we download the text captcha ﬁle, convert it into string, parse the XML that we downloaded. Here the XML string is parsed into a Document Object Model (DOM) called as minidom. Then we retrieve the ﬁrst XML tag that the parser ﬁnds with name tagName. Then send it to next phase. 

- The second phase is Cleaning. Here we mainly try to extract numbers and expected extra words like ”what”, ”who”, ”digits”, ”which”, ”number”, ”these”,etc. 

- The third phase is Scanning. Here we scan diﬀerent formats of numbers,names, colours, positions, mathematical equations signs, total count, comparison words, body parts, day reference, list reference,etc which forms the most important part of the project. 

- The fourth phase is Head selection. Here we categorize into digits, relations, range of values, count of body parts, colour,name, mathematical, positional,etc based upon the results obtained from fetch and clean phases and return the processed data. Here in this phase we mainly make use of retrieval based NLP where in required data sets are already provided in the form of list for head selection process. 

- The last part is translation which combines all 4 phases together and helps in solving text captcha challenge.
1) First we obtain text captcha from ”http://api.textcaptcha.com”.

2)  Send it to fetch and clean phase to obtain required tokens.

3) Then send the token one by one to scan phase to know what kind of token it is.

4) The scanned tokens are then sent to head selection to know which all categories/levels, the tokens fall into.

5) After the head selection is done the required answer for the challenge is ready and is properly printed on the terminal window.
