# frozen_string_literal: true

require "rake"

task default: [:build, :htmlproofer]

task :build do
  sh "bundle exec jekyll build"
end


task :htmlproofer => :build do
  sh "htmlproofer ./_site --disable-external --checks 'Links,Images,Scripts'"
end