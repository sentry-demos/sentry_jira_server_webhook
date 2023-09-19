# sentry_jira_server_webhook

Creating Internal Integration in Sentry:
1) Go to Organization Settings -> Developer Settings, click on "Create New Integration"
2) Give it any name you want
3) Webhook URL should point to your Flask server (main.py)
4) Turn on the Alert Rule Action
5) Copy the content of ticket_schema.json from this repository and paste it inside the Schema field
6) Under permissions: Issue & Event =  Read & Write
7) Under Webhooks mark only the issue checkbox
8) Copy the token and paste it into SENTRY_AUTH_TOKEN in main.py
9) Copy the client secret and paste it into SENTRY_CLIENT_SECRET in main.py
10) Save the changes



Setting up the webhook environment:

Commands for installing Flask:
```
python3 -m venv venv
```
```
. venv/bin/activate
```
```
pip install Flask
```

Command for installing JIRA Python SDK:
```
pip install jira
```

Before you start the Flask server make sure to run:
```
. venv/bin/activate
```

Command for starting the Flask server:
```
flask --app main run
```

![Jira Server Integration chart](https://github.com/sentry-demos/sentry_jira_server_webhook/assets/89414234/a1ad5c96-a23e-4664-a487-90a08ddd89c1)


