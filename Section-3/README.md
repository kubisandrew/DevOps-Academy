# Production went down – My approach

## 1. Check if the application is really down

First I would try to open the application in the browser.

If the page does not load, I would check if there are any alerts or monitoring messages.

I want to confirm that the application is really down and that it is not just a temporary problem.

## 2. Check if the application is running

Next I would check if the application is still running.

For example I would check:
- if the container is running
- if the server is still online

Command I could use:

    docker ps

If the container is not running, I would try to understand why it stopped.

## 3. Check logs

After that I would check the logs of the application.

Logs often show errors or messages that can help understand what happened.

Command example:

    docker logs <container_name>

Sometimes the error can be clearly visible in the logs.

## 4. Check if something changed recently

Then I would check if something changed before the problem happened.

For example:
- a new deployment
- configuration changes
- system updates

Many production issues happen after some change.

## 5. Try to restore the service

If the problem started after a deployment, I would try to roll back to the previous version that was working.

The main goal is to restore the service as quickly as possible.

## 6. After the service works again

When the application is working again, I would try to find the real cause of the problem.

Then I would:
- write down what happened
- think about what caused the issue
- think about how to prevent the same problem in the future