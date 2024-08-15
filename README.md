# University Notes Backup - Notion
Python script to automatically download notion pages from a given notion database and uploads them to github as both markdown files and PDF

Crontab command for an update every day at 1PM - Prints stdout and stderr to /tmp/notion_log:

```
SHELL=/bin/bash
0 13 * * * /path/to/script/directory/build.sh
```

Environment variables:
Environment variables should can be declared in a file called envvars located in the root of the git directory
- NOTION_TOKEN - API Token for notion integration that has access to a given database
- SENDER_EMAIL - Email address used for reporting error messages
- RECEIVER_EMAIL - Email address used for recieving the error messages
- SENDER_PASSWORD - App password generated for 'SENDER_EMAIL'
- DATABASE_ID - Notion ID of the database to be downloaded/uploaded

External Librarys:
- [notion2md](https://github.com/echo724/notion2md) - Converts notion blocks to markdown files
- [notion-client](https://pypi.org/project/notion-client/) - Client for connecting to a particular notion database
- [pypandoc](https://pypi.org/project/pypandoc/) - Converts markdown files to PDFs
