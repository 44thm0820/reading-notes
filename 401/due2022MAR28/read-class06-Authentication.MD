# Readings: Authentication

## Instructions

Below you will find some reading material, code samples, and some additional resources that support today’s topic and the upcoming lecture.

Review the Submission Instructions for guidance on completing and submitting this assignment.

## Readings

### Securing Passwords

[securing passwords with bycrypt - hacker news](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)

In comparison to alternatives such as cryptographic hash algorithm which are susceptible to wordlists and brute force to crack the hashes, Bcrypt seems like a superior alternative.

BCrypt, is considered slow and strong. Using a technique called Key stretching, Bcrypt and PBKDF2 are algorithms that make brute force attacks slower and minimize impact.

Bcrypt is an adaptive hash function based on the Blowfish symmetric block cipher cryptographic algorithm and introduces a work factor (also known as security factor), which allows you to determine how expensive the hash function will be.

### Basic Auth

[Basic access authentication - wikipedia](https://en.wikipedia.org/wiki/Basic_access_authentication)

In the context of an HTTP transaction, basic access authentication is a method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request. In basic HTTP authentication, a request contains a header field in the form of Authorization: Basic <credentials>, where credentials is the Base64 encoding of ID and password joined by a single colon `:`.

### OWASP auth cheatsheet

[Authentication Cheat Sheet - owasp.org](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)

Introduction
Authentication is the process of verifying that an individual, entity or website is whom it claims to be. Authentication in the context of web applications is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know.

Session Management is a process by which a server maintains the state of an entity interacting with it. This is required for a server to remember how to react to subsequent requests throughout a transaction. Sessions are maintained on the server by a session identifier which can be passed back and forward between the client and server when transmitting and receiving requests. Sessions should be unique per user and computationally very difficult to predict. The Session Management Cheat Sheet contains further guidance on the best practices in this area.

Authentication General Guidelines¶
User IDs¶
Make sure your usernames/user IDs are case-insensitive. User 'smith' and user 'Smith' should be the same user. Usernames should also be unique. For high-security applications, usernames could be assigned and secret instead of user-defined public data.

The above three sections are just one of many sections available on the Authentication Cheat Sheet, but in total summarizes the owasp larger documentation library into a few pages.  For greater detail on any topic briefly mentioned, click the menu in the top left corner.

### bcrypt docs 

[bycrypt docs - npm docs](https://www.npmjs.com/package/bcrypt)

This is the link to the npm docs for bcrypt. Use this doc to incorporate bcrypt into your javascript app.  Example code is below.

````javascript
async (recommended)
const bcrypt = require('bcrypt');
const saltRounds = 10;
const myPlaintextPassword = 's0/\/\P4$$w0rD';
const someOtherPlaintextPassword = 'not_bacon';
````

To hash a password:
Technique 1 (generate a salt and hash on separate function calls):

````javascript
bcrypt.genSalt(saltRounds, function(err, salt) {
    bcrypt.hash(myPlaintextPassword, salt, function(err, hash) {
        // Store hash in your password DB.
    });
});
````

Technique 2 (auto-gen a salt and hash):

````javascript
bcrypt.hash(myPlaintextPassword, saltRounds, function(err, hash) {
    // Store hash in your password DB.
});
````
Note that both techniques achieve the same end-result.

To check a password:
````javascript
// Load hash from your password DB.
bcrypt.compare(myPlaintextPassword, hash, function(err, result) {
    // result == true
});
bcrypt.compare(someOtherPlaintextPassword, hash, function(err, result) {
    // result == false
});
````