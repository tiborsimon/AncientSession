#Ancient Session

Ancient Session is a lightweight PHP script that addresses the problem when you have to reload your page to access previously created cookies or session variables.

In version 1.0 you can find this functions:

* __createSession( )__
* __validateSession($refresh)__
* __checkSession( )__

#####Important

It was designed for low traffic sites, because it isn't care about the race conditions that may occour.


---

##Basic usage

####Create a session

	cretaeSession();

	
This code will create a session for the client identified by it's IP address. The session will expire after the defined expiraton time.


####Validate a session

	// check if there is a valid session for the user
	if (validateSession(false)) {
		// refresh the session
		validateSession(true);
		echo "Your session is refreshed.";
	} else {
		echo "Sorry. You don't have a valid session..";
	}

This code will check if there is a valid session for the client. If there is, it refreshes it's expiration timer.


---

 
Relevant articles: <http://stackoverflow.com/questions/10738593/check-if-a-php-cookie-exist-and-if-not-set-him-a-value>