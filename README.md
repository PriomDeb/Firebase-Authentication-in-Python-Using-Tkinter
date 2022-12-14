
# Firebase Authentication in Python Using Tkinter

This module will help you to add authentication system in your desktop based Python apps 
in a couple of seconds. Just add this repository in the root folder of your project and 
write couple of lines to use Firebase authentication system in your python apps.

[![Contributors](https://img.shields.io/badge/Total_Lines_of_Code_🐍-1121-yellow?style=for-the-badge)](https://github.com/PriomDeb/Firebase-Authentication-in-Python-Using-Tkinter/graphs/contributors)
[![Contributors](https://img.shields.io/github/contributors/PriomDeb/Firebase-Authentication-in-Python-Using-Tkinter?style=for-the-badge)](https://github.com/PriomDeb/Firebase-Authentication-in-Python-Using-Tkinter/graphs/contributors)
[![Members](https://img.shields.io/github/forks/PriomDeb/Firebase-Authentication-in-Python-Using-Tkinter?style=for-the-badge)](https://github.com/PriomDeb/Firebase-Authentication-in-Python-Using-Tkinter/network/members)
[![Stars](https://img.shields.io/github/stars/PriomDeb/Firebase-Authentication-in-Python-Using-Tkinter?style=for-the-badge)](https://github.com/PriomDeb/Firebase-Authentication-in-Python-Using-Tkinter/stargazers)


[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[!["FirebaseandPython"](https://img.shields.io/badge/Firebase-Python-yellow)](https://github.com/PriomDeb/Firebase-Authentication-in-Python-Using-Tkinter)
[!["Tkinter"](https://img.shields.io/badge/Tkinter-Python%20Framework-orange)](https://docs.python.org/3/library/tkinter.html)
[!["EZTranslation"](https://img.shields.io/badge/See%20a%20desktop%20app%20that%20uses-this%20authentication%20module-brightgreen)](https://www.priomdeb.com/ez-translation)
[!["PriomDeb"](https://img.shields.io/badge/PriomDeb-web-yellow)](http://priomdeb.com)

<br/>

<details>
<summary> <b> Table of Contents </b> </summary>

<ol>

<li> <b><a href="#dependencies">Install Required Dependencies </a></b> </li>
<ul>
<li><a href="#1-install-tkinter"> Install Tkinter </a></li>
<li><a href="#2-install-firebase-library-for-python"> Install Firebase in Python </a></li>
<li><a href="#3-install-pillow"> Install Pillow </a></li>
<li><a href="#4-install-pygame"> Install Pygame </a></li>
<li><a href="#5-install-pyglet"> Install Pyglet </a></li>
</ul>

<li> <b><a href="#documentation">Documentation </a></b> </li>
<ul>
<li><a href="#documentation"> Clone the Repository </a></li>
<li><a href="#documentation"> Code Implementations Step by Step </a></li>
<li><a href="#full-code-to-implement-sign-in-and-sign-system-in-your-python-app-using-firebase-and-tkinter"> See Full Code After Implementation is Done </a></li>
</ul>

<li><b><a href="#languages-and-tools"> Language and Tools </a></b></li>
<li><b><a href="#contact"> Contact </a></b></li>
<li><b><a href="#screenshots-of-the-ui"> Screenshots of the UI </a></b></li>

</ol>
</details>


## Dependencies

Install these Dependencies from your terminal. I normally use my PyCharm terminal to install 
the libraries so the libraries are only installed for my working project and not for all project.
If you want you can install from your Git Bush/Windows CMD/Powershell.

### 1. Install Tkinter
```bash
pip install tk
```
Please follow the current installation process of Tkinter from online.


### 2. Install Firebase Library for Python
```bash
pip install pyrebase4
```
We will be using pyrebase4 instead of other pyrebase libraries.


### 3. Install Pillow
```bash
pip install Pillow
```
We install Pillow to process .png images for UI.


### 4. Install Pygame
```bash
pip install pygame
```
We are installing pygame to add some audios for click and error in our authentication app. If you don't want to add then you can just ignore to install this library.


### 5. Install Pyglet
```bash
pip install pyglet
```
We are installing this library to add third-party/downloaded fonts in our app.

# Documentation

### 🌵Clone This Repository
- Open Git bash
- Change the current working directory to the location where you want the cloned directory. Basically your main python app project directory.
- ```Right clik in your Git Bash and paste the below code.```

```bash
$ git clone https://github.com/PriomDeb/Firebase-Authentication-in-Python-Using-Tkinter.git
```
You can clone or simply download this repository as a .zip file. But make sure you put these ***folders and scripts*** in your project's root directory.

|  Scripts                    | 
|  :--------                  | 
| `pyrebaseAuthentication.py` | 
| `tkinterLoginUI.py`         | 
| `app.py`                    |


|  Folders                    | 
|  :--------                  | 
| `authenticationUI`          | 
| `fonts`                     | 


## 🐍 Just a few lines of python code to implement authentication
Add these lines one by one in your python script from where your app's function will be called and your Firebase Authentication in Python using Tkinter is done! <img width="50" height="50" src="https://i.gifer.com/origin/87/87863c1f95e7173189a1a1a1e714373a_w200.gif">

<br/>

### First import these 3 required libraries
```python
from tkinter import *
from pyrebaseAuthentication import FirebaseAuthenticationAPI
from tkinterLoginUI import DrawAuthentication
```

### Then create a object of FirebaseAuthenticationAPI()
```python
firebaseAuth = FirebaseAuthenticationAPI()
```

### Next create a Firebase Project
- Go to https://console.firebase.google.com/
- Click "Add project"
- Give your project name (Any name you want) and click Continue
- Keep Google Analytics as same as it (Default is Enabled) given and click Continue
- Select "Default Account for Firebase" and click Create project
- Wait for a couple of seconds to get your project ready and when it is ready click Continue
- A dashboard of **Project Overview** will be opened and you will see iOS+, Android and Web
- Click on the **Web** which icon is </>
- Give an app name and don't select "Also set up **Firebase Hosting** for this app. Learn more" then click Register app
- Now you will see **Add Firebase SDK**
- Look throgh the SDK codes that is generated by Firebase
- You will see a const variable **firebaseConfig** which is your configuration values to use Firebase Authentication
- Copy the entire **firebaseConfig** values
- ```const firebaseConfig = {
  apiKey: "XXxxXxX00XXxxx-xxxxX0XXXx0XxxxxxXXXXxxx",
  authDomain: "xxx-xx-xxxxx.xxxxxxxxxxx.com",
  projectId: "xxx-xx-xxxxx",
  storageBucket: "xxx-xx-xxxxx.xxxxxxxx.com",
  messagingSenderId: "xxxxxxxxxxxx",
  appId: "x:xxxxxxxxxxxx:web:xxxxxxxxxxxxxxxxxxxxxx",
  measurementId: "G-XXXXXXXXXX"}
- Click Continue to console
- Open your python script and create a dictionary variable **firebase_config** and paste the values like the ***given format***
- ```python 
  firebase_config={"apiKey": "XXxxXxX00XXxxx-xxxxX0XXXx0XxxxxxXXXXxxx",
  "authDomain": "xxx-xx-xxxxx.xxxxxxxxxxx.com",
  "projectId": "xxx-xx-xxxxx",
  "storageBucket": "xxx-xx-xxxxx.xxxxxxxx.com",
  "messagingSenderId": "xxxxxxxxxxxx",
  "appId": "x:xxxxxxxxxxxx:web:xxxxxxxxxxxxxxxxxxxxxx",
  "measurementId": "G-XXXXXXXXXX",
  "databaseURL": ""
  }
  # Copy this format exactly and DON"T FORGET TO KEEP "databaseURL":"", an empty string
  # Keep databaseURL value an empty string
  
  # See I have put the keys inside ""
  # You need to put all the keys inside "" as python only accepts this format in its dictionary data types
  ```
- ***Don't forget to add "databaseURL":"" like this***, keep the value of **"databaseURL"** = empty string
- Go to your Firebase Project Overview/Dashboard and last one thing need to configure to use Firebase Authentication
- Click **Build** from left side menu
- Click **Authentication**
- Click Get Started
- From **Sign-in method** select **Email/Password** and **Enable** it
- Click **Save** 

That's all from Firebase console.

<br/>

### Initialize Firebase
```python
firebaseAuth.initialize_firebase(firebase_config)
```


### Write a function like this exact format and call it
```python
def authentication_to_enter_the_app():
    read_authentication = firebaseAuth.check_authentication()
    uui, display_name, signed_in = read_authentication

    if not signed_in:
        login = DrawAuthentication()
        login.drawLogin()

        if login.authentication_success and login.authentication_email_verified and login.authentication_correct_email_password:
            uui, display_name, signed_in = firebaseAuth.check_authentication()

            # Call Your App Function 
            # Anything code that your want to run after Firebase Authentication is complete successfully
            my_tkinter_app(display_name)
    else:
        # Call App Function
        # Anything code that your want to run after Firebase Authentication is complete successfully
        my_tkinter_app(display_name)

authentication_to_enter_the_app()
```
# bada bim bada boom! <img width="100" height="50" src="https://c.tenor.com/19NP4W6Ny2MAAAAC/im-going-crazy-minions.gif">



<br/>
<br/>

## Full code to implement sign in and sign system in your python app using Firebase and Tkinter
```python
from tkinter import *
from pyrebaseAuthentication import FirebaseAuthenticationAPI
from tkinterLoginUI import DrawAuthentication

# Put all your code inside this function or put the main function calls which is necessary to run your app
# 
def my_app(display_name):
    print(f"Hi, {display_name}!")

firebase_config={"apiKey": "XXxxXxX00XXxxx-xxxxX0XXXx0XxxxxxXXXXxxx",
"authDomain": "xxx-xx-xxxxx.xxxxxxxxxxx.com",
"projectId": "xxx-xx-xxxxx",
"storageBucket": "xxx-xx-xxxxx.xxxxxxxx.com",
"messagingSenderId": "xxxxxxxxxxxx",
"appId": "x:xxxxxxxxxxxx:web:xxxxxxxxxxxxxxxxxxxxxx",
"measurementId": "G-XXXXXXXXXX"}

firebaseAuth = FirebaseAuthenticationAPI()
firebaseAuth.initialize_firebase(firebase_config_values)

def authentication_to_enter_the_app():
    read_authentication = firebaseAuth.check_authentication()
    uui, display_name, signed_in = read_authentication

    if not signed_in:
        login = DrawAuthentication()
        login.drawLogin()

        if login.authentication_success and login.authentication_email_verified and login.authentication_correct_email_password:
            uui, display_name, signed_in = firebaseAuth.check_authentication()
            # Call App Function
            my_app(display_name)
    else:
        # Call App Function
        my_app(display_name)


authentication_to_enter_the_app()
```
<br/>

If you clone this entire repository, you will see a app.py script where I showed how the implementation is work and this is very simple. By writing a couple of lines you can implement sign in and sign out in your python apps. Basically for python desktop apps. 


**That's how you add sign in and sign out using Firebase in Python in the simplest way!**

<br/>

# Languages and Tools

<p align="left"> <a href="https://www.figma.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/figma/figma-icon.svg" alt="figma" width="40" height="40"/> </a>            <a href="https://firebase.google.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/firebase/firebase-icon.svg" alt="firebase" width="40" height="40"/> </a>           <a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/> </a>           <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://www.jetbrains.com/pycharm/"> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1d/PyCharm_Icon.svg/2048px-PyCharm_Icon.svg.png" alt="pycharm" width="40" height="40"> </a>        </p> 

<br/>

# Contact 
[![Mail](https://img.shields.io/badge/Direct_Email-yellow)](mailto:priom@priomdeb.com)

priom@priomdeb.com 

diskaouapps@gmail.com 

http://priomdeb.com


# 🌵 Stay peace and keep coding!
<p align="center"> <a href="https://github.com/PriomDeb"> <img src="https://c.tenor.com/UIOAoI_h-XsAAAAd/sleep-tom-and-jerry.gif"> </a> </p>

# Screenshots of the UI
<p>

<img src="https://i.ibb.co/Wx0fZ7S/login-UI-min.jpg" alt="login-UI-min" border="0" width="400">
<img src="https://i.ibb.co/gMrB9Mw/reset-Password-min.jpg" alt="reset-Password-min" border="0" width="400">
<img src="https://i.ibb.co/0nBz1SF/sign-Up-UI-min.jpg" alt="sign-Up-UI-min" border="0" width="400">
<img src="https://i.ibb.co/x86SL7Q/terms-min.jpg" alt="terms-min" border="0" width="400">
<img src="https://i.ibb.co/DLWsBSr/verify-Email-min.jpg" alt="verify-Email-min" border="0" width="400">
<img src="https://i.ibb.co/xhQDfjT/internet-Connection-min.jpg" alt="internet-Connection-min" border="0" width="400">
</p>
