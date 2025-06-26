# Troubleshooting Guide

## Common Issues

### 1. 401 Unauthorized Error
- Ensure the Personal Access Token is valid, has not expired, and has necessary permissions (e.g., `public_repo` scope).
- Verify the token is correctly included in the request headers.

### 2. Rate Limits
- GitHub limits API usage to 5000 requests per hour for authenticated users.
- If a 403 Forbidden error related to rate limits occurs, wait until the limit resets before making more requests.
- Implementing delay between requests helps avoid hitting the rate limit.

### 3. General Error Handling
- Check HTTP response status codes before processing data.
- Handle unexpected errors by logging the error message and retrying if appropriate.
