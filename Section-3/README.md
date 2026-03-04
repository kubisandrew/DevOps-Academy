# Production went down – My approach

## 1. Check if it is really down

First, I would try to open the application in the browser.

If I have access to monitoring, I would check if it shows an error.

I want to be sure the problem is real.

## 2. Check if the application is running

I would check if:

- The container is running
- The server is online

For example, I would use commands like:

```bash
docker ps
```

If the container is stopped, I would check why.

## 3. Check logs

I would check application logs to see if there is any error.

For example:

```bash
docker logs <container_name>
```

Logs usually show the problem.

## 4. Check if there was a recent change

I would check if:

- There was a new deployment
- Someone changed configuration
- Something was updated recently

Many production problems happen after changes.

## 5. Try to restore service

If the issue started after a deployment, I would roll back to the previous working version.

The main goal is to make the application work again as soon as possible.

## 6. After it works again

After restoring the service, I would:

- Find the real cause
- Document the issue
- Think about how to prevent it next time