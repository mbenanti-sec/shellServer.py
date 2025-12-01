# shellServer.py
Simple interactive TCP server that listens on port 8000, accepts one client, sends commands, and prints the responses.

shellServer is a minimal interactive TCP command server. It listens on port
8000, accepts a single client, sends commands typed by the operator, and
prints the responses returned by the client. It pairs naturally with
reverseShell.py.

Features

Listens on TCP port 8000

Uses SO_REUSEADDR to allow quick restarts

Accepts one incoming connection and prints the client address

Interactive command loop:

Prompts the operator for a command

Sends the command to the client

Prints the client's response

Terminates when the operator types exit

Requirements

Python 3

Install:

No extra installation required beyond Python 3.

Usage
python3 shellServer.py

Example session:

Attacker box listening and awaiting instructions
Thanks for connecting to me(es.'192.168.1.50', 54321)
b'Bot reporting for duty'
Please enter a command: whoami
victim-user
Please enter a command: exit


After exit:

The server sends exit to the client.

The connection is shut down and closed.

Disclaimer

This script is for educational purposes to study reverse shells and basic
network C2 behavior. Use it only in authorized lab or test environments.
