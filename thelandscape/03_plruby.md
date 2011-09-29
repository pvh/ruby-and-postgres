!SLIDE subsection

# PL/Ruby

!SLIDE

## Why aren't more Rubyists excited?

!SLIDE bullets incremental

## Obvious first answer:
* Ruby developers don't do databases
* (Much.)

!SLIDE

## So why don't I care about PL/Ruby?

!SLIDE bullets incremental

# What's missing?
* rubygems
* bundler
* version control
* trust

!SLIDE

# But that can all be fixed!

!SLIDE

# PL/Python already fills that need

!SLIDE

# Use the right tool.

!SLIDE subsection

Sidebar: PL/JavaScript

!SLIDE subsection

AKA: PL/V8

!SLIDE bullets incremental

# Awesome features
* well-known syntax
* lots of code out there
* (obviously) native JSON
* JIT compiled

!SLIDE

# Developers love JSON.

!SLIDE

# Indexable semi-structured documents

!SLIDE

    @@@ sql
    CREATE TYPE json;
    INSERT '{"values": [0,1,2]}' INTO json;

!SLIDE

    @@@ sql
    CREATE INDEX titles on json (
      (json_path('$.head.title')
    );

!SLIDE subsection

# end sidebar :)


