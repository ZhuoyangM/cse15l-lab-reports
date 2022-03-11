# Lab-Report-5-Week-10

## Find Different Results
- First I use `diff` command to find the tests with different results.

![diff](screen-shots-report5/diff.png)

- Then I choose the following 2 differences

![2diffs](screen-shots-report5/2differences.png)

- Next I use `vim` to check the lines referred in the above picture and find that these 2 tests are, respectively, test-files/494.md and test-files/495.md.

![2tests](screen-shots-report5/2tests.png)

## Bug Analysis
- First I use `cat` command to check the contents of test 494 and 495.

![contents](screen-shots-report5/contentsoftests.png)

- From the contents of the tests, I think my implementation fails both tests, and the provided implementation is correct for both. 

- Actual outputs of my implementation

![2tests](screen-shots-report5/2tests.png)

- Actual outputs of the provided implementation

![expected](screen-shots-report5/expected.png)

- The expected outputs are those from the provided implementation

- For my implementation, the buggy code is shown below. Basically, my code didn't check whether the next close parenthesis ends an url or is just part of that url. For both test 494 and 495, the links in them have urls that include close parentheses. Therefore, for either of those tests, my code just treats the first close parenthesis it finds as the end of the url, but that parenthesis is actually part of the url and should be included in output. That's where the bug comes.

![bug](screen-shots-report5/bug.png)



