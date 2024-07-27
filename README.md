# Telegram-Work-Tracker

## Prepare Dev Environment

1) Install Dependencies:

    In case you don't have poetry, install it via:

    ```bash
    pip3 install poetry
    ```

    > If root user is needed, add `sudo -H` before the command

    Use poetry as an environment and module manager to install dependencies by:

    ```bash
    poetry install
    ```

2) Add Environment Variables:

    Create a `.env` file in the project working directory. The `.env` file will provide the needed environment variables to Python files.

    Here is the list of the needed environment variables:
    - **TELEGRAM_TOKEN**: Telegram bot token.
    - **DATABASE_URL**: The name of the SQLite3 database.
    - **SPREADSHEET_ID**: The ID of the target Google spreadsheet. The sheet must have edit permission and be owned by the provider of the `sheets_key.json` from the Google account.

3) Get Google Sheets Key:

    You can follow [this guide](https://medium.com/learning-sql/how-to-use-a-google-spreadsheet-as-a-database-3c6f85eea78e) or any other guide to get a service account JSON key from Google Cloud.

    Save your key in a file named `sheets_key.json`.

4) Link Pre-Commit Hook:

    Link the pre-commit hook to your `.git` file to format *Python* files using *black* and *autopep8*.

    ```bash
    ln -s pre-commit .git/hooks/pre-commit
    ```

5) Run:

    Don't forget to run the bot via poetry.

    ```bash
    poetry run python app/bot.py
    ```

## What Needs to Be Done

1) Use the current skeleton to implement the basic new functionality of tracking work. This requires multiple steps:

    - Change the data stored in the database
    - Change the Telegram commands
    - Change/write tests

2) Improve the basic functionality according to what functionality you think is missing. Some examples are:

    - Create a different mode where data is stored in a sheet specific to each user rather than the current all-data-in-one-sheet mode. This argument may be passed before starting the bot to keep both functionalities.
    - Change the current sync with sheet mode. Optimize the current behavior or change it as you see fit. Maybe add different modes for different uses.
    - Improve chat UI and user experience.
    - Finally, don't forget to update the documentation and write a proper one (instead of this primitive one).

Thanks to all contributors!
