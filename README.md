# sentry_jira_server_webhook

Creating Internal Integration in Sentry
1) Go to Oraganization Settings -> Developer Settings, click on "Create New Integration"
2) Give it any name you want
3) Webhook URL should point to your Flask server (main.py)
4) Turn on the Alert Rule Action
5) Copy the content of ticket_schema.json and paste it inside the Schema field
6) Under permissions: Issue & Event =  Read & Write
7) Under Webhooks mark only the issue checkbox
8) Copy the token and paste it into SENTRY_AUTH_TOKEN in main.py
9) Copy the client secret and paste it into SENTRY_CLIENT_SECRET in main.py
10) Save the changes



Setting up the webhook environment:

1) Commands for installing Flask:
    1.1) python3 -m venv venv
    1.2) . venv/bin/activate
    1.3) pip install Flask
2) Command for installing JIRA Python SDK:
    2.1) pip install jira

3) Command for starting the Flask server:
flask --app main run



