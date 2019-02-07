# crisis-sentry

## Background

This bot was created to aid in the process of notification of crisis situations via a slack channel.

# Example Usage
1. Person notices a mention in the social media space that could quite possibly represent a crisis requiring escalation and management.
2. Person captures the url of the post in question and pastes it into a slack channel possibly using a slash command.
3. This bot will listen on that channel and will evaluate the post for a previous submission to avoid duplication.
4. The bot will then add the url to a mongodb document with a status attribute indicating "submitted"
5. The bot will then listen for the following commands:
a. /crisis submit <url> - submit a new url to the crisis management system
b. /crisis list - list the existing, active crisis entries. Each entry will have a unique id.
c. /crisis approve <id> - approve a crisis entry. This will move the entry from status of submitted to status of 'active'. This will launch a jira ticket with the details.
d. /crisis close <id> - set crisis entry to closed
e. /crisis remove <id> - remove crisis entry from the system.



