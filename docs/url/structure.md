### URL Structure
- Defines the structure of the API's URL
- The most important part of the API
- MUST be well thought out

**Should be:**
- Self-explanatory
- Consistent across the API
- Predictable

**Domain Name**
- The first part of the URL
- Usually contains FQDN (Fully Qualified Domain Name) or a server name
- Protocol should be HTTPS
  - e.g. https://api.myapp.com

**API Word**
- If the domain does not include `api`, it comes now
  - e.g. https://www.myapp.com/api
- Emphasizes this URL is for the API, not the website
- Can be part of the domain name itself

**Version**
- If the version strategy is URL - it comes now
- Only natural numbers:
  - Positive
  - No decimals
- Could be prefixed with `v`
  - e.g. https://www.myapp.com/api/v1

**Entity**
- REST deals with resources, or entities
- The next part is the entity we're dealing with
- Should be one word, no more
- NEVER a verb
  - This is the HTTP Verb role (/api/v1/order)

**ID Parameter**
- When dealing with a specific entity - next is the entity ID
- The ID is a part of the URL
  - Relevant for:
    - GET
    - PUT
    - DELETE

**Sub Entity**
- Used for accessing entities that are dependent on other entities
- Example: Get all the items of order no.17
- Common mistake:
  - /api/v1/ItemsInOrder/17
  - Not readable
  - Not simple
- Sub Entity should come after the ID parameter
  - /api/v1/order/17/items
- URL is hierarchical, easy to understand
- Same goes for sub-sub-entity, etc.

**Query Parameters**
- Used to query the entities in GET method
- Come at the end of the URL, after `?`
- Concatenated with `&`
  - /api/v1/orders?fromDate=12/12/2018&toDate=2/2/2019

**Singular vs Plural**
- The dilemma:
  - /api/v1/order or /api/v1/orders
  - /api/v1/order?user=john or /api/v1/orders?user=john
