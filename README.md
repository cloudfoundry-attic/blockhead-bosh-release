# blockhead-bosh-release
A BOSH release for Blockhead broker

# Deploying the Broker to Bosh-Lite
**NOTE** The manifest in the release works with the cloud config that can be found at
https://github.com/cloudfoundry/cf-deployment/iaas-support/bosh-lite/cloud_config.yml

1. Edit the value of `blockhead.url` in the releases section of `blockhead.yml`
   to the location of this repo. Replace the value of `<location-of-blockhead-bosh-release>`
   with the location
2. Run `bosh -d blockhead deploy blockhead.yml --vars-store creds.yml`
