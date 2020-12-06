RAILS_VERSIONS = %w[3.1 3.2 4.0 4.1 4.2 5.0 5.1 5.2 6.0 6.1].freeze

RAILS_VERSIONS.each do |rails_version|
  appraise "rails-#{rails_version}" do
    gem 'rails', "~> #{rails_version}.0"
    # Webrick is missing on ruby-3
    gem 'webrick'
  end
end

SERVER_NAMES = %w[puma falcon thin].freeze

SERVER_NAMES.each do |server_name|
  appraise server_name do
    gem server_name
  end
end
