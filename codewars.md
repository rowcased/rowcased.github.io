# Codewars.com

<h4 style="text-align:left;">The Site</h4> <!-- <a href="https://codewars.com">Codewars</a> -->
Codewars is a very active user-driven site offering thousands of coding challenges in 50+ languages. Borrowing from _Kendo_, challenges are called 'kata', points are known as 'honor', and a 'kyu' rank system is used. As a member earns higher honor, they are granted additional site privileges.

<h4 style="text-align:left;">My involvement</h4>
First I only <a style="font:bold;" href="https://rowcased.github.io/codewars.html#solver">solved</a> kata in Python to learn how to code. As I began C, I also <a href="https://rowcased.github.io/codewars.html#translator">translated</a> kata into that language. With greater proficiency I added more new languages and started <a href="https://rowcased.github.io/codewars.html#creator">creating</a> original kata. While advancing through the ranks, I evolved from user to contributor into an ad hoc site <a href="https://rowcased.github.io/codewars.html#moderator">moderator</a>.

<h2 id="solver"><br>1. Problem Solver</h2>
Signing on with no experience, I had to learn how to learn by studying other user's solutions, reading their comments, and using tutorials. I soon found solving kata in multiple languages offered many invaluable coding insights, as well as how to use documentation to more rapidly learn a new language.

<h style="color: grey; font-weight: bold; font: times; font-size: 15px;">Stats</h>

* <h style="white-space: pre; color: black; font-family: menlo;"> rank (began as 8kyu)        2kyu </h>
* <h style="white-space: pre; color: black; font-family: menlo;"> leaderboard position         124 </h>
* <h style="white-space: pre; color: black; font-family: menlo;"> honor points              <div><object src="https://github.com/rowcased/rowcased.github.io/blob/master/honor_points"></object></div>

 </h> <!-- 17,790 -->
* <h style="white-space: pre; color: black; font-family: menlo;"> honor percentile          0.057% </h>
* <h style="white-space: pre; color: black; font-family: menlo;"> distinct solved kata       2,444 </h>
* <h style="white-space: pre; color: black; font-family: menlo;"> in multiple languages      1,364 </h>
* <h style="white-space: pre; color: black; font-family: menlo;"> total valid solutions      3,808 </h>

<h style="color: grey; font-weight: bold; font: times; font-size: 15px;">Languages</h>

* <h style="white-space: pre; color: black; font-family: menlo;"> Python        thyjyhgf             2,000 </h>
* <h style="white-space: pre; color: black; font-family: menlo;"> JavaScript                   631 </h>
* <h style="white-space: pre; color: black; font-family: menlo;"> C                            515 </h>
* <h style="white-space: pre; color: black; font-family: menlo;"> Ruby                         180 </h>
* <h style="white-space: pre; color: black; font-family: menlo;"> C#                           115 </h>
* <h style="white-space: pre; color: black; font-family: menlo;"> Java                          98 </h>
* <h style="white-space: pre; color: black; font-family: menlo;"> C++                           95 </h>
* <h style="white-space: pre; color: black; font-family: menlo;"> 28 others                    174 </h>
 
<h2 id="translator"><br>2. C Translator</h2>

A fascination with core differences between Python and C lead me to create translations for the site. I developed a very streamlined code structure and wrote a lot of strong unit tests with edge cases and quality feedback. I like that coders around the world are improving their skills via my test suites.

* 150 ~ number of my [C translations available on Codewars](/C_translations)
* 21.0% ~ percentage these make of all 713 approved C kata
* 16,000+ ~ number of valid solves made collectively worldwide

```python
def say_hello(name="World"):   # simple Python function
    text = f'Hello, {name}!'
    print(text)
    return text
```
```c
#include <stdlib.h>            //  equivalent code in C
#include <string.h>
#include <stdio.h>

char *say_hello(const char *name) {
  size_t n = name ? strlen(name) + 9 : 14;
  char *text = (char *) malloc(n * sizeof(char));
  sprintf(text, "Hello, %s!\n", name ? name : "World");
  printf("%s\n", text);
  return text;
}
```

<h2 id="creator"><br>3. Kata Creator</h2>

Codewars is built entirely on user contributions. Each new kata is submitted in beta form to undergo quality consideration by the comminity prior to its approval. My experience creating original kata was very rewarding, having had total control over the concept, design, execution and code structure.

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

Another great feature of Codewars is that it’s maintained by its members; largely an unofficial network of power-users with full site privileges. On any given day I may take part in a variety of activities to assist other members with their code or contribute to maintaining the overall quality of the site.

* directly edit live production code
* answer questions on the dashboard
* address suggestions made for kata
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

