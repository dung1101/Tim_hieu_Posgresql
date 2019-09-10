# 2) User
Create user
```
CREATE USER myuser with PASSWORD '123';
```

Change password
```
ALTER USER myuser PASSWORD 'newpassword';
```

Delete
```

```

# 3) Grant
```
GRANT privilege [, ...] ON object [, ...] TO { PUBLIC | GROUP group | username }

GRANT SELECT ON mytable TO myuser;
GRANT ALL ON ALL TABLES IN SCHEMA PUBLIC TO myuser;
GRANT SELECT ON DATABASE mydb TO myuser;
```
- privilege - value could be: SELECT, INSERT, UPDATE, DELETE, RULE, ALL.
- object - the name of object to which to grant access: table, view, sequence
- PUBLIC - representing all user
- GROUP - group
- username - username

# 4) Revoke
```
REVOKE privilege [, ...] ON object [, ...] FROM { PUBLIC | GROUP groupname | username }
```

