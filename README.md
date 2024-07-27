# The-Mighty-Todolist-Telegram-Bot

## Prepare Dev Environment

1) Install Dependencies:

    Use poetry as an environment and module manager to install dependencies by:

    ```bash
    poetry install
    ```

2) Add Environment Variables:

    Create `.env` file in project working directory. The env file will provide the needed environment variables to python files.

    Here is the list of the needed environment variables:
    - **TELEGRAM_TOKEN**:
    - **DATABASE_URL**:
    - **SPREADSHEET_ID**:

3) Get google sheets key:

    You can follow [this guide](https://medium.com/learning-sql/how-to-use-a-google-spreadsheet-as-a-database-3c6f85eea78e) or any other guide to get a service account json key from google cloud.

    Save your key in a file named `sheets_key.json`.

4) Link Pre-Commit Hook:

    Link pre-commit hook to your `.git` file to format *python* files using *black* and *autopep8*.

    ```bash
    ln pre-commit .git/hooks/pre-commit
    ```

5) Run:

    Don't forget to run the bot via poetry.

    ```bash
    poetry run python app/bot.py
    ```
