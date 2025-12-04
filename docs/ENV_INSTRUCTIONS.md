## Backend Variables (Used in backend/.env)  
These variables are required for the Flask backend to successfully connect to your database.  
`*MONGO_CONNECTION_STRING`
is the URI needed by the backend to establish a secure connection with a MongoDB server.

**Source**: MongoDB Atlas Dashboard

Log into your MongoDB Atlas account.  
Navigate to Database Deployments.  
Find your cluster and click the Connect button.  
Choose Drivers and copy the resulting connection string.

Format Example: `mongodb+srv://<username>:<password>@cluster0.abcde.mongodb.net/?retryWrites=true&w=majority`

`*MONGO_DB_NAME`
is the specific database name the application will target within your MongoDB cluster.

You choose this name.  
Use a simple, descriptive name `like dev_db` or `internship_app_dev`.

## Frontend Variables (Used in frontend/.env)
These variables are required for the React frontend to run authentication and know where to find the backend API.

`*VITE_CLERK_PUBLISHABLE_KEY`
allows the frontend to initialize Clerk, manage authentication, and display the sign-in/sign-up components.

**Source**: Clerk Dashboard

Log into your Clerk account.  
Navigate to your application settings or API Keys.  
Find and copy the Publishable Key.  
[This key is safe to share publicly (it's loaded by the browser), but should still be managed via `.env`]  
Format Example: `pk_test_xxxxxxxxxxxxxxxxxxxxx`

`*VITE_API_URL`
tells the frontend where the backend API is located during local development.

**Source**: Your local backend server address.

While developing locally, this is always set to the address where you run python app.py: `http://127.0.0.1:5000`

