!SLIDE subsection

# Unloved
## Unsupported or Uninvented

!SLIDE

# Arrays

!SLIDE code

    pvh=# select array_agg(name) from users;
        array_agg     
    ------------------
     {Peter,Dan,Will}
    (1 row)

!SLIDE

Not so bad for strings, but what about complex types?

!SLIDE

# Ruby Support
* very poor
* ActiveRecord (activerecord-postgresql-arrays)
* Sequel (... despair)

!SLIDE

# Record Types

!SLIDE

    @@@ sql
    select (user) from users;

!SLIDE code

    pvh=# select (users) from users;
               users           
    ---------------------------
     (0,Peter,pvh@heroku.com)
     (1,Dan,daniel@heroku.com)
     (2,Will,will@heroku.com)
    (3 rows)

