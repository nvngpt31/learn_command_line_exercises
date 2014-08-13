cat cat cat cat cat cat cat cat cat cat

cat cat cat cat cat cat cat cat cat cat

cat cat cat cat cat cat cat cat cat cat
 
cat cat cat cat cat cat cat cat cat cat

cat cat cat cat cat cat cat cat cat cat

cat cat cat cat cat cat cat cat cat cat


Do More:
--------

###1) Make a few more text files and work with cat.
    Please see ex13a.txt and ex13b.txt in the chapter_13 directory

###2) Unix: Try cat ex12.txt ex13.txt and see what it does.
    It streams both files, one after the other

Other
-----

###1) Can you show me the contents of database.yml?
      Bills-MacBook-Pro:earthquake_grapher was3$ cat config/database.yml
      
      # MySQL.  Versions 5.0+ are recommended.
      #
      # Install the MYSQL driver
      #   gem install mysql2
      #
      # Ensure the MySQL gem is defined in your Gemfile
      #   gem 'mysql2'
      #
      # And be sure to use new-style password hashing:
      #   http://dev.mysql.com/doc/refman/5.0/en/old-client.html
      #
      default: &default
        adapter: mysql2
        encoding: utf8
        pool: 5
        username: root
        password:
        socket: /tmp/mysql.sock
      
      development:
        <<: *default
        database: earthquake_mapper_development
      
      # Warning: The database defined as "test" will be erased and
      # re-generated from your development database when you run "rake".
      # Do not set this db to the same as development or production.
      test:
        <<: *default
        database: earthquake_mapper_test
      
      # As with config/secrets.yml, you never want to store sensitive information,
      # like your database password, in your source code. If your source code is
      # ever seen by anyone, they now have access to your database.
      #
      # Instead, provide the password as a unix environment variable when you boot
      # the app. Read http://guides.rubyonrails.org/configuring.html#configuring-a-database
      # for a full rundown on how to provide these environment variables in a
      # production deployment.
      #
      # On Heroku and other platform providers, you may have a full connection URL
      # available as an environment variable. For example:
      #
      #   DATABASE_URL="mysql2://myuser:mypass@localhost/somedatabase"
      #
      # You can use this database configuration with:
      #
      #   production:
      #     url: <%= ENV['DATABASE_URL'] %>
      #
      production:
        <<: *default
        database: earthquake_mapper_production
        username: earthquake_mapper
        password: <%= ENV['EARTHQUAKE_MAPPER_DATABASE_PASSWORD'] %>

###2) What is in your Gemfile?
      Bills-MacBook-Pro:learn_command_line_exercises was3$ cat Gemfile
      
      source 'https://rubygems.org'
      
      gem 'guard-rubocop'
