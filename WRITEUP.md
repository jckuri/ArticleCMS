# WRITE-UP

## Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

### Costs

Virtual Machines are more expensive than App Services. Virtual Machines have a lower up-front cost compared to purchasing and maintaining hardware.

With App Services, cost varies based on the plan you choose and you’re always paying for the service plan, even if your services or application isn’t running.

### Scalability & Availability

Multiple Virtual Machines can be grouped to provide high availability, scalability, and redundancy. There are two options when it comes to scaling: Virtual Machine Scale Sets and Load Balancers.

App Services have high availability, auto-scaling and support of both Linux and Windows environments. App Services have Vertical or Horizontal scaling. Vertical scaling increases or decreases resources allocated to our App Service, such as the amount of vCPUs or RAM, by changing the App Service pricing tier. Horizontal scaling increases or decreases the number of Virtual Machine instances our App Service is running.

### Workflow

**Azure Virtual Machines (VMs)** provide infrastructure as a service (IaaS) by allowing you to create and use virtual machines in the cloud. VMs allow you full access and control of the VM. There is support of both Linux and Windows VMs. VMs allow for the installation of custom images and are an excellent choice for migrating from an on-premises server to the cloud. VMs can be more time consuming for the developer than other compute options.

**Azure App Service** is an HTTP-based service for hosting web applications, REST APIs, and mobile back ends. It is a Platform as a Service (PaaS) that allows a developer to focus on the application while Azure takes care of the infrastructure. App Services provide continuous deployment model using GitHub, Azure DevOps, or any Git repo. You have limited access to the host server, so you are unable to control the underlying OS or install software on the server. While they support multiple languages, as noted in the benefits above, they are limited to just using those languages (as of when this course was built).

### Decision: App Service

I chose an App Service to develop this website:<br/>
http://blog-post.azurewebsites.net/

### Justification

- App Services are perfect for small web applications.
- Since we are building a small web application, the free tier is enough. We don't need high scalability and availability.
- We are using Python and Flask to develop the web application. And Azure App Services support Python.
- We don't need to install additional software.
- App Services provide Paas (Platform as a Service). So, developers are focused on programming the web application and let Azure take care of the infrastructure.
- App Services provide continuous deployment through GitHub.
- Virtual machines can ease the migration of preexisting code. But I'm not migrating a preexisting code.

## Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

- If we were migrating a preexisting software from an on-premises server to the cloud, Virtual Machines would ease this migration.
- If we were deploying a large web applications whose requirements include high scalability and high availability, Virtual Machines could become a more attractive choice.
- If costs didn't matter too much, we would forget the free tier of App Services and choose expensive Virtual Machines.
- If the hardware requirements outsized 14GB of memory and 4 vCPU cores per instance, Virtual Machines would be required.

--------------------------------------------------------------------------------

# Virtual Machines vs. App Services

https://classroom.udacity.com/nanodegrees/nd081-ent/parts/0905e741-5b5f-485e-a20d-7dce7f5957b9/modules/e866a6d8-695c-4f8a-aae8-af3dcb5a721f/lessons/b2ca2f8f-bf72-48aa-a18f-06ccc5b7181c/concepts/239ca133-a070-478a-ae2d-b0a33d8e9b22

## Virtual Machines

**Azure Virtual Machines (VMs)** provide infrastructure as a service (IaaS) by allowing you to create and use virtual machines in the cloud.

Some of the benefits of VMs are:

- VMs allow you full access and control of the VM.
- Lower up-front cost compared to purchasing and maintaining hardware.
- Support of both Linux and Windows VMs.
- Multiple types to choose from, such as compute or memory-optimized VMs, along with varying amounts of CPU, RAM and storage.
- VMs allow for the installation of custom images and are an excellent choice for migrating from an on-premises server to the cloud.
- Multiple VMs can be grouped to provide high availability, scalability, and redundancy. There are two options when it comes to scaling—Virtual Machine Scale Sets and Load Balancers. These will be covered in a different course.

Some of the limitations of VMs are:

- They are more expensive
- They can be more time consuming for the developer than other compute options

## App Service

**Azure App Service** is an HTTP-based service for hosting web applications, REST APIs, and mobile back ends. It is a Platform as a Service (PaaS) that allows a developer to focus on the application while Azure takes care of the infrastructure.

Some of the benefits of using an App Service are:

- Support of multiple languages, such as .NET, .NET Core, Java, Ruby, Node.js, PHP, or Python
- High availability, auto-scaling and support of both Linux and Windows environments.
- Continuous deployment model using GitHub, Azure DevOps, or any Git repo.
- Vertical or Horizontal scaling. Vertical scaling increases or decreases resources allocated to our App Service, such as the amount of vCPUs or RAM, by changing the App Service pricing tier. Horizontal scaling increases or decreases the number of Virtual Machine instances our App Service is running.
- You can set the amount of hardware allocated to host your application, and cost varies based on the plan you choose. There are three different tiers - Dev/Test, Production, and Isolated. We’ll be using the free option within Dev/Test for the exercises in this course.

Some of the limitations of an App Service are:

- You have limited access to the host server, so you are unable to control the underlying OS or install software on the server.
- You’re always paying for the service plan, even if your services or application isn’t running.
- There are hardware limitations, such as a maximum of 14GB of memory and 4 vCPU cores per instance
- While they support multiple languages, as noted in the benefits above, they are limited to just using those languages (as of when this course was built).

