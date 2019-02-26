# Hack The Box
## Total Points: 60 pts
__________________________________________________________________________________________

### Challenge 1: Reversing Snake [10 pts]
The first challenge I completed was reversing the snake program. This one was pretty easy. I was given a python program in which I had to reverse what the code was doing. I had to find the username and password asked for in the program. The flag was a concatenation of the username and password. The full break down can be seen below.  

The first thing I did was to identify what the username as password are looking for. The username is comparing the first user input with the "slither" variable which is a concatenation of various shellcode values defined above it. I used a hex to ascii converter I found online. The username found was "anaconda".  

<img src="snake0.PNG" alt="hi51" class="inline"/>

Next, I needed to idenitfy how to bypass the password. The code shows that it compares each character in the variable chars with the second user input. After looking through the code and trying to reverse this variable I realized...Why don't I just print it? I have the source! So I made a for loop in the code that prints chars. The output can be seen below.  

<img src="snake1.PNG" alt="hi51" class="inline"/>

After putting the first character in the program sucessfully exited, but...where was the flag? This actually ended up being the most time consuming portion of this challenge. After quite a few tries I went back to the challenge on hack the box to read the question more carefully and found the flag format is HTB{username:password}. This result can be seen below.

<img src="snake2.PNG" alt="hi51" class="inline"/>

Success!!!!  

<img src="snake3.PNG" alt="hi51" class="inline"/>


