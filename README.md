# Verify_Duplicate_IPv4_Addresses

This repo is for a simple script to verify if a CLI template will create duplicated IPv4 addresses with addresses. 
This script will use the Cisco DNA Center APIs to access tge device and client inventories.

- This script will:
 - load a file with a CLI configuration that is intended to be deployed to a network device
 - identify the IPv4 addresses that will be configured on interfaces
 - search in the DNA Center inventory database if these IPv4 addresses are configured on any interfaces, regardless the operational state of the interface, if "up" or "down"
 - find if any clients are using the IPv4 addresses
 - Determine if deploying the configuration file will create an IP duplicate