!SLIDE subsection

# ORMs: Less Awful Every Year

!SLIDE bullets incremental

# A Tale of Two Cities
* ActiveRecord
* Sequel

!SLIDE subsection

# Sequel
## The ORM for grownups.

!SLIDE

# Jeremy Evans maintaining
## (Hi Jeremy)

!SLIDE

# Abstract as little as you like

!SLIDE

    @@@ ruby
    DB.fetch("SELECT * FROM albums") do |row|
      puts row[:name]
    end

!SLIDE

    @@@ ruby
    DB[:albums].each |row|
      puts row[:name]
    end

!SLIDE

    @@@ ruby
    class Albums < Sequel::Model; end

    Albums.all.each do |a|
      puts a[:name]
    end

!SLIDE

# Datasets
## Queries you can modify programmatically

!SLIDE

    @@@ ruby
    ds1 = DB[:albums]
    # <Dataset: "SELECT * FROM "albums"">
    #

!SLIDE

    @@@ ruby
    ds2 = DB[:albums].where(:name => 'Beck')
    # <Dataset: "SELECT * FROM "albums" 
    #           WHERE ("name" = 'Beck')">

!SLIDE

    @@@ ruby
    ds3 = ds2.select(:year)
    # <Dataset: "SELECT "year" FROM "albums"
    #           WHERE ("name" = 'Beck')">

!SLIDE code

# No magic!

!SLIDE code

    @@@ ruby
    Albums.dataset == DB[:albums]

!SLIDE

## ...withhold tomatos...

!SLIDE subsection

## The infamous
# ActiveRecord

!SLIDE

# 3.0: Less terrifying

!SLIDE

# A detour

!SLIDE

# ARel
# The relational algebra library

!SLIDE

!SLIDE

# Enter: ActiveRecord 3.0

!SLIDE


