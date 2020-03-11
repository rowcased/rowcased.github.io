# Codewars.com

#### The Site

<!-- <a href="https://codewars.com">Codewars</a> -->
Codewars is a very active user-driven site offering thousands of coding challenges in 48 languages. Borrowing from _Kendo_, challenges are called 'kata', a 'kyu' rank system is used, and points are known as 'honor'. As a member earns higher honor, they are granted additional site privileges.

#### My involvement

First I only <a href="https://rowcased.github.io/codewars.html#solver">solved</a> kata in Python to learn coding. C was next and I began <a href="https://rowcased.github.io/codewars.html#translator">translating</a> kata to that language. As my proficiency grew I added many new languages and started <a href="https://rowcased.github.io/codewars.html#creator">creating</a> original kata. While advancing through the ranks, I evolved from user to contributor into an ad hoc site <a href="https://rowcased.github.io/codewars.html#moderator">moderator</a>.

<h2 id="solver"><br>1. Problem Solver</h2>

I had zero skill when I signed on, but quickly learned how to learn; studying other coders' solutions, reading the comments, and using tutorials. I found solving a kata in multiple languages offered invaluable insights into coding, as well as how to use documentation to more rapidly learn a new language.

* 2kyu ~ rank (began as 8kyu)
* 136 ~ leaderboard position 
* 15,708 ~ honor points 
* Top 0.069% ~ honor percentile
* 2,117 ~ number of distinct solved kata
* 1,030 ~ resolved in multiple languages
* 3,147 ~ total correct solutions<br><br>
```
Python      1,706
JavaScript    519
C             478
Ruby          115
C#             78
C++            69
Java           65
27 others     117
```


  * Python&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1,706
  * JavaScript&nbsp;&nbsp;&nbsp;&nbsp;519
  * C&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;478
  * Ruby&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;115
  * C#&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;78
  * C++&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;69
  * Java&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;65
  * 27 others&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;117
  * <h style="white-space: pre-wrap;">27 others          117</h>
  * <p style="white-space: pre-wrap;">27 others          117</p>
  * <pre style="white-space: pre-wrap;">27 others          117</pre>
  
<h2 id="translator"><br>2. C Translator</h2>

When I began C, I so was fascinated by how it differed from Python that I started creating translations into C for use on the site. I learned about code structure quality, and especially writing strong unit tests. I like the idea that coders around the globe are using my test suites to improve their skills.

* 132 ~ number of my [C translations available on Codewars](/C_translations)
* 19.4% ~ percentage these make of all 680 approved C kata
* 14,926 ~ number of valid solves made collectively worldwide

```python
# an example of a simple Python function
def say_hello(name):
    greet = "Hello, {}!".format(name)
    print(greet)
    return greet
```
```c
// the equivalent code translated to C
#include <stdlib.h>
#include <string.h>
#include <stdio.h>

char *say_hello(const char *name) {
    size_t n = strlen(name);
    char *greet = (char*) malloc((n+10) * sizeof(char));
    sprintf(greet, "Hello, %s!\n", name);
    printf("%s", greet);
    return greet;
}
```

<h2 id="creator"><br>3. Kata Creator</h2>

Codewars is built entirely on user contributions. A new kata begins in a beta stage under the scrutiny of moderators where any issues must be resolved and satisfaction must reach 80% prior to approval. Each kata I created was well-received and also translated to new languages by other members.

1 [is_sator_square](https://rowcased.github.io/is_sator_square)<br>
<!-- &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The first kata was based on a stone tablet found at Pompeii, known as a "sator square". It is an form of two dimentional palindrome admitting four symmetries. The coder of this kata must study the pattern of characters on the square and determine whether it conforms to the regulations of a sator square. -->

2 [build_square](https://rowcased.github.io/build_square)<br>
<!-- &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This one was based on my experience playing with toy blocks with my daughter and as a kid myself. I simply created a challenge for the coder to determine if a square could be built out of the available different-sized blocks. -->

3 [mutations](https://rowcased.github.io/mutations)<br>
<!-- &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This kata was inspired by playing word games on road trips. This game involves altering a word by changing one letter. The coder is tasked with running a game between two fictional players who are trying to think up new words, such that the program determines the winner of the game. -->

* 1,276 ~ number of members attempting my kata
* 352 ~ number correct solutions submitted
* 93.6% ~ average satisfaction rating

<h2 id="moderator"><br>4. Site Moderator</h2>

One of the interesting features if Codewars is that it's maintained by its own members, which is largely an unofficial network of power-users with full site privileges. On any given day I may take part in a variety of activities that assist other members or contribute to maintaining the quality of the site.

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

