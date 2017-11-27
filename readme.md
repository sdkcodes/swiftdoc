Base url is: http://swifticket.com/api

##List of endpoints:

###GET /movies

###GET /movies/{movieId}

###GET /movies/{movieId}/theatres

###GET /movies/{movieId}/theatres/{theatreId}/showtimes

###GET /movies/showing/today

###GET /movies/showing/tomorrow

###GET /movies/showing/upcoming

###GET /users/{userId}/tickets

###GET /users/{userId}

###POST /users/login

###POST /users

###GET /tickets/{ticketId}

###POST /tickets

###GET /states

##Important information:
All Urls must have a query string `api_token` appended   
e.g http://swifticket.com/api/movies?api_token=[INSERT YOUR ASSIGNED API TOKEN HERE]


#List Movies  
* Url: /movies?api_token=YOUR API TOKEN
* Method: GET
* Url Params: None
* Query String: api_token
* Success Response
	* Code: 200
	* Response:
* Error Response
	* Code:
	* Response:
* Sample: http://swifticket.com/api/movies?api_token=YOUR API TOKEN

#Get Movie
* Url: /movies/:id
* Method: GET
* Url params:
	* id **integer** **Required** "Id of the movie to get"
* Query String: api_token
* Success Response
	* Code: 200
	* Response
* Error Response
* Sample: http://swifticket.com/api/movies/id?api_token=YOUR API TOKEN  

#Get Theatres showing a movie
* Url: /movies/:id/theatres
* Method: GET
* Url params:
	* id **integer** **Required** "Id of the movie"
* Query String: api_token
* Success Response
	* Code: 200
	* Response
* Error Response
* Sample: http://swifticket.com/api/movies/id/theatres?api_token=YOUR API TOKEN  

#Get showtimes for a movie
* Url: /movies/:movieid/theatres/:theatreid/showtimes
* Method: GET
* Url params:
	* movieid **integer** **Required** "Id of the movie to show"
	* theatreid **integer** **Required** "Id of the theatre whose showtimes you're getting"
* Query String: api_token
* Success Response
	* Code: 200
	* Response
* Error Response
* Sample: http://swifticket.com/api/movies/id?api_token=YOUR API TOKEN  

#List movies showing today
* Url: /movies/showing/today
* Method: GET
* Url params:None
* Query String: api_token
* Success Response
	* Code: 200
	* Response
* Error Response
* Sample: http://swifticket.com/api/movies/showing/today?api_token=[YOUR API TOKEN]  

#List movies showing tomorrow
* Url: /movies/showing/tomorrow
* Method: GET
* Url params:None
* Query String: api_token
* Success Response
	* Code: 200
	* Response
* Error Response
* Sample: http://swifticket.com/api/movies/showing/tomorrow?api_token=[YOUR API TOKEN]

#List upcoming movies
* Url: /movies/showing/upcoming
* Method: GET
* Url params:None
* Query String: api_token
* Success Response
	* Code: 200
	* Response
* Error Response
* Sample: http://swifticket.com/api/movies/showing/upcoming?api_token=[YOUR API TOKEN]

#Create a new ticket
* Url: /tickets
* Method: POST
* Url params: None
* Post Params: {"showtime_id":12, "user_id":2, "quantity":1}
* Query String: api_token
* Success Response
	* Code: 200
	* Response
* Error Response
* Sample: http://swifticket.com/api/tickets?api_token=YOUR API TOKEN  

#Get tickets of a user
* Url: /users/:id/tickets
* Method: GET
* Url params:
	* id **integer** **Required** "Id of the user whose tickets we are getting"
* Query String: api_token
* Success Response
	* Code: 200
	* Response
* Error Response
* Sample: http://swifticket.com/api/movies/id?api_token=[YOUR API TOKEN]

#Get User
* Url: /users/:id
* Method: GET
* Url params:
	* id **integer** **Required** "Id of the user"
* Query String: api_token
* Success Response
	* Code: 200
	* Response
* Error Response
* Sample: http://swifticket.com/api/users/id?api_token=YOUR API TOKEN  

#User Login
* Url: /users/login
* Method: POST
* Url params: None
* Post Params: {"email":"user@email.com", "password":"user_password"}
* Query String: api_token
* Success Response
	* Code: 200
	* Response
* Error Response
* Sample: http://swifticket.com/api/users/login?api_token=YOUR API TOKEN  

#Register User
* Url: /users
* Method: POST
* Url params: None
* Post Params: {"email":"user@email.com", "password":"user_password", "name":"First Last"}
* Query String: api_token
* Success Response
	* Code: 200
	* Response
* Error Response
* Sample: http://swifticket.com/api/users?api_token=YOUR API TOKEN  