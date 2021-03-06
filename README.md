# Practice Interview Questions
1. what is the most influential book or blog you have ever read regarding web development?

A. The most influential book that I currently own, would have to be John resign javascript ninja
a complete concise guide to prototype javascript. This book impacted me when I was learning javascript to build my google play store game "Bruiser's Spring Adventure, by allowing me to conceive the abstraction in more detail, since the game engine I used at the time, cocos2d had only mandarin API documentation.

2. Tell me about a web application you have built. Why did you choose to build
it? What did you learn? What challenges did you face and how did you overcome them?

A.  A web application that I am proud of was one made for the Udacity Full Stack degree called Road Map To Health. At first, this app was just a requirement for my nano degree course, but then it became much more to me, being a person who is interested in health knowledge. The main purpose of the application is an open source database of medical knowledge which allows an authenticated user to create
organ systems of the human body then populate that organ system with a medicine
product that pertains to aiding that system with the options of categorizing by glands and different
types of recognized medicines. I needed to learn the flask framework, SQL, and Python
to complete this project. At first getting my database to be recognized by the app was difficult.
I quickly overcame this barrier by reading the documentation again.


3. Write a function in Python that takes a list of strings and returns a single
string that is an HTML unordered list (<ul>...</ul>) of those strings.
You should include a brief explanation of your code. Then, what would you have
to consider if the original list was provided by user input?
```
def unordered_list(strings):
    #unordered list element
    list = '<ul>'

    #iterate over input
    for s in strings:
        #append and format elements
        lst += '<li>{}<li>\n'.format(s)
         #close off the unordered object
         list += "</ul>"
return list
```
If the data input came from the user then the function would need to check if
the input was a list, not null, and is of type string!

4. List 2-3 attacks that web applications are vulnerable to. How do these
attacks work? How can we prevent those attacks?

4.1 SQL Injection attacks are when an attacker injects SQL code into input fields on a web page. This would allow the attack to do damage such as spoof an identity and or tamper with existing data. One way to protect against SQL injection attacks would be to remember to never trust the user input
and use third-party security code like bleach within your code to sanitize any input from the user.

4.2 Local File Inclusion attacks are when an attacker exploits a dynamic file inclusion by including a file or ../ to the websites un proper validation of user input.
   Typically the webpage being attack would receive an as input the path to the file that has to be included. This would allow for directory transversal further giving the attacker the ability to enter "../". To protect against this type of vulnerability the web application should avoid passing user submitted input to any filesystem and framework API , or at least contain a white list of files to be included by the page and then used as an identifier to be accessed to the selected file, thus allowing any invalid identifier to be rejected.

4.3   Cross-Site Request Forgery(CSRF) attacks tricks the victim into submitting a malicious request. The attacker would then embed this attack into a hyperlink and use either social engineering (sending it through email or chat to the victim directly) or if the site has a database they may store the bad request directly on the site. A victim would now just need to click on the link which opens the web page that their credentials are already stored, thus giving the attacker full access to the victim's data on that web application. One common way to prevent this attack from occurring on your web application would be to simply rely on header values by determining that the origin request is coming from the original source and going to the original target. A recommended second defense practice is to utilize synchronizer tokens, which are a secure random token unique to the user's session.

5. Here is some starter code for a Flask Web Application. Expand on that and
include a route that simulates rolling two dice and returns the result in JSON.
You should include a brief explanation of your code.
```
from flask import Flask
app = Flask(__name__)

import json
import random

@app.route('/')
def hello_world():
 return 'Hello World!'

@app.route('/roll_dice/<int:n>json')
def roll(n):
    rolls = []
    for i in range(n):
    # Comprehenion list of the two random dice rolls
    two_dice = random.randint(1,6) + random.randint(1,6)
        #inserting the data into our array object rolls
        rolls.append(two_dice)

    # Formatted for a json style output
    return json.dumps(rolls)

if __name__ == '__main__':
 app.debug = True
 app.run()
```
6. If you were to start your full-stack developer position today, what would be
your goals a year from now?

A. If I were to start the position today, the goals that I would achieve in one year are
to enhance my skills by learning new object-oriented, object-relational mapper, and frameworks.
I would achieve this goal simply, by continuing my learning experience at Udacity completing a react.js, web application specialist, and an android java nano-degree. Currently enrolled in the Google web challenge course giving me a head start to the completion date of these goals and aspirations. My intent and goals of expanding my development skills are essentially just a milestone, that will not only allow me to be a more robust and efficient programmer but a better asset to the company in which I work for! In summary, giving a year of experience as a full-web developer, whichever company I am working for, I would contribute to the fullest, so that their mission statement is being fulfilled. 
