# Voting Application Architecture


![image](https://user-images.githubusercontent.com/93056758/179829815-4aef70ab-6ae2-44e8-87ca-edc7d3c4bf07.png)

- front-end web app in Python or ASP.NET Core which lets you vote between two options
- Redis  queue which collects new votes
- .NET Core, Java or .NET Core 2.1 worker which consumes votes and stores them in…
- Postgres database backed by a Docker volume
- Node.js or ASP.NET Core SignalR webapp which shows the results of the voting in real time


Notes

The voting application only accepts one vote per client. It does not register votes if a vote has already been submitted from a client.

This isn't an example of a properly architected perfectly designed distributed app... it's just a simple example of the various types of pieces and languages you might see (queues, persistent data, etc), and how to deal with them in Docker at a basic level.
