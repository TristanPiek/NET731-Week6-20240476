# NET731-Week6-20240476NET731
This Repository is for my Week 6 NET practical. 

Tristan Piek

20240476


## Secure Score Summary

A security statistic known as Secure Score is available with Microsoft Defender for Cloud. This is a reflection of the
compliance to which Azure resources adhere to the security requirements established by Microsoft. The higher the score, the
more robust the security features are and their posture and the lower the score, the more vulnerable they can be to attacks
that are contained within it.


### Top 3 Recommendations


1. All network ports should be restricted on network security groups associated to your virtual machine - This one was fixed
2. Azure Backup should be enabled for virtual machines
3. Email notification for high severity alerts should be enabled



## Why I Chose this Recommendation Fix For SSH

While I was reviewing the recomendation that Defender for Cloud suggested, I saw that it was the SSH that was the issue, the virtual machine had a incoming NSG rule allowing any internet source to access port 22 for SSH features.
As Recommended any open management ports are a major cloud security issue, therefore I fixed this. Instead of confining the rule to IP addresses, I deleted it entirely because remote SSH was never specified in the scenario that
was givin. When I deleted the SSH rule, it immediately made the virtual machine less sensitive to internet threats and brought its settings up to Azures standards. This fix will enhance its security by limiting unnecessary
external access.


## What I Configured on Update Manager


The Azure Update Manager was set up to check for updates and deploy them at predetermined intervals. Operating system security was thus enhanced and vulnerabilities are mitigated by regular patch management.


