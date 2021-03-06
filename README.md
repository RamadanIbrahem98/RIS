﻿# HIS

<p align="center">
  <img src="https://img.shields.io/github/license/RamadanIbrahem98/RIS?style=plastic&logo=appveyor&color=blue" alt="license" />
  <img src="https://img.shields.io/github/last-commit/RamadanIbrahem98/RIS?style=plastic&logo=appveyor" alt="last-commit" />
</p>

## Table of Contents

* [About the Project](#about-the-project)
* [Toolbox](#toolbox)
* [Setting Up the Environment](#setting-up-the-environment)
* [Working Demo of the System](#working-demo-of-the-system)
* [Our Team](#our-team)
* [Acknowledgements](#acknowledgements)
* [About](#about)

## About The Project
This is a Radiology Information System MVP project implementing the core concepts of Database Engineering

## Toolbox

* HTML
* CSS
* JavaScript
* JQuery
* Bootstrap
* Flask
    * Flask WTF
    * Flask SQLAlchemy
    * Flask Mail
    * Flask Bcrypt
    * Flask LoginManger

## Setting Up the Environment
1. Clone the repo
    - HTTPS
        ```sh
        git clone https://github.com/RamadanIbrahem98/RIS.git
        ```
    - SSH
        ```sh
        git clone git@github.com:RamadanIbrahem98/RIS.git
        ```
1. Create a Virtual Environment (Optional)
    ```sh
    python -m venv .RIS
    ```
1. Activate the virtual environment 
    - using CMD
        ```sh
        .\.RIS\Scripts\activate
        ```
    - using PowerShell
        ```sh
        .\.RIS\Scripts\Activate.ps1
        ```
    - using Bash
        ```sh
        source .RIS/bin/activate
        ```

1. Install the requirements and dependancies
    ```sh
    pip install -r requirements.txt
    ```
1. Set Up the Environment Variables in the **RIS/\_\_init\_\_.py** file with your own.
    * SECRET_KEY: Is a random secret key used to log sessions.
    * SQLALCHEMY_DATABASE_URI: Is the URI of your database
    * MAIL_USERNAME: Your gmail account.
    * MAIL_PASSWORD: This is an app password assigend from google. you can get one from [Here!](https://security.google.com/settings/security/apppasswords)

1. Create the database and add an Admin to the System. write in the python shell in the **app.py** folder
    ```sh
    from RIS import bcrypt, db
    from RIS.models import User
    db.create_all()
    hashed_password = bcrypt.generate_password_hash('your password here').decode('utf-8')
    user = User(username='Admin user name', email='anything@A.com', password=hashed_password)
    db.session.add(user)
    db.session.commit()
    ```

1. Run the application
    ```sh
    python app.py
    ```
1. View the application on localhost
    ```
    http://localhost:5000/
    ```
## Working Demo of the System

You can find a video demo here

```
https://youtu.be/JKOfDyNr8GI
```

## Our Team

* Ramadan Ibrahem - [![linkedin-shield]](https://www.linkedin.com/in/ramadanibrahem/)
* Muhammad Seyam - [![linkedin-shield]](https://www.linkedin.com/in/mohamed-seyam-91b3b81b7/)
* Muhammad Abd-ElAziz - [![linkedin-shield]](https://www.linkedin.com/in/mohamed-ahmed-abdelaziz)

## Acknowledgements

*We want to thank*
* [StackOverflow Community](https://stackoverflow.com)
* [Cory M. Schafer](https://www.youtube.com/user/schafer5)

## About
This project is a part of the SBE306 course (Computer Systems 3) in the [Systems and Biomedical Engineering Department - Cairo University](http://bmes.cufe.edu.eg/)\
Dr.Ahmed Kandil\
TA. Ayman Anwar


[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
