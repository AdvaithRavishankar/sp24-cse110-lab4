**1. What was the bug?**

ANS: the variables num1 and num2 are strings and not integers/numbers. Hence, when we run `calculateSum` it concatenates the strings together, producing the buggy add calculation.

*2. How would you fix it? Include a screenshot of your fix. Name it fix.png (or whatever image extension you would like to use) and add it to your expand/screenshots directory.**

ANS: the fix would be the convert num1 and num2 to a `Number()` when the element is fetched. Here is a link to the fixed image: [https://github.com/AdvaithRavishankar/sp24-cse110-lab4/blob/main/expand/screenshots/fix.png](https://github.com/AdvaithRavishankar/sp24-cse110-lab4/blob/main/expand/screenshots/fix.png)
