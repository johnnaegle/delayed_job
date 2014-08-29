source 'https://rubygems.org'

gem 'rake'

platforms :ruby do
  gem 'sqlite3'
end

platforms :jruby do
  gem 'jruby-openssl'
  gem 'activerecord-jdbcsqlite3-adapter'
end

group :test do
  gem 'activerecord', (ENV['RAILS_VERSION'] || ['>= 3.2', '< 4.2'])
  gem 'actionmailer', (ENV['RAILS_VERSION'] || ['>= 3.2', '< 4.2'])
  gem 'coveralls'
  gem 'rspec', '>= 3'
  gem 'rubocop', '>= 0.25'
  gem 'simplecov', '>= 0.9'

  if ENV['RAILS_VERSION'] == '4.2.0.beta1'
    # see https://github.com/rails/rails-deprecated_sanitizer/pull/1
    gem 'rails-deprecated_sanitizer', github: 'rails/rails-deprecated_sanitizer'
  end

end

gemspec
