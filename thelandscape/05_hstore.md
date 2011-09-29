!SLIDE subsection

hstore

!SLIDE bullets incremental

# Details
* "key-value store" type
* dictionary string->string
* useful operators

!SLIDE bullets incremental

# Useful for
* structured logs
* diverse collections
* reducing migrations

!SLIDE

## Example

    @@@ sql
    SELECT features->'core' 
      FROM installs
      WHERE features ? 'some_addon';

!SLIDE bullets incremental

# Ruby Support
* ActiveRecord (activerecord-postgres-hstore)
* Sequel (sequel-hstore)

!SLIDE

## The Sequel one is better.

!SLIDE

## Disclaimer: I wrote it.

