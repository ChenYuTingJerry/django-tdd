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