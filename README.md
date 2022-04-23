# Linux_Terrorists
A simple bash project for beginners.  Review Flight.Manifests against a FAA no-fly list.

#!/usr/bin/bash

# Purpose:  FAA flight screening script

# Algorithm:
# 1) Open a directory that has a list of 'Flight Manifests'.
#      note: Flight Manifests are named Flight_???.manifest
#            Flight_103.manifest
#            Flight_20.manifest
# 2) For each 'Flight Manifest' go through it one line at a time
#       - parse each line into its fields:
#PassportID,First Name,Middle Name,Last Name
#US463924034,Geo,ZESATI,MCKNIGHT
#       - compare the PASSPORTID of the traveler against the PassportIDs in the DoNotLetFly.csv file
#           (This is the No-Fly List provided by government security)
# 3) Prepare a report named (Flight_???.FaaReport) (one report per manifest file)
#    The report needs to have the following format:
#NoFly: 4 (count of BadGuys here)
#PassportID,First Name,Middle Name,Last Name
#PassportID,First Name,Middle Name,Last Name
#PassportID,First Name,Middle Name,Last Name
#PassportID,First Name,Middle Name,Last Name
#OK To Fly: 100 (count of GoodGuys here)
#PassportID,First Name,Middle Name,Last Name
#PassportID,First Name,Middle Name,Last Name
#...
#PassportID,First Name,Middle Name,Last Name

##### HINT: These are linux commands that might be helpful to you to lookup and consider using:
# grep
# cut -d"," -f 1,2
# wc -l
#
