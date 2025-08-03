+++
date = '2025-08-03T21:38:51+05:30'
draft = false
title = 'More About APIs'
+++
## Common HTTP methods
- GET: Retrieve data
- POST: Create records
- PUT: Update resource
- PATCH: Partially update
- DELETE: Delete a resource
## HTTP Request Components
- Version
- URL
- Method
- Request header: Cookies, user-agent, refers, etc
- Body (optional) : form data  (JSON/ Form encoded)
## HTTP Response Components
- Requested resource
- Content length
- Content type
- Headers
- Time last modified
- HTTP status codes

## HTTP Status codes
- 100 series: Informational
- 200 series: Successful
- 300 series: Redirection
- 400 series: Client error: Bad API request, Resource not on server etc
- 500 series: Server error: Configuration mismatch, Error check issues, Package dependency issue
- Examples: 
  - 102: Processing
  - 200: Successful
  - 201: Created (POST)
  - 301: Permanently moved
  - 404: Not found
  - 400: Bad request
  - 401: Unauthorised
  - 403: Forbidden

## API Restfulness
1. Client-Server architecture
2. Stateless
3. Cacheable: Responses can be saved by browser/server, Reduce server load, Resuse API results.
4. Layered
5. Uniform interface: Unique URLs for each resource. Unified procedures to modify/other action for each resource
6. Code on demand: API can deliver code/ business logic

## Miscellaneous points
- Caching
- Versioning
- KISS: Keep It Simple Stupid
- Filter, order, paginate
- Rate Limiting
- Monitoring
- Standard API naming conventions
- Consistent naming strategy
- Query parameters
- No trailing slash
- No file names
- Nouns, not verbs
- Forward slashes for hierarchy
- Lower case letter
- Tools:
  - Insomnia
  - Postman
  - cURL
