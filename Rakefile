desc 'outputs hello to the terminal'

task :environment do
  require_relative './config/environment'
end

namespace :greeting do 
  task :hello do 
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do 
    puts "hola de Rake!"
  end
end

desc 'migrate changes to your database' 
desc 'seed the database with some dummy data'
namespace :db do 
  task :migrate => :environment do 
    Student.create_table
  end

  task :seed do 
    require_relative './db/seeds.rb'
  end
end

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start 
end

