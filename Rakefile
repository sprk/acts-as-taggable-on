require 'rubygems'
require 'bundler/setup'

desc 'Default: run specs'
task :default => :spec

desc 'Copy sample spec database.yml over if not exists'
task :copy_db_config do
  cp 'spec/database.yml.sample', 'spec/database.yml'
end

task :spec => [:copy_db_config]

require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new do |t|
  t.pattern = 'spec/**/*_spec.rb'
end

Bundler::GemHelper.install_tasks
