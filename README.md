# KeyManagementServiceTips
Slmgr commands to aid in configuration and testing of a new Windows Volume Activation Services Key Management Service server.

https://youtu.be/lKGY6jwhhtk
![Windows Volume Activation Key Management Service Tips](https://github.com/ShotokuTech/KeyManagementServiceTips/blob/main/kms%20tips.png)

All commands require elevated command prompt.

Turn off auto publish to DNS.
Slmgr /cdns

Detailed activation information in Wscript window.
Slmgr /dlv all

Detailed activation information in the command prompt.
Cscript.exe slmgr.vbs /dlv all

This command turns off host caching.
Slmgr /ckhc

This command forces the client to use the new Key Management Service server for activation.
Slmgr /skms New-KMS.NewDomain.com

Now run this to activate using the new server.
Slmgr /ato

Check the results with this command.
Slmgr /dli

Remove the forced Key Management Service server entry.
Slmgr /ckms

Turn host caching back on with this command.
Slmgr /skhc

Slmgr.vbs Options for Volume Activation
https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn502540(v=ws.11)

How to prevent publishing SRV _VLMCS from any computer of domain?
https://social.technet.microsoft.com/Forums/en-US/fff35ca6-b427-4dab-a396-5b6f777af3c2/how-to-prevent-publishing-srv-vlmcs-from-any-computer-of-domain?forum=winserversetup

Deploy KMS Activation
https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn502531(v=ws.11)

Microsoft Office 2013 Volume License Pack 
https://www.microsoft.com/en-us/download/details.aspx?id=35584

Microsoft Office 2016 Volume License Pack 
https://www.microsoft.com/en-us/download/details.aspx?id=49164
