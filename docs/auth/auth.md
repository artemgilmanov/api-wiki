### Authentication and Authorization

- Your API will not always be publicly accessible
- Only authorized users may access it
- Authentication - Who is the user
- Authorization - What is he allowed to do

OAuth2
- Standart protocol for authentication and authorization
- Widely used, mainly in the web apps

App Registration
- Authorization Server should be familiar with the Resource Server (API)
- Resource Server must register itself with the Authorization Server

JWT
- JSON Web Token
- Contains the data the server needs in order to authenticate the user
- Has three sections:
  - Header-type of token (JWT) and signing algorithm
  - Payload-Data on the user
  - Signature
- The three parts are:
  - Base64 encoded
  - Concantinated with "."

JWT and REST Api
- JWT should be send with the Authorization: bearer header
- Can be sent also in body or request parameter
  - Not recommended
