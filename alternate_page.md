## Codewars.com
<hr>

#### The Site

Codewars is a prominent, user-driven website with a highly interactive community, offering thousands of coding challenges on a variety of topics in over 40 supported languages. The site borrows from Kendo; using a ‘kyu’ rank system and referring to challenges as ‘kata’. Points earned by activity on the site are considered _honor_. As increasing levels of honor are achieved, additional site privileges are granted to the user.
<hr>
#### My involvement

At first I just solved a lot of kata in Python as I learned the basics of coding. Eventually I studied C and started translating kata into that language. For a while I solved kata in a multitude of  new languages. I also finally created several original kata. As I earned additional honor and advanced through the ranks, I evolved from user to contributor into an ad hoc site moderator.
<hr>
### 1. Coder

Solving code challenges is main feature of the website. I solved a lot of them. I learned a lot while solving. You will see the good and the bad. Most of it was serious, some of it was play, some of it was art, but all of it was study. I'm in the top 100 users for solved kata, my honor percentile is in thd top 0.074%, and my leaderboard position is #137. Rank is 2kyu.

* 2,968 total correct solutions
    * 2,033 is the base number of distinct solved kata
    *   935 represents resolving in multiple languages

```
1 Python     1,643
2 JavaScript   479
3 C            446
4 Ruby         104
5 C#            66
6 C++           63
7 Java          52
& 27 others    115
```
<hr>
### 2. Translator

One day I tried translating a kata from Python to C. It was reviewed by a moderator, I made some revisions, and it was approved for use on the website. I really enjoyed this process and just kept translating. I like that coders around the globe are using my test suites to improve their skills.

* 119 ~ number of approved translations active on Codewars
* 18% ~ percentage these make of all approved C kata on site
* 5,000 ~ number of correct solves made collectively worldwide

Here is a list of my [C Translations](/C_translations) currently available for use online.

```python
# Here is a piece of Python code for you to look at:

def str_sum(a, b):
    c = str(a + b)
    print("{} + {} = {}".format(a, b, c))
    return c
```
```c
// And here is the equivalent code in the C language:

#include <stdlib.h>
#include <string.h>
#include <limits.h>
#include <stdio.h>

#define ull unsigned long long
char *str_sum(ull a, ull b) {
    if(ULONG_MAX - a < b) {
        printf("Overflow Error\n");
        return NULL;
    }
    char c_str[21];
    sprintf(c_str, "%llu", a + b);
    size_t m = strlen(c_str);
    char *c = (char *) malloc((m + 1) * sizeof(char));
    strcpy(c, c_str);
    printf("%llu + %llu = %s\n", a, b, c);
    return c;
}
```
<hr>
### 3. Creator

    1 is_sator_square
    The first kata was based on a stone tablet found at Pompeii. It was an example of a "sator square"
    
    2 build_square
    This is the second one.
    
    3 mutations
    And the third. <!-- <img src="images/grass pile.JPG"/> -->
<hr>
### 4. Moderator

One of the greatest features of Codewars is the community of members that develop and maintain the site. Most of the day to day activity is managed by a large set of highly active and very talented programmers

oh, and you can get banned or punished
fix kata
answer questions
raise issues on kata
resolve issues, mostly wrongs, but somwtimes I fix a problem

### site maintainance
could add a test, change a parameter, alter syntax or name-casing according to language, 
### issues

### 

moderator; in providing maintenance to kata, ranking beta submissions, and guiding new users.

Because rank, did stuff... in answering questions and repairing issues with faulty kata
 There is no pay, but the hours are good. I have no real authority, although I do have the power to make some changes. I like that I have earned the ability to alter things on the website, so I respect that power and tread very carefully. 
<hr>
<a href="https://rowcased.github.io/">(return to portfolio)</a>

<!-- For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/). -->

Along the way, I learned many things other than algorithms and data sets, such as maintainability, legibility, portability, optimization, documentation, unit testing, and many other fundamental principles of computer programming.

Eventually I decided to also study C, and later branched out into other languages such as JavaScript, C++, Ruby, C#, and Java. This taught me how to rapidly learn the basics of a new language.
As part of my study of the C language, I began translating kata I had previously solved in Python into C for use on the site. This taught me a lot about code structure, maintainability, legibility, and writing strong unit tests.
After some experience with that I created several original kata which were all approved and are currently in use online.
With the earned privileges of rank, I now may also serve the site as a moderator; creating or resolving issues, answering questions, as well as improving the site by directly live-editing the production code of other code author's kata material.


#### The Long Story<br>
Shortly after beginning my study of C, I decided to try writing a translation into that language of a simple kata I had previously solved in Python. I made some mistakes, but there were moderators knowlegable in the language to scrutinize my work. I appreciated that they would usually only tell me _what_ the problem was so up to me to figure out how to fix it. Much to my delight the translation was approved and I just kept making more. All new kata and translation submissions are thus peer-reviewed by moderators, and only when all issues are fixed by the translator will the moderator approve the translation for use on the website. Once it's active on the site, if any issue arises, it's up to the translator to fix the problem to resolve the issue. I like the idea that coders all around the world are honing their skills on the random tests suites I constructed for use on the wensite. Learned how interact.



