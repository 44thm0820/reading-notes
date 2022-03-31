# Readings: Authentication

## Instructions

Below you will find some reading material, code samples, and some additional resources that support today’s topic and the upcoming lecture.

Review the Submission Instructions for guidance on completing and submitting this assignment.

## Readings

### JWTS Explained

[JWTS Explained - youtube](https://www.youtube.com/watch?v=926mknSW9Lo)

JWT is JSON Web token - Open standard (anyone can use), Strictly transfer info between two bodies, digitally signed - info is verified and trusted, Compact - can be sent via url, post request, http header, and has fast transmission.
Self-contained - contains info about the user, avoids querying the database more than once.

JWT is useful for authenticiation amd information exchange

Structure of JWT is header, payload and signature.

### Intro to JWT

[Intro to JWT - jwt.io website](https://jwt.io/introduction/)

repetitive info compared to the youtube clip.

### Are JWTs secure?

[Are JWTs secure? stack overflow](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

The gist it seems of this stack overflow article is like anything, nothing is 100% secure. But relatively speaking, the JWT concept allows a higher level of protection than most alternatives.

### Bookmark and Review

[npm jsonwebtoken docs - npm docs](https://www.npmjs.com/package/jsonwebtoken)


## Things I want to know more about, and anytime a question arises in your mind, or something catches your curiosity, note it under this heading.

jwt in use