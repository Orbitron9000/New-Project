# New-Project
none
 <html>
   <head>
 
   <script type="text/javascript">
   
   var message = [];
   var gameForm =  ' Your Input:<input type="text" id="answer"> <input type ="button" id ="enter" onclick="yourMove()" value = "enter">';
   var stage = 1;
   var number = 1;
   
   function stuff(){
   //stage 1
   message[1] = "Do you want to play a game?";
   //stage 2
   message[2] = " You are sitting in front of a computer On the screen a cursor blinks: 'Do you know tha password?' glows in the centre 
   beneath         a    skull and crossbones";
   message[3] = "That is not the password - Do you know tha password?";
   
   //stage 3    
   message[4] = "<>Computer code scrolls down the screen the light fills the message with a dull green swamplike glow. Four more terminals
   jump     into action. You are in..... </p> 
   message[4] +="<>You will need help. You can call Jack and Maeve ,the hackers or Kate and David the cyper-coders.";
   message[4] +="Jack and Maeve can only be contacted via irc ,a few hours at least. They're less likely to be detected but could take hours. </p>";
   message[4] +="<>Kateand David specialise in encryption but they are more likely to be watched by the enemy.</p>";
   message[4] +=" <> Type IRC or email to continue.</p> ";
   //stage4
   message[5] = "You chose the hackers. You will need to access the mainframe, by creating a madelbrot virus programe.";
   message[6] = "You choose the coders. You will need to decrypt the Central Firewall System.";
   var respond = document.getElementById("container");  
   var input = document.getElementById("input_form"); 
   respond.innerHTML = message[1];
   input.innerHTML = gameForm;
   }  
//

   function yourMove()
   {
   respond = document.getElementById("container");  
   input = document.getElementById("input_form"); 
   answer = document.getElementById("answer").value;
   ///////////////////////////////////////////////
   if (stage == 1 && answer == "yes")
   { 
   number = 2;
   stage = 2 ;
   }
   else if( stage=="no"){
   number = 3;
   }
   ////////////////////////////////////////////////////////////////////
    if (stage == 2  && answer == "no") 
   {
    number = 4;
   stage  = 4;
   }
   if (stage == 4 && answer == "IRC") 
   {
   stage   = 5;
   number  = 5;
   }
   if (stage == 4 && answer == "email")
   {
   stage  = 5;
   number = 6;
   }
   respond.innerHTML = message[number];
   input.innerHTML= gameForm;
// I have deliberately not used case/switch statements if/else is good enough. A ninja can pick up case/switch in their own time.

    }
   </script> 
   </head>
   <body onload = "stuff()">
   </body>
 </html>
You will notice that the variable 'number' is redundant in it's current form. The aim is not to remove it , but instead make it relevant. If the game where to allow for a rooms with a realtionship to each other then perhaps number =number +1 , would produce more meangigfull results than number = 6 or number = 5. Or better yet what about making a multidemsuional array for the messages that includes exits.

   message[0][0] ="You are standin in a room you see a table. On the table are:";
   message[0][1] ={1,3,4,5"};
   message[0][3]= {"a knife","a bag of gold","a ring"};
