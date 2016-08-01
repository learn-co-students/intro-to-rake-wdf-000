desc 'outputs hello to the terminal'
namespace :greeting do
  task :hello do
    puts "hello from Rake!"
  end

  task :hola do
    puts "hola de Rake!"
  end
end

desc 'migrate changes to your database'
namespace :db do
  task :migrate => :environment do
    Student.create_table
  end

  task :seed do
    require_relative './db/seeds.rb'
  end

  task :environment do
    require_relative './config/environment'
  end

  desc 'drop into the Pry console'
  task :console => :environment do
    Pry.start
  end
end
