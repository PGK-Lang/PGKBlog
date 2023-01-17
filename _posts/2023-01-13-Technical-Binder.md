---
title: Ideating Technical Details 
description: Ideating technical data that we developed last week.
comments: false
permalink: /posts/pgk
layout: post
---

<script>

function printTextIfRight(){
    input = document.getElementById("input");
    ret = document.getElementById("ret");
    text = input.value.toLowerCase();
    if (text === "something"){
        console.log("True");
        ret.innerHTML = "true";
    }
    else if (text == ""){
        console.log("Something like this");
        ret.innerHTML = "the answer would then be considered whether it was true";
    }
    else{
        console.log("False");
        ret.innerHTML = "false";
    }

}

</script>
# Ideating Technical Details
**TASK**: Upon the tasks that which you ideated last week, ensure that you have technical details upon which you can execute in order to ensure that your ideas work. 

<br> 

## Task 1: Constructor/Constructor Championship Quiz
1. Build the list
    - Get raw data from github images. form into a list of various lists
    - Generate a function that can get a random element from the list
        - retrieve one link *&* its answer
        - return the image generated + extra information if necessary
    - With the image, place it and store the answer
        - Probably means dictionary is necessary
    - allow the user to input something
    - <input placeholder="Something Like this" id="input"> 
    - <button onclick="printTextIfRight()"> Button also included for work </button>
    - <p id="ret"> the answer would then be considered whether it was true </p>
    - Running on this basic system switch out questions depending on whether it was correct or not. (Also save strikes if incorrect)
    - **<mark> After the game </mark>**:  Save into a file/api? allow to save and display a highscore for those who wish to save as such. Gives as an incentive to continue.

## Task 2: F1 Statistic Page
   - Retrieve data from the API by making an HTTP request to the API endpoint   
     - https://rapidapi.com/sportcontentapi/api/f1-live-motorsport-data/
       - Contains Information Regarding: Constructor Standings, Drivers Standings, Races, Seasons, Drivers, and Constructors
   - Organize the statistics into a structured format. Create a table
   - Integrate in Webpage and add Images to enhance the appeal
   - Style the webpage with CSS
   - Updated regularly by scheduling a task to pull the data from the API at regular intervals

## Task 3: F1 Circuits Page
   - Fetch data from API to receive images and extra details about F1 circuits
     - https://rapidapi.com/api-sports/api/api-formula-1
   - Organize the circuits into a readable format
   - Allow and input bar to more easily find circuits
   - Improve webpage with SASS and CSS
   - Update webpage periodically with calls to the API
