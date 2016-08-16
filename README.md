# AirVPN Utils

This script is useful for querying the [AirVPN](https://airvpn.org/) API from the command line.

###Install

####Prerequisites

* docopt
* requests

####Setup

You need an [API key from AirVPN](https://airvpn.org/settings/) to use this script.

Either create a file called api_key.py in the same directory as the airvpn script containing: `API_KEY = 'xxxyyyzzz'` or add your API key to the script `API_KEY = ''`.

*Optional:* Copy the airvpn script into a PATH directory (like /usr/local/bin) so you can run it from any directory.

###Commands

Using this script, you can retrieve any information provided by [AirVPNs API](https://airvpn.org/faq/api/). See their documentation for details.
`sessions` and `user` commands provide data listed in the userinfo section of their API documentation. 


####sessions

`airvpn sessions`

*Returns:* All information listed under sessions of their API

`airvpn sessions -k`

*Returns:* The same information in Key -> Value format

`airvpn sessions exit_ip`

*Returns:* Only the exit IP for each connected client


####user

`airvpn user`

*Returns:* Similar to session, returns all user information provided by their API

`airvpn user -k expiration_days`

*Returns:* Number of paid days remaining in Key -> Value format

####status

`airvpn status -s Albireo`

*Returns:* All information relating to the server named Albireo. Information available is
also posted online at their [status page](https://airvpn.org/status/)

###To Do:

* Add option to provide API key via CLI
* Add option to request disconnect
* Add option to send a notification
* Test options for running on Windows


[![Analytics](https://ga-beacon.appspot.com/UA-10006093-3/github/cjsheets/airvpn-utils?pixel)](https://github.com/cjsheets/airvpn-utils)