require 'rubygems'
require 'rake'

task :default => :check

desc "Verify the environment is installed correctly"
task :check do
  require 'bundler/setup'

  require 'thor'
  shell = Thor::Base.shell.new

  rvm_path = File.expand_path(ENV['rvm_path'] || '~/.rvm')
  $LOAD_PATH.unshift File.join(rvm_path, 'lib')
  require 'rvm'
  if RVM.current.info.keys.grep(/ruby-1.9.3/).empty?
    shell.say_status "ERROR", 'Ruby 1.9.3 not found. Did you run: "rvm install 1.9.3"?', :red
  else
    shell.say_status "Success", 'RVM, Ruby and Bundler appear installed correctly', :green
  end
end
