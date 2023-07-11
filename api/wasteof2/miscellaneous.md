# miscellaneous

- `/username-from-id/:id`
	```
	method: GET
	example: /username-from-id/60c4976b59c722b5661559c4

	-----------
		
	returns a user with the specified id.
	```
 	sample responses:
  	- `GET /username-from-id/60c4976b59c722b5661559c4`
  		```
		{
		  "username": "jeffalo"
		}
   		```
  	- `GET /username-from-id/fake_id`
  		```
		{
		  "error": "user not found"
		}
   		```

- `/username-available?username=:username`
	```
	method: GET
	example: /username-available?username=jeffalo

	-----------
		
	returns if a username is eligible for use or not.
	```
 	sample responses:
  	- `GET /username-available?username=jeffalo`
  		```
		{
		  "available": false
		}
   		```
  	- `GET /username-available?username=anaccountthatdoesnotexist`
  		```
		{
		  "available": true
		}
   		```
  	- `GET /username-available`
  		*due to a bug in the api, this request will not complete*

- `/random-post`
	```
	method: GET
	-----------
		
	returns a random post from the site.
 	```
  	- `GET /random-post`
  		```
		{
		  "_id": "60c4977c59c722b5661559c6",
		  "poster": {
		    "name": "jeffalo",
		    "id": "60c4976b59c722b5661559c4",
		    "color": "yellow"
		  },
		  "content": "<p>hello world!</p>",
		  "time": 1623496572456,
		  "pinned": true,
		  "revisions": [
		    {
		      "content": "<p>hello world!</p>",
		      "time": 1623496572456,
		      "current": true
		    }
		  ],
		  "comments": 134,
		  "loves": 134,
		  "reposts": 7
		}
   		```
  	 
