# lesson 3 - Firewall planning

## objective

Design a network where a firewall sits in front of all application servers.

## Current Network

Internet
   |
Home Router
   |
ubuntu Server
 |- Service 1 (8000)
 |- Service 2 (8080)
 |- Service 3 (9000)

## Furture Network

Internet
  |
Home Router
  |
Firewall VM
  |
Application Server

## Benefits

- Only the firewall is exposed.
- The firwall control incoming traffic.
- Internal server are protected.
- Easier to  monitor and log network activity.
- Similar to enterprise environments.

## Next Steps

- Create a Firewall VM.
- Configure two network interfaces.
- Enable packet forwarding.
- Add firewall rules.
- Route traffic to internal server.
