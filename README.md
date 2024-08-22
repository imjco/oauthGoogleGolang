# Google OAuth2 using Golang

This project is a web application that allows users to log in using their Google account. The application is built using Go and utilizes OAuth2 for authentication.  

## Prerequisites

Go (version 1.16 or later)

Git

A Google Cloud project with OAuth 2.0 credentials

## Installation
Clone the repository:  
```
git clone https://github.com/imjco/oauthGoogleGolang.git

cd myapp
```

## Setting Up CLIENTID and CLIENTSECRET for Google OAuth 2.0

1. Create a Google Cloud Project:  
  + Go to the Google Cloud Console.
  + Click on the project dropdown and select "New Project".
  + Enter a project name and click "Create".

2. Enable OAuth 2.0 API:  
 + In the Google Cloud Console, navigate to APIs & Services > Library.
+ Search for "Google+ API" and click on it.
+ Click "Enable".

3. Create OAuth 2.0 Credentials:  
+ Navigate to APIs & Services > Credentials.
+ Click on "Create Credentials" and select "OAuth 2.0 Client IDs".
+ Configure the consent screen by providing the necessary information.
+ Set the application type to "Web application".
+ Add http://localhost:8080/callback to the "Authorized redirect URIs".
+ Click "Create".

4. Retrieve Client ID and Client Secret:  
+ After creating the credentials, you will see a dialog with your Client ID and Client Secret.
+ Copy these values.

## Set Up Environment Variables:  
+ Create a .env file in the root directory of your project.
+ Add the following lines to the .env file:
```
CLIENTID=your-client-id

CLIENTSECRET=your-client-secret

REDIRECTURI=http://localhost:8080/callback
```
Replace your-client-id and your-client-secret with the values you copied from the Google Cloud Console.



## Install dependencies:  
```google
go mod tidy
```

## Running the Application
Start the server:  
```google
go run main.go
```

## Navigate to the application: 
Open your web browser and go to 
```
http://localhost:8080.  
```

## Project Structure
main.go: The main entry point of the application.
index.html: The HTML template for the home page.
.env: Environment variables for OAuth 2.0 credentials (not included in the repository).

## Endpoints
**/**: The home page.

**/login**: Initiates the Google OAuth 2.0 login process.

**/callback**: Handles the OAuth 2.0 callback and displays user information.

 
