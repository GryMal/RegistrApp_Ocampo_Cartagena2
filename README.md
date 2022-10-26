# RegistrApp_Ocampo_Cartagena2
Very humble work
To properly use this application, you must have the following programs for both editing and function:

node: As an event-driven asynchronous JavaScript runtime, Node.js is designed to build scalable network applications. In the following "hello world" example, many connections can be handled simultaneously. After each connection, the callback fires, but if there is no work to be done, Node.js will sleep.

const http = require('http');

const hostname = '127.0.0.1';
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World');
});

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
This is in contrast to the most common concurrency model today, where OS threads are employed. Thread-based networking is relatively inefficient and very difficult to use. In addition, Node.js users do not have to worry about process deadlock, as there are no locks. Almost no function in Node.js directly performs I/O, so the process never deadlocks, except when I/O is performed using synchronous methods from the Node.js standard library. Since nothing blocks, scalable systems are very reasonable to develop in Node.js.

If some of this language is unfamiliar to you, there is a full article on Blocking vs. Non-Blocking.

Node.js is similar in design to, and influenced by, systems like Ruby's Event Machine and Python's Twisted. Node.js takes the event model a bit further. It presents an event loop as a runtime construct rather than as a library. In other systems, there is always a blocking call to start the event loop. Typically, the behavior is defined through callbacks at the beginning of a script, and at the end a server is started through a blocking call like EventMachine::run(). In Node.js, there is no such event loop start callback. Node.js simply enters the event loop after executing the input script. Node.js exits the event loop when there are no more callbacks to perform. This behavior is like JavaScript in the browser - the event loop is hidden from the user.

HTTP is a first class citizen in Node.js, designed with streaming and low latency in mind. This makes Node.js well suited for the foundation of a library or web framework.

Just because Node.js is designed without threads doesn't mean you can't take advantage of multiple cores in your environment. Child processes can be spawned using our child_process.fork() API, and are designed to be easy to communicate with. Built on top of that same interface is the cluster module, which allows you to share sockets between processes to allow load balancing on your cores.

ionic services

android studio(coming soon)
