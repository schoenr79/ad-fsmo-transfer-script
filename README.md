# Active Directory FSMO Transfer Script
Transfers and displays holder of FSMO Roles on Active Directory Domain Controllers

## About
A very nice batch script, how you can transfer FSMO Roles from one domaincontroller to a another. With some simple choices you can move roles between domaincontrollers in a AD environment.

NTDSUTIL.EXE of Windows Server Support Tools is used to wich is used by this script. It is installed by default on a Active Directory Domaincontroller.

## Known Issues
* [2017-07-01] UPDATE: Added Windows Server 2016 compatibility, transfer the naming master role. (Thanks to @Herculoid, reporing this issue)
* [2014-01-24] UPDATE: I noticed a small bug in the script, that i updated quickly. The Domain Naming Master role could not be found and displayed.
* Before you can use the script: Look if the path to NTDSUTIL.EXE is in the `%PATH%` variable, to call it globally. Or copy NTDSUTIL.EXE into the script directory. CHOICE.EXE is used to handle the choosable options in the script.
* Ensure that you have elevated rights to execute the script

## Examples
1. Script call: FSMOtransfer.bat [DNSDOMAIN]

Where [DNSDOMAIN] Must be a Fully Qualified Domain name (FQDN) of a existing Microsoft Active Directory Domain.

