## Editor's note

This is the project I developed for my A Level Computer Science Non-Exam Assessment in 2023. It was my first end to end project and gave me a good introduction to Flask and SQL databases. I also implemented passwordless login using JWT tokens and an SMTP client, which in hindsight is a cool feature to add at a relatively beginner level. 

It has been mostly unmaintained since I first wrote it, and is very rough around the edges. It has no testing, has no static typing and only uses a sqlite database. Nevertheless, it's good to reflect on past work so I've left it up here and make occasional tweaks to make sure it is in a runnable state.

# StudentConnect

StudentConnect is a web app that allows students to:
- Create an account and log in using a magic link sent to their email address
- Upload, edit and save their lesson timetable
- Compare their timetable with other students, highlighting free periods in common
- Control who sees their timetable

It uses Flask as a web framework, Jinja to generate webpages and emails and JWT to generate authentication tokens.

## How to run

1. Set up and activate a virtual environment. I like to use UV but any method is fine.
```bash
uv venv
source .venv/bin/activate
```
2. Install the project as editable. This will also install its dependencies.
```bash
uv pip install -e .
```
3. Initialise the database.
```bash
uv run flask --app studentconnect init-db
```
4. Run the app in a development server.
```bash
uv run flask --app studentconnect run
```

