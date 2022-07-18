# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** VM and App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*

VMs are relatively more expensive than web apps. Regardless of the fact that VMs run on a pay as you go (PAYG) payment schedule, one still has to be accountable for the additional cost of paying the staff to manage the VMs, configuring, updating, maintaining, scaling and purchase of addiional softwares also. With the use of app service, one has to always pay for the service plan whether in use or not, but it affords the developer the luxury to focus on application development solely, and various pricing tiers are available depending on ones choice.

VMs and app service are both scalable, with VMs having the virtual machine scale sets (vmss) as a means of autoscaling, while in app service, autoscaling is also supported and could be vertical (increase the resources allocated) or horizontal(increase number of instances).

The VMs and app service are both highly available, as azure services have an estimate of about 99.95% SLA.

In terms of work flow, VMs workflow can be automated, but would require advanced management configuiration, while for app services, continuous deployment is supported, hence after initial deployment, the developer can be concerned with just pushing the code to production branch in the version control system, and it is updated automatically in the app service.


- *Choose the appropriate solution (VM or App Service) for deploying the app*

For this project, I would be utilizing an app service (web app).

- *Justify your choice*

Reason: The project is a simple content management system for publishing and viewing articles, so a web app is proposed for deployment as it removes the need for additional cost of managing the VMs as it is not specified as a critical business solution and it allows for more concentration on the app development. It is highly available with an SLA of 99.95%, supports continuous deployment from version control systems and also can be easily auto-scaled up and down easily depending on the traffic the site would receive.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

For my choice of deployment to change from the use of a web app to a virtual machine(VM), it would be when my application would require a hardware computing resource of over 14gb of RAM and/ or 4 VCPU's to handle the load per instance, or also if the application becomes a means of storing critical business information, requiring business specific softwares and configurations.