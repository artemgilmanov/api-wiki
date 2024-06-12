### Performance

Async Operations
- Do not wait for long operations to complete
- Relevant mainly for IO operations (files, database access, networking, etc.)
- Almost every platform supports this concept

Caching
- Store frequently accessed data close to the API
-- Usually in-Memory
- Set expiration and invalidation

Rate Limit
- Limit the maximum concurrent requests the API handles

Quota
- Limits the number of requests a specific client can make
- Minimizes risk of heavy load
