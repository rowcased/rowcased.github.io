## Codewars.com
<hr>

#### The Site

Codewars is a user-driven website with a highly interactive community, offering thousands of diverse coding challenges in over 40 supported languages. The site borrows a ‘kyu’ rank system from _Kendo_ and refers to challenges as ‘kata’. Points earned are called _honor_. As increasing levels of honor are achieved, additional site privileges are granted to a member.
<hr>
#### My involvement

At first I just solved a lot of kata in Python as I learned the basics of coding. Eventually I studied C and started translating kata into that language. For a while I solved kata in a multitude of  new languages. I also finally created several original kata. As I earned additional honor and advanced through the ranks, I evolved from user to contributor into an ad hoc site moderator.
<hr>
### 1. Coder

Because I began Codewars as a noob, I was baffled by some challenges and many early solutions were inefficient or clumsy. But I rapidly learned about algorithm best practices by reading comments and studying other people's code. Solving the same kata in multiple languages offered many invaluable insights to programming. I never thought I would accomplish so much.
<br>
* 2kyu ~ rank (began as 8kyu)
* 137 leaderboard position 
* 14,953 ~ honor points 
* 0.074% ~ honor percentile
* 2,968 total correct solutions
    * 2,035 is the base number of distinct solved kata
    *   935 represents resolving in multiple languages
<br>
```
Python     1,643
JavaScript   481
C            448
Ruby         104
C#            66
C++           63
Java          53
27 others    115
```
<hr>
### 2. Translator

One day I tried translating a kata from Python to C. It was reviewed by a moderator, I made some revisions, and it was approved for use on the website. I really enjoyed this process and just kept translating. I like that coders around the globe are using my test suites to improve their skills. I learned about code structure, maintainability, and writing strong unit tests.

* 119 ~ number of my translations now available on Codewars
* 18% ~ percentage these make of all approved C kata on site
* 5,000 ~ number of valid solves made collectively worldwide

Here is a complete list of my approved [C Translations](/C_translations).

```python
# some Python code for you to look at:

def str_sum(a, b):
    c = str(a + b)
    print("{} + {} = {}".format(a, b, c))
    return c
```
```c
// equivalent code in the C language:

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
    char local[21];
    sprintf(local, "%llu", a + b);
    size_t m = strlen(local);
    char *c = (char *) malloc((m + 1) * sizeof(char));
    strcpy(c, local);
    printf("%llu + %llu = %s\n", a, b, c);
    return c;
}
```
<hr>
### 3. Creator
1User contributions.<br>
2Peer reviewed.<br>
3Beta stage.<br>
4<br>
5<br>

1 [is_sator_square](https://www.codewars.com/kata/5cb7baa989b1c50014a53333/python)

    The first kata was based on a stone tablet found at Pompeii. It was an example of a "sator square"
    
* build_square
    This is the second one.
    
* mutations
    And the third. <!-- <img src="images/grass pile.JPG"/> -->
<hr>
### 4. Moderator
1<br>
2<br>
3<br>
4<br>
5<br>

One of the greatest features of Codewars is the community of members that develop and maintain the site. Most of the day to day activity is managed by a large set of highly active and very talented programmers

oh, and you can get banned or punished
fix kata
answer questions
raise issues on kata
resolve issues, mostly wrongs, but somwtimes I fix a problem

could add a test, change a parameter, alter syntax or name-casing according to language, 
creating or resolving issues, answering questions, as well as improving the site by directly live-editing the production code of other code author's kata material.

moderator; in providing maintenance to kata, ranking beta submissions, and guiding new users.

Because rank, did stuff... in answering questions and repairing issues with faulty kata
 There is no pay, but the hours are good. I have no real authority, although I do have the power to make some changes. I like that I have earned the ability to alter things on the website, so I respect that power and tread very carefully. 
<hr>
<a href="https://rowcased.github.io/">(return to portfolio)</a>

<!-- For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/). -->

