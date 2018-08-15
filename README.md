# blockhead-bosh-release
A BOSH release for Blockhead broker

# Deploying the Broker to Bosh-Lite
**NOTE** The manifest in the release works with the cloud config that can be found at
https://github.com/cloudfoundry/cf-deployment/iaas-support/bosh-lite/cloud_config.yml

Run `bosh -d blockhead deploy blockhead.yml --vars-store creds.yml`

The manifest will create a local release.
