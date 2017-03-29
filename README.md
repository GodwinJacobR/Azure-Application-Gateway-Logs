# Azure-Application-Gateway-Logs
This Power shell script downloads multiple application gateway logs and makes a report out of it.shell 

Consider you have your website is hosted on Azure, then most likely you would be using Azure Load Balancer or Azure Application Gateway.

Application Gateway log is one log which helps you understand the number of hits made to your site.

Consider you have your Application Gateways in multiple Azure regions, you can still use this script to collate logs from multiple Application Gateways.

You can capture all your Application Gateway Logs in your Azure Storage Account. By default, this is disabled. You may have to turn on diagnostics and select the option *Archive to Storage Account*.

Application Gateway logs so many attributes. This script would only collect information like Client ip, Request URI, time, response time etc. and then exports them into a csv file.

Once all the needed logs are collected, the script would calculate the number of hits made to all the unique URIs in your site with the average reponse time and exports it into a csv file which can be sent to many through e-mail. This report can give a fair idea about the number of hits made to your site and also its performance. This csv file can then be fed into some visualization tools to get a detailed analysis of it.
