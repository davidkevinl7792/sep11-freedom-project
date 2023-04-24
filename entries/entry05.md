# Entry 5
##### 4/23/23

Once I finished up with authentication, I decided to look into firestore since that's what we decided that I should work on. I started by learning it from [The Net Ninja](https://www.youtube.com/watch?v=qWy9ylc3f9U&t=4s&ab_channel=TheNetNinja). I learned that the function `collection()` is like creating a folder, `.doc` create files, and `.set()` would set the information you want inside the file. <br>
![Screenshot 2023-04-23 232129](https://user-images.githubusercontent.com/91745064/233893070-052ad367-739c-4319-b1c7-564a9745327d.png)
<br>
So I created a folder which lists all the users that would have thier own id which stores the longitude and latitude. Now the problem was that the information where they put their longitude and latitude isn't in the same file as where they put their sign up information. So I watched a [video](https://www.youtube.com/watch?v=x0VcigW9kN0&ab_channel=OpenJavaScript) and learned to use `localstorage`.<br>
![Screenshot 2023-04-23 235734](https://user-images.githubusercontent.com/91745064/233897205-eaa39cb7-212c-4400-acca-105bf97241d4.png)
![Screenshot 2023-04-24 000134](https://user-images.githubusercontent.com/91745064/233898110-30ea0d2e-71cf-4db8-a3b1-143c5f73153b.png)
<br>
I learned how to use `.getItem` and `.setItem` to import and export information around.
![Screenshot 2023-04-24 001347](https://user-images.githubusercontent.com/91745064/233898670-ab51e6e2-9e9e-4d96-9349-bbbae53cd40b.png)
![Screenshot 2023-04-24 001759](https://user-images.githubusercontent.com/91745064/233899151-0ba1f995-3f5f-4578-9372-451503347bc8.png)
<br>
This is how it looked like when I put it all together, but then I got hit with an error which didn't make sense to me at first because Latitude was a name of one of the information I want it to store. It's basically like a variable and I wondered how it was a unxpected identifier since I should be able to name my information how ever I like.<br>
![Screenshot 2023-04-24 002227](https://user-images.githubusercontent.com/91745064/233899533-c6da7a54-c589-4b3c-bf8d-61a7ad508e58.png)<br>
The error was I missed a comma since I'm listing what information I want to put in there and when when list stuff, you use commas. When I ran it, that's how I saved user inputs with no errors.

We are currently in the fourth step of our EDP (Engineering Design Process) where we layout with the information we learned over the year with Javascript and our tool. My next step is to go onto the fifth step of our EDP where we polish our work and finish our year long project with some html, css, and a bit more Javascript.

The two skills I used was how to learn and debugging. I used how to learn to learn how to move information from one file to another. I also used debugging to debug my error that I had and think about how was it even considered an identifier.

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
