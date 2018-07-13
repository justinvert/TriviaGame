# Trivia Game
 <a href="https://justinvert.github.io/TriviaGame/">Live Version</a>
 </br>
This page contains a basic Trivia Game.

Once the user clicks the start button, they have only a certain amount of time to complete the quiz. If they do not complete it in the allotted time, the game will automatically read what answers were put in or left un-answered. The user is provided with the option of re-taking the quiz after that screen is shown.


# The Countdown

In order to create the countdown for this code, a global variable was set at 120, standing for 120 seconds. 

```
  var countdown = 120;

```

After the user has decided to click start, they start a function with multiple other functions in it. The important part of this function is the setInterval() method that begins to properly countdown to zero. It uses the function counting and 1000 milliseconds as its pace. 

```
function startGame(){
       fullGame();
       counting();
       quiz();
       
       var countFast = setInterval(counting, 1000);

       onClick = this.style.display = 'none';
    }
```
The counting function itself. As can be seen, clearInterval() method will stop the setInterval().

```
   function counting(){
   
        if (countdown > 0){

        countdown--;
       counters.innerHTML = "Time Remaining: " + countdown + " seconds";
}

else if (countdown = 0){
    clearInterval(counting);
    disable();

}
else {
        clearInterval(counting);
    
        disable();
              document.getElementById("start").innerHTML = "Thank you for playing.";
              return quizCheck();
         }
         
        
    }
```
