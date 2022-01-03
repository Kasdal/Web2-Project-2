# Assignment 2 - Web API.

Name: Milan Ples
## Features.

...... A bullet-point list of the ADDITIONAL features you have implemented in the API **THAT WERE NOT IN THE LABS** ......,
 
 + Feature 1 - Implemented user login, signup and authentication
 + Feature 2 - Implemented api for trending movies.
 + Feature 3 = Played with the API to get the mongoose and mongo atlas working. Got close.

## Installation Requirements
```
Download or clone the repository from [https://github.com/Kasdal/Web2-Project-2.git]

```
```
install mongo, mongoose, mongo atlas.
```
```mkdir db
mongod -dbpath db
```

```npm install in the project folder. Both movies-api and reactApp to download the dependencies for the project.
```

```bat
git install
```

## API Configuration

```
NODE_ENV=development
PORT=8080
HOST=localhost or my ip
MONGO_DB=mongodb://*YOUR LOCAL HOST HERE*:27017/movies_db or your db in cloud similar to mine. [mongodb+srv://kasdal:<password>@milanples.zo6s9.mongodb.net/myFirstDatabase?retryWrites=true&w=majority]
SEED_DB=false
SECRET=YourJWTSecret
TMDB_KEY=YOUR TMDB API KEY HERE
```


## API Design
Give an overview of your web API design, perhaps similar to the following: 

|  |  GET | POST | PUT | DELETE
| -- | -- | -- | -- | -- 
| /api/upcoming |Gets a list of movies 
| /api/topRated/{movieid} | Get a Movie by id
| /api/movies/{movieid}/reviews | Get a list of reviews for a movie



## Security and Authentication
Used JWT for authentication and authorization of the API.

## Integrating with React App


~~~
export const getMovies = () => {
    return fetch(
        '/api/movies',
        {headers: {
            'Authorization': window.localStorage.getItem('token')
        }
    }).then(res => res.json());
};

export const getNowPlaying = () => {
    return fetch(
        '/api/movies/now-playing',
        {headers: {
            'Authorization': window.localStorage.getItem('token')
        }
    }).then(res => res.json());
};

~~~

## Extra features

Played around with the API to get the mongoose and mongo atlas working. Got close but not quite there.

