## Codewars.com

#### The Site

<a href="https://codewars.com">Codewars</a> is a user-driven website with a highly interactive community, offering thousands of diverse coding challenges in almost 50 supported languages. The site borrows a ‘kyu’ rank system from _Kendo_ and refers to challenges as ‘kata’. Points earned are called _honor_. As increasing levels of honor are achieved, additional site privileges are granted to a member.

#### My involvement

At first I just <a href="https://rowcased.github.io/alternate_page.html#solver">solved</a> a lot of kata in Python as I learned the basics of coding. Eventually I studied C and started <a href="https://rowcased.github.io/alternate_page.html#translator">translating</a> kata into that language. For a while I solved kata in a multitude of  new languages. I also finally <a href="https://rowcased.github.io/alternate_page.html#creator">created</a> several original kata. As I earned additional honor and advanced through the ranks, I evolved from user to contributor into an ad hoc site <a href="https://rowcased.github.io/alternate_page.html#moderator">moderator</a>.
<hr>
<h3 id="solver"><br>1. Solver</h3>

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
<hr>

<h3 id="translator"><br>2. Translator</h3>

One day I tried translating a kata from Python to C. It was reviewed by a moderator, I made some revisions, and it was approved for use on the site. I really enjoyed this process and just kept on translating. I like the idea that coders around the globe are using my test suites to improve their skills. I learned about code structure, maintainability, and writing strong unit tests.

* 122 ~ number of [C translations available for use on Codewars](/C_translations)
* 18.5% ~ percentage these make of all approved C kata on site
* 5,000 ~ number of valid solves made collectively worldwide
<!--
```python
def str_sum(a, b): # some Python code:
    c = str(a + b)
    print("{} + {} = {}".format(a, b, c))
    return c
```
```c
#include <stdlib.h> // translation to C:
#include <string.h>
#include <limits.h>
#include <stdio.h>
#define ull unsigned long long

char *str_sum(ull a, ull b) {
    if(ULONG_MAX - a < b) {
        printf("Overflow Error\n");
        return NULL;
    }
    char local[21];
    sprintf(local, "%llu", a + b);
    size_t m = strlen(local);
    char *c = (char *) malloc((m + 1) * sizeof(char));
    strcpy(c, local);
    printf("%llu + %llu = %s\n", a, b, c);
    return c;
}
```
-->
<hr>
<h3 id="creator"><br>3. Creator</h3>

Codewars is built on user contributions. New kata begin in a beta stage, being scrutinized by moderators. Issues must be resolved and satisfaction must reach 80% prior to approval. Many never make it out of beta; it's hard to create new material for a site with over 8,000 kata! All three of mine were approved and were also translated to new languages by other members.

1 [is_sator_square](https://rowcased.github.io/is_sator_square)<br>
<!-- &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The first kata was based on a stone tablet found at Pompeii, known as a "sator square". It is an form of two dimentional palindrome admitting four symmetries. The coder of this kata must study the pattern of characters on the square and determine whether it conforms to the regulations of a sator square. -->

2 [build_square](https://rowcased.github.io/build_square)<br>
<!-- &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This one was based on my experience playing with toy blocks with my daughter and as a kid myself. I simply created a challenge for the coder to determine if a square could be built out of the available different-sized blocks. -->

3 [mutations](https://rowcased.github.io/mutations)<br>
<!-- &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This kata was inspired by playing word games on road trips. This game involves altering a word by changing one letter. The coder is tasked with running a game between two fictional players who are trying to think up new words, such that the program determines the winner of the game. -->

* 1217 ~ number of attempts made by codewarriors
* 340 ~ number correct submitted solutions 
* 93.6% ~ average satisfaction rating
<hr>
<h3 id="moderator"><br>4. Moderator</h3>

1 answer questions<br>
2 create issues<br>
3 resolve issues<br>
4 edit anykata<br>
5 votes matter<br>
6 approve / reject translations or kata<br>
7
&nbsp;&nbsp;&nbsp;&nbsp;indent me


::::indent me


> indent me


* indent me


** indent me


*** indent me



One of the greatest features of Codewars is the community of members that develop and maintain the site. Most of the day to day activity is managed by a large set of highly active and very talented programmers

oh, and you can get banned or punished
fix kata
answer questions
raise issues on kata
resolve issues, mostly wrongs, but sometimes I fix a problem

could add a test, change a parameter, alter syntax or name-casing according to language, 
creating or resolving issues, answering questions, as well as improving the site by directly live-editing the production code of other code author's kata material.

moderator; in providing maintenance to kata, ranking beta submissions, and guiding new users.

Because rank, did stuff... in answering questions and repairing issues with faulty kata
 There is no pay, but the hours are good. I have no real authority, although I do have the power to make some changes. I like that I have earned the ability to alter things on the website, so I respect that power and tread very carefully. 
<hr>
<a href="https://rowcased.github.io/">(return to portfolio)</a>

<!-- For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/). -->

