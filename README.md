# Bug Bounty Scripts

Just a small collection of scripts that can be used for bug bounty

***Recon***
-----------------------------------------------------------------------------------------------------------------------------------------
1a.   1a-subdomain-enumeration-using-Amass-and-a-targetFile

Save the script in a file (e.g., amass_enumeration.sh), make it executable (chmod +x amass_enumeration.sh), 
and then you can run it by providing a file containing a list of target domains. Each domain should be on a separate line in the file.

For example, if you have a file named targets.txt with the following contents:
example.com,
example.net,
example.edu

You can run the script like this:
./amass_enumeration.sh targets.txt

The script will create an amass_output directory (if it doesn't exist) to store the output files. 
Each target will have a separate text file with the enumerated subdomains.
Please make sure you have Amass installed on your system and accessible in the PATH before running this script.

------------------------------------------------------------------------------------------------------------------------------------------
2a.   2a-subdomain-enumeration-using-Sublist3r-and-a-targetFile

Save the script in a file (e.g., sublist3r_enumeration.sh), make it executable (chmod +x sublist3r_enumeration.sh), 
and then you can run it by providing a file containing a list of target domains. Each domain should be on a separate line in the file.

For example, if you have a file named targets.txt with the following contents:
example.com,
example.net,
example.edu

You can run the script like this:
./sublist3r_enumeration.sh targets.txt

The script will create a sublist3r_output directory (if it doesn't exist) to store the output files. 
Each target will have a separate text file with the enumerated subdomains.
Please make sure you have Sublist3r installed on your system and accessible in the PATH before running this script. 
You may need to install any required dependencies for Sublist3r as well.

Note: Sublist3r relies on search engine queries and DNS queries, 
so its effectiveness may vary depending on the availability and coverage of those sources.

------------------------------------------------------------------------------------------------------------------------------------------
3a. - 

------------------------------------------------------------------------------------------------------------------------------------------


***Vulnerability Scanning***
-------------------------------------------------------------------------------------------------------------------------------------------
1b.    1b-vuln-scan-using-ZAP-and-a-targetFile

Save the script in a file (e.g., zap_scan.sh), make it executable (chmod +x zap_scan.sh), 
and then you can run it by providing a file containing a list of target URLs or IP addresses. 
Each target should be on a separate line in the file.

For example, if you have a file named targets.txt with the following contents:
https://example.com,
http://example.net,
http://exmaple.edu

You can run the script like this:
./zap_scan.sh targets.txt

The script assumes you have ZAP and zap-cli installed on your system and accessible in the PATH. 
It starts ZAP in daemon mode, waits for it to initialize, and then launches a quick scan for each target in the file 
using the zap-cli command-line interface. 
It saves the ZAP report in HTML format for each target in the zap_output directory.

Note: Adjust the sleep time in the script if necessary, depending on how long it takes for ZAP to start on your system.

Please ensure you have the necessary permissions and have ZAP properly configured before running this script.

---------------------------------------------------------------------------------------------------------------------------------------------
