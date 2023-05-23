##!/bin/bash
#starting assetfinder
assetfinder --subs-only $1 | tee -a domains.txt
#starting amass
amass enum --passive -d $1 -o domains
#removing duplicate entries
sort -u domains -o domains
#filtering the domains
cat domains | filter-resolved | tee -a domains.txt
rm domains
#checking for alive domains
echo "\n\n[+] Checking for alive domains..\n"
cat domains.txt | ~/go/bin/httprobe | tee -a alive.txt
