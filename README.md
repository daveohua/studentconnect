## Editor's note

This is the project I developed for my A Level Computer Science Non-Exam Assessment in 2023. It was my first end to end project and gave me a good introduction to Flask and SQL databases. I also implemented passwordless login using JWT tokens and an SMTP client, which in hindsight is a cool feature to add at a relatively beginner level. 

It has been unmaintained since I first wrote it, and is very rough around the edges. It has no testing, has no static typing and only uses a sqlite database. Nevertheless, it's good to reflect on past work so I've left it up here.

# StudentConnect

StudentConnect is a web app that allows students to:
- Create an account and log in using a magic link sent to their email address
- Upload, edit and save their lesson timetable
- Compare their timetable with other students, highlighting free periods in common
- Control who sees their timetable

It uses Flask as a web framework, Jinja to generate webpages and emails and JWT to generate authentication tokens.

## How to run (testing only)

1. Set up a virtual environment with flask and PyJWT installed.
2. Run flask --app studentconnect init-db in the root of the project, to initialise the database.
3. Run flask --app studentconnect run in the root of the project, to run the app locally.

