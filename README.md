# PHP Technical Task
Suggested recipes for lunch API

## Time​ management
We recommend you to not spend more than 2 hours in this task, but it's up to you how you manage your time
to accomplish at least the requirements.

## Assessment

Our assessment criteria will pay attention on:
- How the application is structured.
- Code quality (Clean code).
- Quality of tests.
- Interpretation of the problem.
- Use of `git`.
- Implementation and final execution.
- Commits, as this will allow us to understand some of the decisions you make throughout the process.

## User Story
As a User I would like to make a request to an API that will determine from a set of recipes what I can have for lunch today based on the contents of my fridge, so that I quickly decide what I’ll be having.

__Acceptance Criteria__
- Given that I have made a request to the `​/lunch`​ endpoint I should receive a JSON response of the recipes 
that I can prepare based on the availability of ingredients in my fridge.
- Given that an ingredient is past its ​use-by​ date (inclusive), I should not receive recipes containing this ingredient.
- Given that an ingredient is past its ​best-before​ date (inclusive), but is still within its ​use-by​ date (inclusive),
any recipe containing the oldest (less fresh) ingredient should placed at the bottom of the response object.

__Additional Criteria__
- The application SHOULD contains unit / integration tests (e.g. using ​PHPUnit​).
- The application MUST be completed using an OOP approach.
- The application MUST be ​PSR​ compliant.
- Any dependencies MUST be installed using ​Composer​ (no need to commit dependencies, the
composer.lock file will be sufficient).
- Use PHP5.6 or PHP7.
- Any installation, build steps, testing and usage instructions MUST be provided in a ​README.md
file in the root of the application.

## Framework
Use the Symfony micro framework (​https://symfony.com/doc/current/setup.html) to create the application API. 

## Application Data
For the purpose of this task, the application should simply read data from 2 x JSON files. The contents for these files can be found [here](src/App/Ingredient/data.json) and
[here](src/App/Recipe/data.json).
 
## Submission
The application should be committed to a ​public​ repository on ​GitHub​ or ​BitBucket (​lastname​-​firstname​-techtask-201910) and simply send us a link to the repository.

## Bonus
Configure a Docker environment so that we can test and run the application quickly.
The application should be installed with a single command.
