### Response Codes
Structure of REST API Response
Response Codes
- Notify clients about the staus of the request
- - Did it succeed?
- - Did it fail?
- - What kind of error?

Importance of Response Codes
- Most clients check for response code and act accordingly
- Monitoring tools check response codes and report it
- Makes the API easie to use and understand
- Very easy to implement, often overlooked

Response Code Groups
- Five groups
- Each groupd represents specific response type (success, error, etc)
- Each group consists of  digit status code

Groups
- 1xx-Informational Response
- 2xx-Success
- 3xx-Redirection
- 4xx-Client Errors
- 5xx-Server Errors

2xx-Success
- 200-Ok
-- The dafault status code
- With GET - returns the entity requested
- With POST - returns the entity created

201-Created
- The request has been fulfilled, a new entity has been created
- Response might contain Location header pointing to the entity
- The expected status code of POST request

202-Accepted
- The request has been accepted ans is pending processing
-  Processing might not be complete
- No nitification is given when processing completes
- Usally used for POST, PUT requests

204-No Content
- Request was fulfilled but no content was sent back
- Schould NOT include body
- Used mainly when updating large entity

The 204 No Content vs 200 OK dilemma
- what schould be returned when a GET returns no entity?
- 200 with no body, or 204?
- No agreed upon answer?

4xx-Client Error
- The client sent a bad request
- Parameters can't be validated (like negativ age)
- JSON can't be parsed
- Used with all verbs

400-Bad Request
- Consider using RFC 7807-Problem Details
- Standard for returning machine-readable data about the problem

401-Unauthorized
- The client is not authorized to access the entity
- Authorization is required
- Not to be confused with 403-Forbidden (I dont know who you are vs I know who you are but you are forbidden)!

403-Forbidden
- The client is not authorized to access the entity
- Authorization failed

404-Not found
- Wht entity specified in the request was not found
- Used when a specific entity was looked for, not with query parameter
- Used all verbs

5xx-Internal Server Error
- Something bad happened while processing the request
- Client can do nothing about it
- Used with all verbs

WebDAV Status
- 207-Multi-Status
- Used for cases where multiple entities are handled, each has its own status
