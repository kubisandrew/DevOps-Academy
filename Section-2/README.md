# Section 2 – 502 Bad Gateway Troubleshooting

## Root Cause
The Node.js application runs on port 3000.

Nginx is configured to forward requests to port 8080.

Since nothing is running on port 8080 inside the container, Nginx cannot reach the backend.

Because of that, Nginx returns a 502 error.

So the problem is a port mismatch between Nginx and the application.


## Fix:

Update the Nginx configuration to proxy traffic to the correct internal port:

proxy_pass http://web:3000;



## Prevention

Avoid hardcoding ports in multiple places.

Keep the port configuration consistent between services.

Use environment variables instead of fixed numbers.

Test service communication before deployment.

Add health checks to detect backend connection issues early.