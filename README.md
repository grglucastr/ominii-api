# ominii-api

Backend API for a Tweet clone app. This project is being developed during the OmniStack Week by RocketSeat.  

**What this API does is** - List posts, add new posts and like posts.

It also comes with socket.io library to provide realtime comunication with its clients.

## Contents
*  [Quick Start](#quick-start)
*  [Database](#db)
	 * [Database  Configuration](#db-config)
*  [API Routes](#routes)
*  [Contribution](#contribution)

## <a name="quick-start"></a>Quick Start

  

1.  **Install via npm:**

Download and install all dependencies
```bash
npm install
```
  
2.  **Configure the port**

By default it runs on port 3000, but you can edit the file

```bash
src/index.js
```

```bash
server.listen(3000, () => {
    console.log('Server started on port 3000')
})
``` 

3.  **Run the API:**
```bash
npm start

```
## <a name="db"></a>Database

For this project, we are using NoSQL (MongoDB) to store the tweets. The database is located in a Cloud Storage Service provided by [MLab](https://mlab.com).

We are also using [Mongoose ORM](https://mongoosejs.com/) to handle database transactions.

### <a name="db-config"></a>Database Configuration

Assuming you're using Mongoose,  can configure the database by accessing the ``` src/index.js ```
 and editing the following line and pass your configuration
```
mongoose.connect('mongodb://<username>:<password>@<host>:<port>/<dbname>', {
  useNewUrlParser:  true
})
```

## <a name="routes"></a>API Routes

All the routes are setted on the ```src/routes.js``` . In overall, the routes are self-descriptive. 

| Route | Description |
| :----- | :----: |
| ```GET /tweets ``` | Lists all the tweets stored on database |
| ```POST /tweets ``` | Post a new tweet to the database |
| ```POST /likes/:id ``` | Increments the like counter for certain tweet. The tweet is passed on the URL by the ```:id``` param |

## <a name="routes"></a>Contribution
We love maintainers! If you are learning NodeJS, Express and want to contribute to this API, just fork it and do a pull request for us! In fact, we not defined any contribution guide, so feel free to do whatever you want to this code.

If you want to contact, send an email to address on this profile bio.