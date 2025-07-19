# Welcome to Bug Wrangler Ranch

This first self-assessment is for you to hone several Core Skills that you need as a software developer.

Taking your time now to be thorough, reflective, patient and curious will give you the foundation to be successful throughout the rest of this course and your career.

If you rush this, or think of it as a test to be "passed", then you will already be on the wrong path.

> 🧨 Make sure you answer the vocabulary and understanding questions at the end of this document before notifying your coaches that you are done with the project

## Description

Slim Jenkins offers a vacation package for people who have always wanted to join a cattle driving team across the American Midwest.

He calls it the **Kansas Slim's Cattle Adventure**.

People join a team of experienced drovers who will train them in the basics of herding cattle and driving them across hundreds of miles to their destination at Old Red's Ranch.

Unfortunately, someone gained access to the code that produces an outline of the adventure to the paying customers, so Slim has hired you to examine and fix the code.

## Learning Objectives

Here are your learning objectives for this self-assessment.

1. Able to use the debugger to step through existing code to discover root causes of bugs.
2. Drawing a sequence diagram for a project.
   > Use the [sequencediagram.org](https://sequencediagram.org/) site to generate your sequence diagram. Make sure you save your work as you go.

   Link to Sequence Diagram: https://tinyurl.com/224d7d63

3. Demonstrate learning efficiency by researching concepts you haven't seen before using your peers, mentors, and the World Wide Web as resources.
4. Awareness of when you need help, and then seeking it out.

## Example Output

If you are able to fix all of the bugs, you will output similar to what is below. It will not be identical, but similar.

```sh
************************************************
**  K A N S A S   S L I M ' S   C A T T L E   **
************************************************

\|/         (__)
     '------(oo)
       ||   (__)               \|/
       ||w--||     \|/
   \|/
            \|/                     (__)
                             '------(oo)
                               ||   (__)
                               ||w--||     \|/

You will be accompanying 5 drovers as they drive 50 cattle to Old Red's Ranch for grazing

The herd is made of up the following types of cattle:
Ankole-Watusi,Brown Swiss,Brown Swiss,American Angus,Brown Swiss,
Ankina,American Angus,Ankina,Brown Swiss,Ankole-Watusi,Brown Swiss,
Brown Swiss,American Angus,Ankina,Ankole-Watusi,Brown Swiss,Brown Swiss,
Ankina,Brown Swiss,Ankina,Ankole-Watusi,Brown Swiss,Brown Swiss,
Ankole-Watusi,American Angus,Brown Swiss,American Angus,Ankole-Watusi,
Ankole-Watusi,American Angus,Ankina,Ankina,Ankina,Ankole-Watusi,
American Angus,Brown Swiss,American Angus,Brown Swiss,American Angus,
American Angus,Ankina,Brown Swiss,American Angus,Ankina,Brown Swiss,
American Angus,Ankole-Watusi,Ankina,American Angus,Brown Swiss

Here is the team of drovers you will be joining
        * Melvyn Hethron
        * Yancy Gresley
        * Willabella Attarge
        * Ynes Gyenes
        * Farlie Spere


Your journey will take you through the wildness of the American Midwest and across the following terrain
        * forest
        * plain
        * river
        * mountain
```

1. In the **main** module, one of the first lines of code is `const drovers = hireDrovers(cattleToDrive)`. Explain what the value of the `drovers` variable is when that line of code runs.
   
   The value of the `drovers` variable on this line of code is where we store the output from calling the function `hireDrovers()` using the variable `cattleToDrive` as the argument.

2. At the bottom of the main module, you will see the following code - `for (const drover of drovers)`. Explain what the values of both the `drover` and the `drovers` variables are.
  
   This line of code is a for..of loop that references an entire the array of objects titled `drovers` The variable `drover` represents each object as the loop passes through the entire array. 

3. In the **journey** module, there is a `journeyMaker()` function. In that function, there is a variable named `areas` which will have the value of an object. Use your debugger to show what the value of each key is on that object. Use [Loom](https://www.loom.com) to record your session.
  
   [> Your public Loom URL here](https://www.loom.com/share/13af5482536d4bdd83990aaccb87cd2d?sid=5b6c2258-760c-4009-aaa0-4d984362f3b9)

4. Also in the **journey** module, there is the following code:
   ```js
   for (let forestNumber = 0; forestNumber < areas.forests; forestNumber++) {
      journey.push("forest")
   }
   ```
   Explain this code with your best vocabulary.

   This line of code is a for loop that first declares a variable called "forestNumber" with a value of 0. This variable can be changed since it was declared using "let." The next step in the loop is the condition "forestNumber < areas.forests;" This part of the code checks the current value of forestNumber and sees if it is less than the current value of "forests" in the "areas" object. The final part of the loop "forestNumber++" will increase the value of forestNumber by 1 if the previous condition is true. After the loop completes, the string "forest" is added to the "journey" array using the .push method. The loop will continue to repeat until the condition "forestNumber < areas.forests; is no longer true.

5. Explain the value of the `database` variable in the **database** module. Be as comprehensive as possible.

   The `database` variable in this module is an object that contains all of the information from the two arrays in the module: `cattleTypes` and `drovers.` Each array is made up of objects: `cattleTypes` contains information about the different kinds of cattle each stored in their own object with an id key and a breed key. `drovers` contains information for each drover stored in their own objects with id, first name, last name, and gender keys. Even though both arrays are made up of multiple objects themselves, all of the information from both of them can be stored in a single variable to easily export to other modules in the workspace. The data from these two arrays can now be used in other modules to create functions without having to copy the entire block of data each time.  


6. In the **drovers** module, there is a `hireDrovers()` function. You will notice the following code on that line - `(herdSize)`. What is that defining, and where does it get its value?
  
  In this line of code `(herdSize)` is defining a parameter for the function `hireDrovers().` It's value can be changed as different arguments are passed into the function when it is called later on. 

## When You Are Done

After you have answered all the questions above, you need to push all of your code back up to Github. Follow these instructions.

1. Be in the `bug-wrangler-ranch` directory.
2. `git add --all`
3. `git commit -m "Code complete"`
4. `git push origin main`

Then go to the Learning Platform and click the **Self-assessment Complete** button.