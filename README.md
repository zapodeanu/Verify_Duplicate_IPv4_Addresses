 
# Verify_Duplicate_IPv4_Addresses

This repo is for a simple script to verify if a CLI template will create duplicated IPv4 addresses with addresses. 
This script will use the Cisco DNA Center APIs to access the device and client inventories.


## Installation
requirements.txt provides the list of Python libraries needed. The script has been tested on Cisco DNA Center version 1.2.10


## Usage

This script will load the CLI template from the file with the name "configuration_template.txt". Update the template file with the desired content. 

- This script will:
  - load a file with a CLI configuration that is intended to be deployed to a network device
  - identify and validate the IPv4 addresses that will be configured on interfaces
  - search using the DNA Center inventory database if these IPv4 addresses are configured on any interfaces, regardless the operational state of the interface, if "up" or "down"
  - find if any clients are using the IPv4 addresses
  - determine if deploying the configuration file will create an IP duplicate
 
## Test

You may test this code on the DevNet Cisco DNA Center sandboxes. Change the config.py file to match the Cisco DNA Center IP address, username and password for your environment.