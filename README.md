#  vagrant-tracing

this project has been superseded by https://github.com/attachmentgenie/vagrant-observability

## Requirements
    Virtualbox                  => https://www.virtualbox.org
    Vagrant                     => http://www.vagrantup.com
    vagrant-hostmanager         => vagrant plugin install vagrant-hostmanager
    vagrant-puppet-install      => vagrant plugin install vagrant-puppet-install
    vagrant-cachier  (optional) => vagrant plugin install vagrant-cachier
    
## Preparation

    git submodule update --init
    bundle install
    
## Setup

    vagrant up

## Inspec tests

    bundle exec rake
    bundle exec rake inspec[centos7] 

## TLDR

### (G)UI interfaces

## TLDR
    
    - name: minio
      public_vhosts:
        - http://minio.tracing.vagrant:9090 admin:supersecret
    - name: tempo
      public_vhosts:
        - http://tempo.tracing.vagrant admin:secret
