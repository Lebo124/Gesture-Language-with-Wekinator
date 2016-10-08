Project “Machine Learning for Musicians”.

The project i started is inspired by the time i worked at a school for disabled children who were deaf. Teachers there used gesture language(one gesture for one letter of the alphabet). I wondered if it is possible to teach the computer to recognize these gestures. This model could be used to learn children this gesture language.
It is not an art project, although I think that with this model you can also put the output to other programs as Chuck or so, to make music(did not try that yet).

I used the Leap as an input. I USED port 11500 as an output port !!
I used a adapted version of the color output for 1 regression output with 27 classifiers. One for each letter of the alphabet and one for the sign “-”.

When I started with the project I thought I would be possible to use the timewarp algorithms. A gesture reminded me of the gestures that were used there. But it did not work out. Maybe it was too much for my computer with the 15 inputs. The program did not work properly. Also the gestures that I used were for the most part static and had nothing to do with movement.
So is switched to the classifiers algorithm. First with 5 letters to see if it could  work. First I used the nearest neighbor. The leap tends to have noise in its output, so the nearest neighbor looked a good choice. It worked pretty good, but it gave to much wrong outputs to be useful.

I switched again to the support vector machine. I tried some other algorithms like ADA, but what I feared came through, they responded to much on the noise. 
The vector machine with the default  configuration gave a very good result (still with 5 different classifiers (the A B C D E ) of the alphabet. 

The most significant challenges were in the first place to find the good algorithm. Then I had to train the the model for 27 different gestures. This took a while and did until now not succeed for the 100%. Why not?  There are two letters that have a little movement in them (the letter J and the letter Z). They did not respond well. It is possible to take other gestures for that (there are more languages. I used two languages that are used a lot in the Netherlands. You can see the two pictures in the files I will send). Another problem was that some gestures were very much alike (the letter U and the letter R for instance). This took a lot of training to be sure that the right gesture gave the right letter. 
 If the Wekinator had the possibility to import datasets than I would be easier for me to do this task. The first model was trained for five letters, but I could not use the data for the new project where I trained 27 letters. (maybe I am not aware of all the possibilities).

I had some trouble with running the Processing sketches that came with the wekinator. Also in previous lessons. The Java Machine stopped several times. When I copied and pasted the code from the original sketch into a new one everything worked fine (pity I did not think of that before). Maybe the problem is that these sketches are made on a Macintosh?  The input and output are both processing files. Should work also on a Mac. To run it you need the Leap.

I only trained the project with my own hands (and like most Dutch hands they are not small). I have no idea how it will work when someone else uses it. Maybe it has to be trained again for smaller hands. I am curious if someone tries this model what the results are. 
I will train my model also for the I, J, U ,R letters more, so it will respond better to those letters and will put my project on github. (https://github.com/Lebo124). 
To use the model try to stay with your hand (I trained it for my right hand, when you are left I am afraid you have to write a smart input program, or train the model again) in the middle of the input window. Although I trained it all over the place, it responds well when you stay in one place as much as possible.
Look also at the position of your finger and your wrist and try to make the gesture look like on the two example pictures. Sometime stretching a finger can make the difference between right or wrong. I will take sometime to find the good gesture.
Maybe it works better if you glue the Leap on the wall ore something like that. The gestures are made for vertical use and not for horizontal (did not try that myself. I am not responsible when the Leap wont come off the wall ;)) 

IMPORTANT. Between the letters stretch your hand and you will see the “-” sign in the output. I noticed that the Leap works a lot better when you first stretch your fingers and then make a new gesture. Don't go too quick. When you get the wrong letter there are three possibilities:
1. the Leap does not give the right data (you can often see that in the input window, especially the index finger can do some strange things sometimes), stretch your hand again and try again.
2. Your gestures is not good, try moving your fingers and watch the two examples pictures (included) good.
3. The model is not good enough and needs some more training on the particular letter. When you train the model yourself be aware that training one letter, might influence other letters as well. After the training it can respond well to the letter you trained, but does worse on letters that look like the one you trained. It took a lot of time to train this model and there is still room for improvement.

Experiences with other outputs, like musical outputs or graphical ones, are welcome. Like to know what you did with it.
There are a lot of gesture languages and they differ in different countries. 
