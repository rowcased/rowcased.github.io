## Codewars.com

**Project description:** I have done at least four different kinds of thing on this website which I will describe in detail in the following catagories: solving, translating, creating, and moderating.

### 1. Solved 2,000 + challenges

Here I put a piece of Python code for you to look at:

```python
from random import randint
dice_roll = lambda : (randint(,1 6), randint(1, 6),)
for i in range(50):
    first, second = dice_roll()
    print("roll = ({}, {})".format(first, second,))
```

### 2. Had over 100 translations into the C language approved

Here is an equivalent piece of code in the C language:

```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int *dice_roll(void) {
    int *numbers = (int *) malloc(2 * sizeof(int));
    numbers[0] = rand() % 6 + 1;
    numbers[1] = rand() % 6 + 1;
    return numbers;
}

int main() {
    srand(time(NULL));
    size_t reps = 50;
    for(size_t i=0; i<reps; i++) {
        int *roll = dice_roll();
    }
    return 0;
}
```

### 3. Created 3 original kata code challenges

<img src="images/grass pile.JPG"/>

### 4. Served as a moderator in answering questions and repairing issues with faulty kata

Here I am going into detail about what it means to be a moderator on codewars. There is no pay, but the hours are good. I have no real authority, although I do have the power to make some changes. I like that I have earned the ability to alter things on the website, so I respect that power and tread very carefully. 

<a href="https://rowcased.github.io/">(return to main page)</a>

<!-- For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/). -->


