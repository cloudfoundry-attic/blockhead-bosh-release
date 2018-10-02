# blockhead-bosh-release
A BOSH release for Blockhead broker

# Deploying the Broker to Bosh-Lite

## ADD Services

service descriptions for services offered by the broker (`service.yml` files) should go under `src/services`. The broker provides an Ethereum node service as an example in the `src/services` directory.

## Deploy

**NOTE** The manifest in the release works with the cloud config that can be found at
https://github.com/cloudfoundry/cf-deployment/iaas-support/bosh-lite/cloud_config.yml

Run `bosh -d blockhead deploy blockhead.yml --vars-store creds.yml`

The manifest will create a local release.

## Credentials

Broker is deployed with user `admin` by default. You can get the generated password for the admin user by running: 

    cat creds.yml | grep blockhead_broker_password

default username `admin` can be changed in the `blockhead.yml` manifest.
