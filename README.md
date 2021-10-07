# Invisibility Cloak: Harry Potter
## “When you are not a magician but still can do magic with some lines of code”.

<p>
<img align="right" src="https://github.com/sagihaider/Invisibility-Cloak_CW_2021_22/blob/main/Images/invisiblecloak.jpeg" width="300" height="200" />
</p>

*** 

### Please tweet your work and use hashtag `#UoE2021LovelaceChallengeWeek`

# 1. About Challenge?

## What is Invisibile Cloak?

An invisibility cloak is a magical garment which renders whomever or whatever it covers invisible. Invisibility cloaks are exceptionally rare and valuable within the wizarding world. We believe everyone loves `Harry Potter` and watched invisble cloak in the movie. Yes! It’s the cloak that makes `Harry Potter` invisible. You can make this happen with few line of Python code.

FYI, the Cloak belonged to Harry‘s father, `James`, but then came into `Dumbledore’s` possession after `James` died. `Dumbledore` is the one who anonymously gifted it to `Harry` during Christmas with a note that says: `"Your father left it in my possession before he died. It is time it was returned to you. Use it well."`


## General information 

* For this challenge you will be working in groups of 6. You will need to come up with the design, discussing and working together as a team. Also, you will need to allocate tasks to team members (who will do what, when, how), monitor progress, take actions if something does not work as expected and so on. It is all about team management and working in a team. 

* In general, every team member is expected to put around 20 hours of work.

* And don’t forget to shoot videos, take pictures (both for your presentation and the 10 seconds a day video)

* I would suggest using [Anaconda](https://www.anaconda.com/). Anaconda is a distribution of the Python and R programming languages for scientific computing, that aims to simplify package management and deployment. The distribution includes data-science packages suitable for Windows, Linux, and macOS. You are only required to install anaconda. 

* Please verify that your Spyder in working once Anaconda installation finished. Open your terminal/command prompt and type `spyder`. Waiting until it opens up. 

* Once it open, install opencv package using command `!pip install opencv-python` in the Spyder console.

*** 

# 2. Let's start designing Invisibile Cloak

1. Accessing the webcam 

We can build very interesting applications using the live video stream from the webcam. OpenCV provides a video capture object which handles everything related to opening and closing of the webcam. All we need to do is create that object and keep reading frames from it.

The following code will open the webcam and display them in a window. You can press the 'q' key to exit. This will save a background in an image `image.jpg`

```python
import cv2 #opencv for image processing
#creating a videocapture object
cap = cv2.VideoCapture(0) #this is my webcam

#getting the background image
while cap.isOpened():
    ret, background = cap.read() #simply reading from the web cam
    if ret:
        cv2.imshow("image", background)
        if cv2.waitKey(5) == ord('q'):
            #save the background image
            cv2.imwrite("image.jpg", background)
            break
cap.release()
cv2.destroyAllWindows()
```

2. Store a single frame before starting the infinite loop. You did it above. (Note: We have to capture the background so that if the cloth comes infront of camera then it shows the background.)
3. Detect the color of the cloth and create a mask.
4. Apply the mask on frames.
5. Combine masked frames together.
6. Removing unnecessary noise from masks.

*** 

# 3. Learn to use Python or other packages for computer vision

Follow a few suggestions as given below:

* Find tutorials on web with the keyword “Invisible Cloak”
* See what Python Packages are available and how you can use them in your product. 
* How each each solution is different from others and how you can use them to make your product best. 
* Now go to section 4: Thinking/Designing Invisible Cloak on paper. Make sure you have Python installed and access to webcam key before going to Section 5. 

*** 

# 4. Thinking/Designing Twitter Sentiment Analysis system on paper

Once you become familiar with the building blocks, how to trigger them you need to start thinking about the overall design of your Twitter Sentiment Analysis-

* What building blocks are needed?
* How to connect them?
* What parameters need to be passed?
* How will the demo look like?
* Any additional features you can think of?
* Come up with a block diagram in the paper?


*** 

# 7. Implementing the Design, Testing Invisible Cloak on the Real Time. 

Make sure that you test individual subsystems separately before you test the full system- it always helps when you are designing a complex system, makes debugging easier. When you are ready to test on the real time. contact the GLA or Dr Raza if you need any help. 

*** 

# 8. Additional Functionalities’ (open to your creativity)
In addition to the basic Invisible Cloak, you may think of other features that will make your demo more impressive, such as 

* Read about [Metamaterial cloaking](https://en.wikipedia.org/wiki/Metamaterial_cloaking)
* Kids entertainers.
* Any other novel ideas are most welcome. 


## What you will gain after completing the challenge week:

While working on this challenge, you will gain the following skills (and hopefully be curious to learn more).

* Finding information from the web about the computer vision, python, and artificial intelligence. Good source of information such as  GitHub, Stackoveflow, Medium, etc. 
* What is computer vision and why it is useful? 
* What is image/video processing and why it is in so demand?
* Learn to use basic built-in features available in Python Packages, for example to processing video/images in python. 
* Thinking about what functionalities do APIs provide. 
* Using Anaconda for programming in Python. 
* Thinking about additional features you would like to have (for example, making the invisibile Cloak more interactive).
* Working as a team, allocating tasks to team members, monitoring progress, taking actions if things don’t work as expected
* Presenting your work to an audience

The hope is that some of these skills are quite general and may apply to any other task/project you undertake in the future. Of course, don’t worry if you get stuck- you can always speak to your team mentor or contact Dr Haider Raza (h.raza@essex.ac.uk) for suggestions.
