# BarnardTechnology.NET
A collection of data communication and helper libraries for .NET

Initially built as a complete library for the WebConsole project, this now houses a number of data communications and helper functions that I use frequently across a number of different projects.

**This is very early code that does not include comments or complete documentation**

Licensed under the GNU GPLv3.

## Components

### WebConsole

The WebConsole is designed to give very simple console apps the ability to duplicate their console output to a web page. This output allows two-way communication - keypresses entered on the web page will be sent to the console app.

In this way, the intention is to allow headless services to output information to the user in a simple and effective way, whilst also allow the user some basic level of interactivity.

### EmbeddedWebServer

A very basic web server designed to allow embedded content to be easily served from a project. Web pages can be packaged into your .DLL or .EXE using a _Build Action_ of _Embedded Content_. The Type class where the content is stored (which could potentially be in another assembly, if so desired), can then be fed to the *EmbeddedWebServer.ContentServer* class, creating a web server which can serve the embedded content.

### WebServer

A simple web server, based on the example found here:

https://codehosting.net/blog/BlogEngine/post/Simple-C-Web-Server

### WebSocketComms

Enables two-way communications over WebSockets using encapsulated JSON commands. The concept is to streamline the generation of client-server communications by allowing client calls to communicate with a specified class within .NET. In this way, a custom class containing all your comms commands can be created and passed to the WebSocketComms object. When a WebSocket client connects, it can simply call the functions up without needing to worry about any of the underlying communications or handshaking. If an new command needs to be developed, it is then very easy to create - simply add a new method into your exposed class and the function will instantly be available to the client.
