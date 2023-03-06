# week11AssignmentRepo

1. console was giving an error with can't get elementbyid of 'null'. I added quotes to fix that problem

2. now the code does nothing and is showing no errors. 

3. the counter, does not incriment

4. moved the counter function to the top

5. the player changes to 2 and the value to O, so that code does in fact work

6. changed the clickcount to ++ instead of clickCount += 1;
had no affect
I have to assume, the counter changes when it recieves the first click and then refreshes after the click and it starts over. I am not sure why though

7. moved event listener to the top of the script

no change

8. when the function is called, it initiates the function and that initializes the variable to zero each time. I need to create an outside variable that increments without initializing

9. I changed all the variables inside the function to 'count' which is outside the function. I commented out the internal variable I created just for the function

10. That fixed that issue

11. My conditionals that should remove the event listener are not working to prevent more than 9 clicks
I don't feel like I need this function as there is a better way to stop the game by using endgame conditionals for the scoring. 
  I will need to get the X and O added to the squares before I address this issue in order to  

12. the header is appending properly with the content on line 77. so the variables count, playerNumber and playerXorO are populating the right information and the innerHTML code is working properly

13. the function idGridBox is not logging at all. No error and no log

I noticed that I had created a function, then, not knowing the proper syntax for the code, I pasted a code from the internet that contained a function. I commented out my original function and am going to try to use the pasted function. 
I will then need to fix some names so it works with everything properly
could not get this code to work out
$( "div" ).click(function(idGridBox) {       
        clickedBox = $( "myDIV" ).html(idGridBox.target.nodeName);
        });
I got an error because I erased the function and I still had it being called in the event listener. the new function is also a function but is written in a way that I can't Identify what it would be called to initiate it in the event listener

the function in fact worked but it logged the entire element with tags and values. I will use the .value to try to output only the value to make it functinoal in adding to methods to use in the game.

of course the value is undefined. I need to find out a way to only output the id

Used getAttribute("id") command to create a new variable. The value of that variable is in fact only the ID

14. working in the addXorO function to get the X or O added to the div and display in the block in the html document.

I changed the name of the variable to match the above id function but I'm still not getting a display.
I am going to console log the clickedId in this function to see if the variable is accessible
log showed X and then O for alternating turns and is infact accessible 
Need to see why it isn't being added to the div @ the ID clicked
the playerXorO logs the proper result here as well.
issue must be in the syntax of my innerHTML argument
I feel like the function is being called before the X or O is established. 
I am going to remove the call from the event listener and add it to the document after the div id function
That caused the game to stop adding the initial player 1 x title. so I returned it
Now it the title is not changing to match the player and X or O
no longer logging the player and choice

commented out lines 88-97 to see if that caused the issue
that didn't fix the issue
comment out:
91-97
100-114
116-138
removed addXorO from event listener
now it only logs player 1 and x and no longer alternates players!? fml
commented out the 9 click conditional
Just uncommented line 62 'declarePlayer(); and it started working
moving all function calls into the handleClick function and will organize their calls there. 
learned to add debugger
