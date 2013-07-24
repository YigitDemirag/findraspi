#!/bin/bash

RaspiMac="7c:dd:90"

echo Searching for Raspberry Pi...
for i in 1 2 3 4 5
do
    IPFound=$(arp -a | grep $RaspiMac | grep -Eo '[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}')
    if [ -n "${IPFound}" ]; then
	echo Raspberry Pi IP is found : $IPFound
	RESULT="64"
	PING=$(ping $IPFound -c 1 | grep 64 | awk '{print $1}')
	if [ "$RESULT" != "$PING" ]
	then
	   echo 'But pinging is failed'
	else
	   echo 'And pinging is successful.'  
	fi
	break
    fi
done
if [[ -z "$IPFound" ]]; then
   echo Raspberry not found.
else
   echo Connecting Raspberry over SSH...
   ssh pi@$IPFound
fi

