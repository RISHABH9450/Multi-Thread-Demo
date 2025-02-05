# Multithreaded Web Server

This project demonstrates a simple multithreaded web server implemented in [Programming Language - e.g., C, Python, Java].  It handles concurrent client requests, improving performance compared to a single-threaded server.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Building](#building)
- [Design](#design)


## Introduction

This web server is designed to handle multiple client requests simultaneously.  Traditional single-threaded servers process requests sequentially, leading to performance bottlenecks when dealing with numerous clients.  This multithreaded approach addresses this issue by creating a separate thread for each incoming connection, allowing the server to handle multiple requests concurrently.

## Features

* **Multithreading:** Handles multiple client requests concurrently using pthreads (or equivalent threading library).
* **HTTP Protocol Support:** Supports basic HTTP GET requests.  
* **Static File Serving:** Serves static files from a specified directory. 


## Building

### Prerequisites

* [Programming Language Compiler/Interpreter - e.g., GCC, Java Interpreter, JDK]

## Design
The server uses a thread pool (or creates threads on demand, describe your approach) to handle incoming connections.  When a new connection is established, the server assigns it to a worker thread.  The worker thread then:

*Reads the HTTP request from the client.
*Parses the request to determine the requested file.
*Reads the requested file from the file system.
*Constructs the HTTP response.
*Sends the response back to the client.
*Closes the connection.

