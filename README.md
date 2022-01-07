[comment]: # "Auto-generated SOAR connector documentation"
# NetBIOS

Publisher: Phantom  
Connector Version: 1\.0\.13  
Product Vendor: Generic  
Product Name: NetBIOS  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 3\.0\.251  

This app implements various investigative actions using the NetBIOS protocol

### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a NetBIOS asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**ip** |  required  | string | IP to Lookup \(for TEST CONNECTIVITY\)

### Supported Actions  
[test connectivity](#action-test-connectivity) - This action runs a lookup ip action to test connection  
[lookup ip](#action-lookup-ip) - Attempts a lookup of the hostname for the provided IP  

## action: 'test connectivity'
This action runs a lookup ip action to test connection

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'lookup ip'
Attempts a lookup of the hostname for the provided IP

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip** |  required  | IP to resolve | string |  `ip` 
**port** |  optional  | Port number | numeric | 
**timeout** |  optional  | Seconds before timeout \(Default\: 30\) | numeric | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.data\.\*\.hostnames\.\* | string | 
action\_result\.status | string | 
action\_result\.summary | string | 
action\_result\.message | string | 
action\_result\.parameter\.ip | string |  `ip` 
action\_result\.parameter\.port | numeric | 
action\_result\.parameter\.timeout | numeric | 