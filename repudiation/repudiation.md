# Repudiation

The example demonstrates a vulnerability that can lead to repudiation by malicious users attempting to access the services provided by a server.

## Steps to reproduce

1. Install all dependencies

   `$ npm install`

2. Run the server **insecure.ts**.

3. Pretend to be a malicous user and interact with the services by sending requests from the browser.

4. Do you think your actions can be repudiated?

## For you to do

1. Briefly explain the vulnerability.
   user message is saved directly into database without authentication. Any user can write a message. This is not ideal because we cannot keep them accountable
2. Briefly explain why the vulnerability is addressed in **secure.ts**.
   it uses logStream to write to record user behavior into server.log file
3. Which design pattern is used in the secure version to address the vulnerability? Briefly explain how it works?
   it uses audit logging process in the code, every activity is documented within the systems. Here, every route that requires authentication is implemented with logging.
