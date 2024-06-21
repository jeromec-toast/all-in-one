### EDI:
1. aws clouldwatch - insight log check:
fields @timestamp, @message, @logStream, @log
| filter @message like 'Hillcrest - Copy.csv'
| sort @timestamp desc
| limit 1000

# Lamda
xc-edi-loader - read sqs and trigger parser lamda
xc-edit-parser

# FTP
https://ftp.xtrachef.com/
ftpuserdev
Century@7

# Source
xtrachef-aws-lambda-edi - template file save here and xc-edi-template record creating
xtrachef-angular-edi-management - secoundary vendor mappig, ftp path mapping
dynamodb table - xc-edi-config

# Process
configure the edi config for the template with the tenant
-- vendor code is the customstring
-- location code in edi config have the same code in excel file
-- ftp path
-- global vendor should be mapped
updload edi file to fpt 
trigger lamda for loader

# Table
edi_invoice
------------------------------------


### Internal System Run:
1. install npm all the project folder using cmd 
2. build it
3. kitchen synch run two times
4. build the secret config project
5. npm install for the main xtrachef project in which folder package.json
------------------------------------

### Aurora | Postgresal:


### File Based Extarct:
