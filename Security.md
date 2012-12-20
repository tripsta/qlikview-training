
# Security
Security on QlikView Documents can be applied on any of the following
* UserID/Password
* Serial
* NTDOMAIN
* NTNAME
* NTSID

The following example locks the document and gives access to users admin, user1, user2 authorized by password
```
Section Access;
LOAD * INLINE [
    ACCESS, USERID, PASSWORD, NTNAME
    admin, admin, admin
    user, user1, user
    user, user2, user
];
Section Application;
```

Security can be applied inline in the script code or by File->'create hidden script' so that authentication is required to view/edit the access.

Security protected by password is obviously not exportable.