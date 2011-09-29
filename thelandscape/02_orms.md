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

## or as much!

!SLIDE

    @@@ ruby
    class Albums < Sequel::Model; end

    Albums.all.each do |a|
      puts a[:name]
    end

!SLIDE

# Sequel Datasets
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

!SLIDE subsection

A detour: Arel

!SLIDE subsection

# Arel
## The relational algebra library

!SLIDE

Kind of like Sequel,

!SLIDE

but more verbose

!SLIDE

and with a relational algebra syntax.

!SLIDE

# Example
    @@@ ruby
    users = Arel::Table.new(:users)
    query = users.project(Arel.sql('*'))
    query.to_sql

!SLIDE

Pretty okay!

!SLIDE

## back to ActiveRecord

!SLIDE

ActiveRecord 3.0 is built on Arel

!SLIDE

When you lift the hood, Arel is there

!SLIDE
    @@@ ruby
    class Posts < ActiveRecord
      def for_topics(topics)
        where(
          self.arel_table[:topic].in(topics)
        )
      end
    end

!SLIDE

ActiveRecord classes are made of ARel objects

!SLIDE

ActiveRecord 3.1 uses prepared statements

!SLIDE

I still prefer Sequel

!SLIDE

but ActiveRecord is getting serious.

!SLIDE

(Okay, feel free to throw tomatos for the rest.)

