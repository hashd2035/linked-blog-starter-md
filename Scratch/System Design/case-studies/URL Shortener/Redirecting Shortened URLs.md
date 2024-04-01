```toc
```
Here's a breakdown of how a user's request with a shortened URL gets redirected to the long URL using REST/HTTP:

## Components:

1. **User's Browser (Client):** Initiates the request.
2. **URL Shortening Service (Server):** Manages shortening and redirection.
    - Shortener: Generates shortened URLs.
    - Redirector: Handles redirection requests.
3. **Database (Server):** Stores the mapping between shortened and long URLs.

## Handshake

1. **Client Request:**
    
    - User clicks/pastes the shortened URL (e.g., [invalid URL removed]) into their browser.
    - Browser sends an HTTP GET request to the shortened URL.
2. **Redirector:**
    
    - Receives the GET request for the shortened URL ("abc123" in this case).
    - Looks up the shortened URL ("abc123") in the database.
3. **Database:**
    
    - Responds to the Redirector's query.
    - If found: Returns the corresponding long URL associated with "abc123".
    - If not found: Returns an error message (e.g., 404 Not Found).
4. **Redirector Response:**
    
    - If long URL found:
        - Sends an HTTP 301 (Moved Permanently) or 302 (Found) redirect response.
        - The response includes a "Location" header containing the long URL.
    - If not found:
        - Sends an error response (e.g., 404 Not Found).
5. **Client Redirect:**
    
    - Browser receives the redirect response.
    - Extracts the long URL from the "Location" header.
    - Sends a new HTTP GET request directly to the long URL.
6. **Target Web Server:**
    
    - Receives the GET request for the long URL.
    - Processes the request and delivers the intended content to the user's browser.

## Additional Considerations:

- **Caching:** The Redirector can cache frequently accessed mappings to reduce database load.
- **Security:** The URL shortening service should implement measures to prevent malicious redirects and track usage statistics.
- **Customization:** Shortened URLs can be customized with unique identifiers or vanity names.

This is a simplified view, and real-world implementations may involve additional components and functionalities.