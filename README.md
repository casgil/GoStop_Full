# GoStop Full Task

This repository contains the code for the GoStop task (a version of a Stop Signal Task) written in jspsych. 
This version is based on previous versions written by 
Florence Larkin (https://github.com/florencelarkin/MiniGoStop) and 
updated by Kelvin Lim (https://github.com/kelvinlim/MiniGoStop).  

The original code was for a brief version of the GoStop task designed to run on mobile
as part of brief EMA surveys delivered in Qualtrics.
Kelvin Lim originally forked the MiniGoStop from Florence Larkin to 
change the size of the buttons and fonts to make it easier to run on mobile.

This version is basically a longer version of the task (more trials than the Mini EMA version), 
still meant to run on mobile.
A future enhancement will be to have it adapt to platforms dynamically.

The main deployment for this task has been using Qualtrics.

## Configuration with Qualtrics

Steps:

1. Create a new Block to hold the task.
2. Create a question.
3. [Add the following Javascript.](https://github.com/casgil/GoStop_Full/blob/main/qualtrics_question.js)

4. From the Survey tab, select SurveyFlow and add "Set Embedded Data"
5. Add a New Field GoStop and set it's value to -1.  This is how the data from the 
   jspsych task is passed to qualtrics to be saved in the response.  The EmbeddedData GoStop
   corresponds to the entry in the question JavaScript where the data is returned from jspsych.

   The code can be found at line 53 in `qualtrics_question.js`.[View the code component here](https://github.com/kelvinlim/MiniGoStop/blob/main/qualtrics_question.js#L52-L58)
