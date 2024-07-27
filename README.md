jira-commention
===============

Convert specially formatted email addresses in input into Jira user IDs by
searching using the Jira API.

Email addresses prefixed with an “@” character and followed by whitespace are
replaced with the Jira user ID corresponding to that email address.


## Usage
The following command replaces the “@”-prefixed email address in the input with
the user’s Jira ID.

	$ cat <<EOS |
		jira-commention \
			--login jira-user@example.com \
			--token jp3cy1PFmDiCw73JJO6YL9Dj \
			--endpoint example.atlassian.net
	> Hello @other-jira-user@example.com ,
	>
	> This is a Jira comment.
	> EOS
	Hello [~accountid:rY9dCCdodzHOGOUFoyqSOdk6] ,

	This is a Jira comment.


## Install
Copy the “jira-commention” script into your `PATH`.


## License
Copyright © 2024 Teddy Wing. Licensed under the GNU GPLv3+ (see the included
COPYING file).
