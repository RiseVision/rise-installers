# Rise-core Node

This Microsoft Azure template deploys a single rise-core which will connect to the public rise-core network.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/" target="_blank"><img src="http://azuredeploy.net/deploybutton.png"/></a>
<a href="http://armviz.io/#/?load=" target="_blank"><img src="http://armviz.io/visualizebutton.png"/></a>

# Template Parameters

When you click the Deploy to Azure icon above, you need to specify the following template parameters:

* `adminUsername`: This is the account for connecting to your rise-core host.
* `adminPassword`: This is your password for the host.  Azure requires passwords to have One upper case, one lower case, a special character, and a number.
* `dnsLabelPrefix`: This is used as both the VM name and DNS name of your public IP address.  Please ensure an unique name.
* `vmSize`: This is the size of the VM to use.  Recommendations: D v2 series is recommended

# Getting Started Tutorial

* Click the `Deploy to Azure` icon above
* Complete the template parameters, choose your resource group, accept the terms and click Create
* Wait about 15 minutes for the VM to spin up and install the software
* Connect to the VM via SSH using the DNS name assigned to your Public IP
* rise-core will already be running. If you want to alter configuration, run ```forever stopall```, make your changes, then run ```npm start``` from the rise-core directory.