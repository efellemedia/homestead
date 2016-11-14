require 'yaml'

VAGRANTFILE_API_VERSION = "2"

confDir = $confDir ||= File.expand_path("~/.homestead")
homesteadPath = confDir + "/Homestead.yaml"

require File.expand_path(File.dirname(__FILE__) + '/src/scripts/homestead.rb')

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    if File.exists? homesteadPath then
        Homestead.configure(config, YAML::load(File.read(homesteadPath)))
    end
end
