# Bearer Authorization

## Review, Research, Discussion

### Write the following steps in the correct order

1. Register your application to get a client_id and client_secret
2. Ask the client if they want to sign in via a third party
3. Redirect to a third party authentication endpoint
4. Make a request to the third-party API endpoint
5. Receive authorization code
6. Make a request to the access token endpoint
7. Receive access token

### What can you do with an authorization code?

The authorization code is a temporary code that the client will exchange for an access token. The code itself is obtained from the authorization server where the user gets a chance to see what information the client is requesting, and approve or deny the request. (source: [OAuth](https://www.oauth.com/oauth2-servers/server-side-apps/authorization-code/))

### What can you do with an access token?

Access tokens are the thing that applications use to make API requests on behalf of a user. The access token represents the authorization of a specific application to access specific parts of a user’s data. (source: [OAuth](https://www.oauth.com/oauth2-servers/access-tokens/))

### What's a benefit of using OAuth instead of your own basic authentication?

Better security, token management provides you with a means of tracking each connected device that uses your API. (source: [API UX](http://apiux.com/2013/07/10/oauth-2-trumps-basic-authentication/))

## Vocabulary Terms

- **Client ID:** a public identifier for apps
- **Client Secret:** secret known only to the application and the authorization server
- **Authentication endpoint:** where the user is sent to input credentials to become authorized
- **Access Token Endpoint:** where apps make a request to get an access token for a user
- **API Endpoint:** can include a URL of a server or service, each endpoint is the location from which APIs can access the resources they need to carry out their function
- **Authorization Code:** temporary code that the client will exchange for an access token
- **Access Token:** the thing that applications use to make API requests on behalf of a user

### Sources

- Client id and secret from [OAuth](https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/)
- [Access tokens](https://www.oauth.com/oauth2-servers/access-tokens/)
- [API endpoints](https://smartbear.com/learn/performance-monitoring/api-endpoints)

## JSON Web Tokens

- JSON web token is an open standard that defines a compact and self-contained way for securely transmitting information between parties as a JSON object
- When to use JSON web token:
  - authorization
  - information exchange
- JSON web token consists of three parts separated by dots: header, payload, signature
- JSON web tokens are a good choice to be passed in HTML and HTTP environments
- JSON parsers are common in most programming languages because they map directly to objects
