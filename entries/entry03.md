# Entry 3
##### 2/12/23

During the past month, I've been trying to fix all my errors that I've been having displayed in the console and trying to add webpack. My previous error was fixed because I realized my script tags were outside of the body tags and just had to move them back in. 

![Screenshot 2023-02-12 215448](https://user-images.githubusercontent.com/91745064/218360155-7fabd9af-1bb5-49a1-85cb-b66259b45bab.png)
<br><br>After that, all my errors were temporarily gone and I decided I wanted to try to progress on with firebase by watching [The Net Ninja](https://www.youtube.com/watch?v=vK2NoOoqyRo&list=PL4cUxeGkcC9jERUGvbudErNCeSZHWUVlb&index=2&t=26s&ab_channel=TheNetNinja) and adding webpack. Once I finished installing webpack with my firebase, it returned an error where it said:

![Screenshot 2023-02-12 222133](https://user-images.githubusercontent.com/91745064/218363170-a9fe7a2e-9776-4827-95ac-b9d68fddce06.png)
<br><br> It was confusing for me since it was telling me to initalize firebase which I did in app.js and it was naming me some files that I didn't have and I only know I had bundle.js and app.js files. I decided to look at [stackoverflow](https://stackoverflow.com/questions/40563140/error-no-firebase-app-default-has-been-created-call-firebase-app-initiali) and it was showing me how to initalize firebase which I already did. So then I headed on to [slack](https://hstatsep.slack.com/archives/CA44BSLRZ/p1675995708937299) where I tried to ask in the #firebase channel for help. I tried a bunch of stuff like messing with the bundle.js file and copying the initialization information into it and removing import commands and turning them into script tags. None of them was able to solve the issue. Then I started trying to comment things out to see if the issue was in bundle.js or app.js. I started commenting out my entire app.js file and the error was still there, but when I commented the entire bundle.js file, the error was gone. At this point I tired to look at [firebase](https://github.com/brianmueller/mfa-pds/blob/main/y2122/firebase/like.html) [examples](https://github.com/allenz2423/sep11-freedom-project) to see where I went wrong. I realized firebase was still useable without webpack so I decided to drop it.

![Screenshot 2023-02-09 213615](https://user-images.githubusercontent.com/91745064/218367015-3c1822eb-3c3e-4cc2-abe9-0ee0d1c9e653.png)
<br><br>Then I went to my next error I had to fix was:<br><br>
![Screenshot 2023-02-12 215758](https://user-images.githubusercontent.com/91745064/218360487-29a7dd4f-babd-4945-bfa5-f1a9c8383c2c.png)
<br><br>This was very misleading for me since I thought my error was in the first line of my html file. When I looked at my first line, it was `<!DOCTYPE html>` and I didn't know what was wrong with my first line. So I dirrectly copied and paste the error into google and found what the error really meant on [stackoverflow](https://stackoverflow.com/questions/40574159/refused-to-execute-script-strict-mime-type-checking-is-enabled). The error meant I just typed in the javascript file incorrectly. I started commenting out each script tag one by one until the error disappeared to find out which script tag was causing this error. I found out it was `<script src="app.js"></script>` and I realized the app.js file was inside my src file and I forgot that I moved my files inside of folders while watching [The Net Ninja](https://www.youtube.com/watch?v=vK2NoOoqyRo&list=PL4cUxeGkcC9jERUGvbudErNCeSZHWUVlb&index=2&t=26s&ab_channel=TheNetNinja). So then I fixed it to `<script src="../src/app.js"></script>"`.

![Screenshot 2023-02-12 225503](https://user-images.githubusercontent.com/91745064/218366849-c8a05aa1-dc54-4c51-b2ea-9943d3f53e3e.png)
<br><br>
# Planning for future
I hope I don't run into more errors about setting up firebase still and skip some The Net Ninja videos towards [episode 11](https://www.youtube.com/watch?v=n-kUZw97-lA&list=PL4cUxeGkcC9jERUGvbudErNCeSZHWUVlb&index=12&ab_channel=TheNetNinja) where I could learn more about how to use firebase authentication.

We are currently in the second step of our EDP (Engineering Design Process) where we are suppose to research our problem and I was researching how to solve my errors. My next step is to stay in the second step of our EDP, but instead of focusing on errors, I would probably move glance at authentication again, but I should really be moving onto realtime database by now.

The two skills I used was how to google and how to read. I used how to google by copying my errors and pasting them to google to find a way to solve them. I also use how to read to read the document once I got on the website and dissected the answer I need instead of looking into the other 30 possible solutions where some had to deal with react and angular.


[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
