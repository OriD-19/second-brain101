---
name: Authentication (Laravel) 
---
*tags: [[Backend Development]] [[Security]]*
Created at: 2022-12-14 21:28

---

# Authentication facade

The most important component for the authentication process. It contains several helper methods to access:
- The authenticated user data with `Auth::user()`.
- Help the process of login (with the `Auth::attempt()` and `Auth::login()` function) and logout (with the `Auth::logout()` function).

## User sessions 

Additionally, the Auth facade also takes care of many security concerns, such as the session management, with the use of SIDs (Session Identifiers).

# Middleware

Laravel also has a built-in `auth` middleware ready to use in routes. You just need to configure it in the `app/middleware` folder if some other functionality is needed in the application.

---
## References:

- [[@Laravel - The PHP Framework For Web Artisans ()]]