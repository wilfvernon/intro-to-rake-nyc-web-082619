namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts 'hola de Rake!'
  end

end

task :environment do
  require_relative './config/environment'
end

desc 'opens a Pry environment in the console'
task :console => :environment do
  Pry.start 
end

namespace :db do
  desc 'migrates changes to the database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'populates the table with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end