# django-tdd

## Required Software Installations

+ **The Git version control system**
+ **A virtualenv with Python 3, Django 1.11, and Selenium 3 in it**
+ **Browser**
    - Firefox
        + **Geckodriver**
    - Crome
        + need nothing

# TDD

***Overall TDD process***
![](https://www.obeythetestinggoat.com/book/images/twp2_0403.png)
<br>

***The TDD process with functional and unit tests***
![](https://www.obeythetestinggoat.com/book/images/twp2_0404.png)

## Useful TDD Concepts

+ **User Story**
+ **Expected failure**

## TDD approach

1. We start by writing a functional test, describing the new functionality from the user’s point of view.
<br>
2. Once we have a functional test that fails, we start to think about how to write code that can get it to pass (or at least to get past its current failure). We now use one or more unit tests to define how we want our code to behave—​the idea is that each line of production code we write should be tested by (at least) one of our unit tests.
<br>
3. Once we have a failing unit test, we write the smallest amount of application code we can, just enough to get the unit test to pass. We may iterate between steps 2 and 3 a few times, until we think the functional test will get a little further.
<br>
4. Now we can rerun our functional tests and see if they pass, or get a little further. That may prompt us to write some new unit tests, and some new code, and so on.

### Functional Tests

> <font color="darkred">Terminology: 
Functional Test == Acceptance Test == End-to-End Test</font>
FTs should have a human-readable story that we can follow.

### Unit Tests

>Better Unit Testing Practice: Each Test Should Test One Thing


## Useful Commands and Concepts

**Running the Django dev server**

```
python manage.py runserver
```

**Running the functional tests**

```
python functional_tests.py
```

**Running the unit tests**

```
python manage.py test
```

**The unit-test/code cycle**

1. Run the unit tests in the terminal.
2. Make a minimal code change in the editor.
3. Repeat!

**Regression**
When new code breaks some aspect of the application which used to work.

**Unexpected failure**
When a test fails in a way we weren’t expecting. This either means that we’ve made a mistake in our tests, or that the tests have helped us find a regression, and we need to fix something in our code.

**Red/Green/Refactor**
Another way of describing the TDD process. Write a test and see it fail (Red), write some code to get it to pass (Green), then Refactor to improve the implementation.

**Triangulation**
Adding a test case with a new specific example for some existing code, to justify generalising the implementation (which may be a "cheat" until that point).

**Three strikes and refactor**
A rule of thumb for when to remove duplication from code. When two pieces of code look very similar, it often pays to wait until you see a third use case, so that you’re more sure about what part of the code really is the common, re-usable part to refactor out.

**The scratchpad to-do list**
A place to write down things that occur to us as we’re coding, so that we can finish up what we’re doing and come back to them later.

## Using Selenium to Test User Interactions

## The TDD Process

+ Functional tests
+ Unit Tests
+ The unit-test/code cycle
+ Refactoring