## Codewars.com

#### The Site

<!-- <a href="https://codewars.com">Codewars</a> -->
Codewars is a user-driven website with a highly interactive community, offering thousands of diverse coding challenges in almost 50 supported languages. The site borrows a ‘kyu’ rank system from _Kendo_ and refers to challenges as ‘kata’. Points earned are called _honor_. As increasing levels of honor are achieved, additional site privileges are granted to a member.

#### My involvement

At first I just <a href="https://rowcased.github.io/codewars.html#solver">solved</a> a lot of kata in Python as I learned the basics of coding. Eventually I studied C and started <a href="https://rowcased.github.io/codewars.html#translator">translating</a> kata into that language. Then I began to solve kata in a multitude of  new languages. I also finally <a href="https://rowcased.github.io/codewars.html#creator">created</a> several original kata. As I earned additional honor and advanced through the ranks, I evolved from user to contributor into an ad hoc site <a href="https://rowcased.github.io/codewars.html#moderator">moderator</a>.

<h3 id="solver"><br>1. Problem Solver</h3>

Being new to coding as I began Codewars, I was baffled by some challenges and some early solutions were inefficient. I rapidly learned about algorithm best practices by reading comments and studying other people's solutions. Solving a kata in multiple languages offered invaluable insights to coding. I never imagined I would solve so many kata and learn as much as I have.
<br>
* 2kyu ~ rank (began as 8kyu)
* 137 ~ leaderboard position 
* 14,992 ~ honor points 
* 0.074% ~ honor percentile
* 3,054 ~ total correct solutions
    * 2,037 is the base number of distinct solved kata
    * 1,017 represents resolving in multiple languages
<br>
```
Python     1,646
JavaScript   483
C            450
Ruby         105
C#            69
C++           63
Java          53
27 others    115
```

<h3 id="translator"><br>2. C Translator</h3>

One day I tried translating a kata from Python to C. It was reviewed by a moderator, I made some revisions, and it was approved for use on the site. I really enjoyed this process and just kept on translating. I like the idea that coders around the globe are using my test suites to improve their skills. I learned about code structure, maintainability, and writing strong unit tests.

* 125 ~ number of [C translations available for use on Codewars](/C_translations)
* 18.9% ~ percentage these make of all 662 approved C kata on site
* 5,000 ~ number of valid solves made collectively worldwide


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

<h3 id="creator"><br>3. Kata Creator</h3>

Codewars is built on user contributions. New kata begin in a beta stage, being scrutinized by moderators. Issues must be resolved and satisfaction must reach 80% prior to approval. Many never make it out of beta; it's hard to create new material for a site with over 8,000 kata! All three of mine were approved and were also translated to new languages by other members.

1 [is_sator_square](https://rowcased.github.io/is_sator_square)<br>
<!-- &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The first kata was based on a stone tablet found at Pompeii, known as a "sator square". It is an form of two dimentional palindrome admitting four symmetries. The coder of this kata must study the pattern of characters on the square and determine whether it conforms to the regulations of a sator square. -->

2 [build_square](https://rowcased.github.io/build_square)<br>
<!-- &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This one was based on my experience playing with toy blocks with my daughter and as a kid myself. I simply created a challenge for the coder to determine if a square could be built out of the available different-sized blocks. -->

3 [mutations](https://rowcased.github.io/mutations)<br>
<!-- &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This kata was inspired by playing word games on road trips. This game involves altering a word by changing one letter. The coder is tasked with running a game between two fictional players who are trying to think up new words, such that the program determines the winner of the game. -->

* 1217 ~ number of members attempting my kata
* 340 ~ number correct solutions submitted
* 93.6% ~ average satisfaction rating

<h3 id="moderator"><br>4. Site Moderator</h3>

One of the greatest features of Codewars is that it is mostly maintained by an unofficial network of moderators (power-users) that have earned site privileges through earning honor points. However, members that abuse their authority can be banned. On any given day I may take part in a variety of activities to help maintain the site and improve its overall quality. 

* answer questions on the dashboard
* address suggestions made for kata
* directly edit live production code
* post issues on kata with faults
* resolve kata issues (often bogus)
* assist newer members debug their code
* vote on new beta kata submissions 
* rank new beta kata submissions
* report unethical / forbidden behavior
* approve new kata for use on site
* approve or reject kata translations
* add / adjust kata test suites
<br><br><br><br><br><br><br><br><br><br><br><br><br>

<a href="https://rowcased.github.io/">(return to portfolio)</a>

<!-- For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/). -->
