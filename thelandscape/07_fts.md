!SLIDE subsection

# Full Text Search

!SLIDE bullets

# Mechanism
* tokenize data
* stem values
* maintain GIN index

!SLIDE
## Example:
    @@@ sql
    SELECT * FROM table
     WHERE to_tsvector('english', desc)
           @@ plainto_tsquery('english', ?);

!SLIDE code

ERROR: must be owner of language plpgsql

!SLIDE

"this error [...] constitutes [...] proof that PostgreSQL [...] supports terrorism"

!SLIDE

# Someone seems sad.

!SLIDE

# Ruby Support
* pg_search
* buscando_el_viento
* others
* (see Will's talk)

