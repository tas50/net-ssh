source 'https://rubygems.org'

# Specify your gem's dependencies in mygem.gemspec
gemspec

gem 'byebug', group: %i[development test] if !Gem.win_platform? && RUBY_ENGINE == "ruby"

if ENV["CI"]
  gem 'codecov', require: false, group: :test
  # simplecov 1.x declares ruby >= 3.2, but passes an anonymous block
  # parameter inside a block, which is a SyntaxError before Ruby 3.4.
  gem 'simplecov', (RUBY_VERSION < '3.4' ? '< 1.0' : '>= 0'), require: false, group: :test
end

gem 'webrick', group: %i[development test] if RUBY_VERSION.split(".")[0].to_i >= 3
