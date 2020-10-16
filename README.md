## Project Details
# Flask Web Framework Project

Agenda:
Building a static Web page with Python Flask Web Framework in Google Cloud Platform using Terraform Orchestration tool.

Tools/ Technologies/ Platforms used :
Git
Terraform (IAC- Infrastructure as code tool)
Python Flask web framework
Google cloud platform

Steps:
Creating a project in google cloud platform ( Used here to create and run virtual machines on Google infrastructure.).
Setting up a service account key (key type : json ), which Terraform will use to create and manage resources in this Google Cloud project.
  Setting up terraform :
    - Creating a main.tf (The contents of this file describe all of the Google Cloud resources that will be used in the project.)
    - Download the latest version of the Google cloud terrafrom provider and build a .terraform directory.

Creating a compute instance:
  - Initialize terraform again to download and install an extra plugin for naming a random instance id.
  - Get the preview of what will be craeted
  - Run (terraform apply) through which terraform call the Google cloud API's to create an instance.
  - Now instance is created.
SSH access to compute engine instance :
  - Add a public SSH key to the Compute Engine instance to access and manage it by modifying a terraform file.
  - Again see the preview of what is going to be implemented
  - Apply the changes.

Use a terraform varaible which is helper to expose the instance's ip address.
Apply the changes
Get the instance ip address
Making sure firewall rules ( applied to the traffic b/w internet and computer) to be in place before you can use SSH to connect to the instance.
Validate everything by connecting the ip address with SSH.

Building a Python flask server app:
- Building an app so that you can have a single file describing your web server and test endpoints.
- Adding a new python file with a greeting and running it
- Confirm the greeting is returned by running curl ( flask serves traffic through - localhost:5000 ).
- Open the port 5000 on the instance through a change in terraform file and review the plan and apply to create the firewall rule.
- Point the ip and port to browser to confirm the server is up and running.


Brief Concepts :
Terraform Orchestration:
  - Terraform as an infrastructure provisioning tool that communicates with VMware, AWS, GCP, and        ensures infrastructure deployment.
  - Terraform is a tool for building, changing, and versioning infrastructure safely and efficiently.
  - Terraform generates an execution plan describing what it will do to reach the desired state, and     then executes it to build the described infrastructure.
  - The infrastructure Terraform can manage includes low-level components such as compute instances,     storage, and networking, as well as high-level components such as DNS entries, SaaS features, etc

Git Deployment Process :
  - Git is a very popular version control system used to implement development workflows.
  - Use git init for intializing
  - Use git push command for upload local repository content to a remote repository.
  - git checkout for naviagating b/w branches.

Protocols :
TCP : Transmission control protocol (for sending and recieving data )
HTTP : It is a request-response protocol and is an application protocol for distributed, collaborative, and hypermedia information systems.
SSH : A cryptographic network protocol for operating network services securely over an unsecured network.The SSH protocol uses encryption to secure the connection between a client and a server.

Firewall Rules :
    A firewall rule can be applied to traffic from the Internet to your computer (inbound), or from your computer to the Internet (outbound). A rule can also be applied to both directions at the same time.
    A firewall rule consists of firewall services , which specify the type of traffic and the ports that this type of traffic uses. For example, a rule called Web browsing has a service called HTTP, which uses the TCP and port number 80.
   
Server Ports :
- Port is a communication Endpoint
- 65,535 ports are present on a server
- Ports 0 to 1024 are called well-known ports, and are conventionally associated with the most common types of network service. Web servers use port 80, SSH servers use port 22.

GCP compute engine :
Compute Engine lets you create and run virtual machines on Google infrastructure. Compute Engine offers scale, performance, and value that lets you easily launch large compute clusters on Google's infrastructure.

