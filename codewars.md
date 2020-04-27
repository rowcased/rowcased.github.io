# Codewars.com

#### The Site

<!-- <a href="https://codewars.com">Codewars</a> -->
Codewars is a very active user-driven site offering thousands of coding challenges in 48 languages. Borrowing from _Kendo_, challenges are called 'kata', a 'kyu' rank system is used, and points are known as 'honor'. As a member earns higher honor, they are granted additional site privileges.

#### My involvement

First I only <a href="https://rowcased.github.io/codewars.html#solver">solved</a> kata in Python to learn how to code. As I began C, I also <a href="https://rowcased.github.io/codewars.html#translator">translated</a> kata into that language. With greater proficiency I added more new languages and started <a href="https://rowcased.github.io/codewars.html#creator">creating</a> original kata. While advancing through the ranks, I evolved from user to contributor into ad hoc site <a href="https://rowcased.github.io/codewars.html#moderator">moderator</a>.

<h2 id="solver"><br>1. Problem Solver</h2>
Signing on with no experience, I had to learn how to learn by studying other coders' solutions, reading their comments, and using tutorials. I soon found solving kata in multiple languages offered many invaluable coding insights, as well as how to use documentation to more rapidly learn a new language.

* 2kyu ~ rank (began as 8kyu)
* 131 ~ leaderboard position 
* 16,618 ~ honor points 
* Top 0.063% ~ honor percentile
* 2,228 ~ number of distinct solved kata
* 1,271 ~ resolved in multiple languages
* 3,499 ~ total correct solutions<br><br>

  * <h style="white-space: pre; font-family: 'Menlo', monospace, Monaco , Courier, Courier New, Lucida Console;">Python      1,794</h>
  * <h style="white-space: pre; font-family: 'Menlo', monospace, Monaco , Courier, Courier New, Lucida Console;">JavaScript    589</h>
  * <h style="white-space: pre; font-family: 'Menlo', monospace, Monaco , Courier, Courier New, Lucida Console;">C      507</h>
  * <h style="white-space: pre; font-family: 'Menlo', monospace, Monaco , Courier, Courier New, Lucida Console;">Ruby      165</h>
  * <h style="white-space: pre; font-family: 'Menlo', monospace, Monaco , Courier, Courier New, Lucida Console;">C#      104</h>
  * <h style="white-space: pre; font-family: 'Menlo', monospace, Monaco , Courier, Courier New, Lucida Console;">Java      93</h>
  * <h style="white-space: pre; font-family: 'Menlo', monospace, Monaco , Courier, Courier New, Lucida Console;">C++      88</h>
  * <h style="white-space: pre; font-family: 'Menlo', monospace, Monaco , Courier, Courier New, Lucida Console;">28 others      159</h>
  
<h2 id="translator"><br>2. C Translator</h2>

My fascination with language differences from Python lead me to create translations to C for use on the site. I learned about code structure quality, maintainability, and especially writing strong unit tests. I like the idea that coders around the globe are using my test suites to improve their skills.

* 145 ~ number of my [C translations available on Codewars](/C_translations)
* 20.6% ~ percentage these make of all 702 approved C kata
* 16,000+ ~ number of valid solves made collectively worldwide

```python
def say_hello(name="World"):
    greet = "Hello, {}!".format(name)
    print(greet)
    return greet               # simple Python function
```
```c
#include <stdlib.h>            //  equivalent code in C
#include <string.h>
#include <stdio.h>

char *say_hello(const char *name) {
    size_t n = name? strlen(name) + 9 : 14;
    char *greet = (char *) malloc(n * sizeof(char));
    sprintf(greet, "Hello, %s!\n", name? name : "World");
    printf("%s", greet);
    return greet;
}
```

<h2 id="creator"><br>3. Kata Creator</h2>

Codewars is built entirely on user contributions. Each new kata begin in a beta stage where it's scrutinized for quality, the author must resolve issues, and it must have 80% rating prior to approval. Each kata I created was well-received and later translated to different languages by other members.

1 [is_sator_square](https://rowcased.github.io/is_sator_square)<br>
<!-- &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The first kata was based on a stone tablet found at Pompeii, known as a "sator square". It is an form of two dimentional palindrome admitting four symmetries. The coder of this kata must study the pattern of characters on the square and determine whether it conforms to the regulations of a sator square. -->

2 [build_square](https://rowcased.github.io/build_square)<br>
<!-- &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This one was based on my experience playing with toy blocks with my daughter and as a kid myself. I simply created a challenge for the coder to determine if a square could be built out of the available different-sized blocks. -->

3 [mutations](https://rowcased.github.io/mutations)<br>
<!-- &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This kata was inspired by playing word games on road trips. This game involves altering a word by changing one letter. The coder is tasked with running a game between two fictional players who are trying to think up new words, such that the program determines the winner of the game. -->

* 1,331 ~ number of members attempting my kata
* 371 ~ number correct solutions submitted
* 93.3% ~ overall satisfaction rating

<h2 id="moderator"><br>4. Site Moderator</h2>

Another great feature of Codewars is that it's maintained by its members; largely an unofficial network of power-users with full site privileges. On any given day I may take part in a variety of activities to assist other members with their code or contribute to maintaining the overall quality of the site.

* answer questions on the dashboard
* address suggestions made for kata
* directly edit live production code
* post issues on kata with faults
* resolve kata issues (often bogus)
* help newer members debug their code
* vote on new beta kata submissions 
* rank new beta kata submissions
* report unethical / forbidden behavior
* approve new kata for use on site
* approve or reject kata translations
* repair & improve kata unit tests
<br><br><br><br><br><br><br><br><br><br><br><br><br>

<a href="https://rowcased.github.io/">(return to portfolio)</a>

<!-- For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/). -->

