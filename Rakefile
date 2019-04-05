desc 'dependency for #console and #migrate; provides access to .config/environment'
task :environment do
  require_relative './config/environment.rb'
end

desc 'opens a pry console'
task :console => :environment do
  Pry.start
end

namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs "hola de Rake!" to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'creates a table in the database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seeds the database with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end
