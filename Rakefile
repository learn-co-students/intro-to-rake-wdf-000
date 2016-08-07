namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts 'hello from Rake!'
  end

  desc 'greets you, master!'
  task :hola do 
    puts 'hola de Rake!'
  end
end

task :environment do
  require_relative './config/environment'
end

desc "start up pry console"
task :console => :environment do
  Pry.start
end

desc 'migrate changes to your database' 
namespace :db do 
  task :migrate => :environment do 
    Student.create_table
  end
  
  task :seed do 
    require_relative './db/seeds.rb'
  end

end
