<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Set Up a Web App in the Cloud

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-devops-vscode)

**Author:** cdumanyie@gmail.com  
**Email:** cdumanyie@gmail.com

---

## Set Up a Web App Using AWS and VS Code

![Image](http://learn.nextwork.org/warm_vermilion_kind_finger_lime/uploads/aws-devops-vscode_7a1de541)

---

## Introducing Today's Project!

Today’s task introduces the basics of building a web application using Amazon Web Services (AWS) and Visual Studio Code (VS Code). The goal is to help you understand how modern applications are created and deployed in a cloud environment.

You begin by learning how AWS provides scalable infrastructure, allowing you to run applications without physical servers. It offers services that support hosting, storage, and application management. At the same time, VS Code is used to write and manage your code efficiently with useful tools and extensions.

The process involves setting up your development environment, creating a simple web app, and testing it locally before deploying it to AWS. This helps you understand the connection between coding and deployment.

Overall, this task introduces key DevOps concepts and prepares you for more advanced topics like automation, continuous integration, and managing applications in the cloud.                                                               

I will begin my next project immediately after successfully uploading this one to my GitHub repository. Once the code, configurations, and documentation are properly pushed and verified, I plan to move straight into the next task without delay. This approach helps me maintain momentum and build consistency in my learning process.
Uploading the project ensures that my work is safely stored, version-controlled, and accessible for future reference or collaboration. It also allows me to review what I’ve done, identify areas for improvement, and apply those lessons to the next project.
By transitioning immediately, I can reinforce the skills I’ve gained from working with tools like Apache Maven and cloud platforms such as Amazon Web Services. Overall, continuing right away keeps me productive and helps me steadily advance in building and deploying more complex applications.                                                                                                                       

I worked on this project today to strengthen my practical understanding of cloud-based application deployment and to apply what I have been learning in a real-world context. Using Amazon Web Services allowed me to move beyond theory and actually configure and manage a live environment. By launching and working with an Amazon EC2 instance, I was able to gain hands-on experience with server setup, remote access, and application hosting.
Another reason for doing this project was to improve my familiarity with essential development and deployment tools. Working with Apache Maven and Apache Tomcat helped me understand how applications are built, packaged, and deployed in a structured way.
Additionally, I wanted to build confidence in troubleshooting common issues like connection drops and permission errors. Overall, the project was an opportunity to develop practical skills, reinforce my learning, and prepare for more advanced cloud and DevOps tasks in the future.                           

### Key tools and concepts

In this project on setting up a web application in the cloud, I learned several key services and core concepts using Amazon Web Services. A major service was Amazon EC2, which allowed me to create and manage a virtual server to host the application. This introduced the concept of Infrastructure as a Service (IaaS), where resources are provided on demand.
I also learned how to securely connect to the server using SSH and key pairs instead of passwords. Additionally, AWS Identity and Access Management helped me understand how to manage permissions and control access to resources.
On the development side, I used Apache Maven to manage dependencies and build the project, and Apache Tomcat to deploy and run the web application.
Overall, the project strengthened my skills in cloud deployment, configuration, and troubleshooting.                                                                                                                                                                       

### Project reflection

It took me about two weeks to complete this project of setting up a web application in the cloud using Amazon Web Services. The process involved launching and configuring an Amazon EC2 instance, setting up the development environment, installing necessary tools, and deploying the application.
However, the timeline was extended due to a few challenges. One major delay was my poor internet connection, which made it difficult to maintain stable SSH sessions and slowed down package installations and updates. Frequent disconnections meant I had to reconnect multiple times, interrupting my workflow.
Another issue was the need to repeatedly sign in to my AWS Identity and Access Management account, which added extra time and sometimes disrupted continuity during setup.
Despite these setbacks, I was able to complete the project successfully. The experience improved my patience, troubleshooting ability, and overall understanding of cloud-based application deployment.                             

One thing I didn’t expect in this project was how frequently connection and environment issues would interrupt the workflow. While setting up the web application on Amazon EC2, I assumed the process would be mostly straightforward once the instance was running. However, I encountered unexpected SSH disconnections, permission errors, and session timeouts that required additional troubleshooting.
I also didn’t anticipate how important configuration details would be, such as correct user access, file permissions, and server settings. Small misconfigurations could completely block progress, even when the main setup seemed correct. Working with tools like Apache Tomcat and Apache Maven further highlighted the need for precise setup and compatibility between components.
Overall, the project taught me that cloud development is not just about deployment, but also about diagnosing issues, maintaining stable connections, and understanding how different systems interact behind the scenes.        

---

## Launching an EC2 instance

### What I did in this step

In this step, you will launch a new EC2 instance on AWS. Start by navigating to the EC2 dashboard and selecting “Launch Instance.” Choose an appropriate Amazon Machine Image, such as Ubuntu or Amazon Linux. Next, select the instance type based on required CPU, memory, and storage. After that, set up a key pair for secure access. A key pair includes a private key you download and keep safe and a public key stored by AWS. This enables secure SSH access to your instance. Then, configure the network settings, including the VPC, subnet, and security groups. Security groups act as firewalls controlling inbound and outbound traffic. Ensure you allow only the ports necessary for your application, such as port 22 for SSH and 80 or 443 for web access if needed. After completing these steps, review the configuration and launch the instance. Once launched, you can connect securely using your key pair and begin configuring your server environment.                                                    

Launching an EC2 instance is important when you need a reliable and scalable environment to run applications in the cloud. Instead of using physical servers, EC2 provides virtual machines that can be created and managed easily. One reason for launching an EC2 instance is flexibility, as you can select different instance types depending on your CPU, memory, and storage needs. It also allows you to scale resources up or down based on demand. Another reason is cost efficiency, since you only pay for what you use, making it suitable for both small and large projects. EC2 also integrates well with other AWS services, which helps in building complete and efficient systems. Security is improved through the use of key pairs and security groups that control access and traffic. Additionally, EC2 enables quick deployment and testing of applications. Overall, it provides a simple, secure, and scalable way to host and manage applications without maintaining physical hardware.                       

![Image](http://learn.nextwork.org/warm_vermilion_kind_finger_lime/uploads/aws-devops-vscode_7852fbf3)

### I also enabled SSH

SSH, which stands for Secure Shell, is a network protocol used to securely connect to and manage remote computers over an unsecured network. It allows users to access a server, such as an EC2 instance, from their local machine through a command-line interface. SSH uses encryption to protect the data being transmitted, ensuring that sensitive information like login credentials and commands cannot be intercepted by attackers. When connecting via SSH, authentication is typically done using a key pair, where the private key on your computer matches the public key on the server. This makes it more secure than traditional password-based login methods. SSH is commonly used for tasks such as configuring servers, deploying applications, and managing files remotely. It also supports secure file transfers using protocols like SCP and SFTP. Overall, SSH provides a safe, reliable, and efficient way to control and interact with remote systems over a network.                                          

### Key pairs

A key pair is a set of two cryptographic keys used to securely access an EC2 instance. It consists of a public key and a private key that work together for authentication. The public key is stored on the AWS server when you create or launch the instance, while the private key is downloaded and kept securely on your local computer. When you try to connect to the instance using SSH, AWS verifies that the private key matches the public key on the server before granting access. This method is more secure than using passwords because the private key is not transmitted over the network. Key pairs help prevent unauthorized access and protect your instance from attacks. It is important to store the private key safely, as losing it means you may not be able to access your instance. Overall, a key pair provides a secure and efficient way to authenticate and manage access to cloud resources.                                                                                                           

### Downloaded key pair file

The file that was downloaded to my local computer was my key pair, specifically the private key file. When creating the key pair during the EC2 instance setup, AWS automatically generates both a public and a private key. The public key is stored on the EC2 instance, while the private key is provided to me as a downloadable file, usually with a .pem extension. This private key is essential for securely connecting to the instance using SSH. It acts as a form of identification that proves I am authorized to access the server. Without this file, I would not be able to log into the instance. It is important to keep the private key safe and not share it with others, as anyone with access to it can connect to the instance. Overall, the downloaded file was my private key, which is a critical part of securely managing and accessing my EC2 environment.                                                                                                                                                  

---

## Set up VS Code

### What I did in this step

In this step,I am preparing my local development environment so I can connect to and manage my EC2 instance efficiently. First, I will download and install Visual Studio Code on my computer, which will serve as my primary code editor and workspace. VS Code is useful because it provides built-in tools and extensions that make development and remote access easier. Next, I will set up the terminal inside VS Code. This terminal allows me to run commands directly within the editor, making it convenient to communicate with my EC2 instance using SSH without switching applications.Finally, I will update the permission settings of my key pair file. This is important because SSH requires strict security permissions on the private key before it can be used.By restricting access to the key file, I ensure that only my system can use it to authenticate.Lastly, this step is about setting up the necessary tools and security configurations needed to securely connect to and interact with my EC2 instance

### What is VS Code?

Visual Studio Code, commonly known as VS Code, is a lightweight and powerful source code editor developed by Microsoft. It is used to write, edit, and manage code in various programming languages such as Python, JavaScript, and C++. One of its main strengths is flexibility, as it supports many extensions that allow users to customize their environment. VS Code includes an integrated terminal, enabling users to run commands and interact with systems like remote servers without leaving the editor. It also provides features such as syntax highlighting, code completion, debugging tools, and version control integration with Git. These features help developers work faster and stay organized. Additionally, VS Code is user friendly, fast, and works on multiple operating systems. Overall, it is a reliable and widely used tool that helps both beginners and experienced developers build, test, and manage software projects efficiently.                                                                

I will use Visual Studio Code to write, edit, and manage my code efficiently while working on my project. It will serve as my main development environment where I can create and modify files such as Python scripts and configuration files. I will also use its integrated terminal to run commands, connect to my EC2 instance using SSH, and execute programs without leaving the editor. Additionally, VS Code will help me debug my code, identify errors, and improve performance through its built-in tools. I can install extensions to support different programming languages and enhance my workflow. It will also allow me to manage version control using Git, making it easier to track changes in my project. Overall, I will use VS Code as a central tool to develop, test, and manage my application in an organized and efficient way.                                                                                                                                                                             

![Image](http://learn.nextwork.org/warm_vermilion_kind_finger_lime/uploads/aws-devops-vscode_53d05e68)

---

## My first terminal commands

The first command I ran in my terminal was cd ~\Desktop\DevOps. This command is used to change the current working directory to the DevOps folder located on my Desktop. The “cd” stands for change directory, and it allows me to navigate through different folders in my computer using the command line. The path ~\Desktop\DevOps specifies the exact location of the folder I want to access, making it easier to organize and work on my project files. By running this command, I ensured that I was inside the correct directory before executing any other commands related to my project. This is important because many commands depend on the current working directory to locate files and perform tasks correctly. Overall, this command helped me position myself in the right workspace so I could continue setting up, managing, and running my DevOps project efficiently without confusion or errors.                                                                                                               

### Updating file permissions

I changed my file’s permissions using a terminal command to ensure my key pair could be used securely for SSH access. Specifically, I used the command chmod 400 my-key.pem. The “chmod” command stands for change mode, and it is used to modify file permissions in systems like Linux or macOS. By setting the permission to 400, I made the file read-only for the owner and removed all permissions for other users. This is important because SSH requires that private key files are not publicly accessible, otherwise it will refuse to use them for security reasons. Before running the command, I made sure I was in the correct directory where the key file was located. After applying the permission change, the file became secure and ready for authentication. Overall, this step ensured that my private key was properly protected and met the required security standards for connecting to my EC2 instance.                                                                                                      

![Image](http://learn.nextwork.org/warm_vermilion_kind_finger_lime/uploads/aws-devops-vscode_9328ada1)

---

## SSH connection to EC2 instance

### What I did in this step

In this step, I am preparing to connect to my EC2 instance so I can begin interacting with it remotely. This involves using SSH to establish a secure connection between my local computer and the cloud server. First, I ensure that my key pair file is properly stored and has the correct permission settings, since it will be required for authentication. Next, I confirm that I have the correct public IP address or DNS name of the EC2 instance, which is needed to initiate the connection. I also make sure that the security group attached to the instance allows inbound traffic on port 22, which is used for SSH access. Then, I open my terminal, either in my system or within VS Code, and prepare the SSH command that includes my key file and the instance address. Overall, this step is about setting up all the required details and conditions so that I can successfully and securely connect to my EC2 instance.                                                                                          

### Connecting to EC2

You said
make it 156

Gemini said
To connect to an Amazon EC2 (Elastic Compute Cloud) instance, you most commonly use the Secure Shell (SSH) protocol for Linux or Remote Desktop Protocol (RDP) for Windows. This process requires a Key Pair, which consists of a public key stored on AWS and a private key file (usually .pem or .ppk) stored safely on your local machine.

When you initiate a connection, your terminal uses the private key to prove your identity to the instance’s Public IPv4 address. For a standard Linux instance, the command typically follows the format ssh -i "key.pem" ec2-user@instance-ip. Crucially, the instance’s Security Group—acting as a virtual firewall—must have an inbound rule specifically allowing traffic on Port 22 for SSH. Without this permission, the connection will time out, ensuring that only authorized users with the correct credentials and network access can reach the server.                                                                                     

### This command required an IPv4 address

You said
What does a server's IPV4 DNS mean?...pls give me 159 words

Gemini said
An IPv4 DNS (Internet Protocol version 4 Domain Name System) acts as the digital "phonebook" for the internet. While humans use memorable domain names like google.com, computers communicate using numerical IP addresses. An IPv4 address specifically follows a 32-bit format, typically expressed as four sets of numbers ranging from 0 to 255, separated by periods (e.g., 192.168.1.1).

When you enter a URL into a browser, the DNS server intercepts that request. It "resolves" or translates the alphabetical hostname into the corresponding IPv4 address. Without this service, you would have to memorize complex strings of numbers for every website you visit. Essentially, a server's IPv4 DNS settings tell the machine which database to consult to find the correct numerical destination for any web traffic. It is the bridge between human language and the binary-based routing infrastructure of the global web.           

![Image](http://learn.nextwork.org/warm_vermilion_kind_finger_lime/uploads/aws-devops-vscode_e3069dca)

---

## Maven & Java

### What I did in this step

Gemini said
To transform your EC2 instance into a functional web environment, you need a robust build tool and a reliable Java runtime. Apache Maven and Amazon Corretto 8 are the industry-standard duo for this task. Maven acts as your project’s architect; it automates the building, dependency management, and packaging of your Java applications. By using a pom.xml file, Maven ensures that every library your app needs is downloaded and configured correctly, saving you from manual setup headaches.

Complementing Maven is Amazon Corretto 8, a no-cost, multiplatform, production-ready distribution of the Open Java Development Kit (OpenJDK). Developed by AWS, Corretto 8 provides a stable environment optimized for high-performance cloud applications. It is particularly valued for its long-term support and security fixes. Together, these tools allow you to compile source code into executable JAR or WAR files, bridging the gap between raw code and a live, accessible web application.             

### Why I'm using Maven

Apache Maven is a tool that helps developers build and organize Java software projects. It's also a package manager, which means it automatically download any external pieces of code your project depends on to work.
At its core, Apache Maven is a powerful build automation and project management tool primarily used for Java applications. While it simplifies the process of compiling and packaging code, its true value lies in its declarative approach to software construction. Instead of writing complex scripts to describe how to build a project, developers use a standard XML file called the Project Object Model (POM) to describe what the project is. This pom.xml file serves as the single source of truth, containing configuration details, project dependencies, and plugin goals.                                                                                                                                                                                                                        

We use Apache Maven in this project to simplify and standardize the development process. Maven handles dependency management by automatically downloading required libraries from sources like Maven Central Repository, so we don’t need to manage JAR files manually.

It also provides a structured build lifecycle, allowing us to compile, test, and package the application using simple commands like mvn install. This ensures consistency across different environments.
Another critical advantage is plugin extensibility. Maven plugins enable integration with testing frameworks, code quality tools, packaging strategies, and deployment pipelines.

Additionally, Maven improves team collaboration because all configurations are stored in the pom.xml file. This makes the project easy to share, maintain, and integrate into CI/CD pipelines, ensuring reliable and repeatable builds.                                                                                                                            

### Why I'm using Java

Java is a high-level, object-oriented programming language designed to be portable, secure, and robust. It was developed by Sun Microsystems (now owned by Oracle Corporation) and released in 1995.
Java follows the principle of “write once, run anywhere” (WORA). This means that code written in Java can run on any system that has the Java Virtual Machine (JVM). Instead of compiling directly into machine code, Java programs are compiled into bytecode, which the JVM interprets.
It is widely used for building web applications, mobile apps (especially Android), desktop software, and enterprise systems. Java emphasizes object-oriented concepts such as classes, inheritance, encapsulation, and polymorphism, making code more modular and reusable.
Additionally, Java has strong memory management through automatic garbage collection, reducing common programming errors. Its large ecosystem,extensive libraries, and strong community support make it one of the most popular and reliable programming lang

We are using Java in this project because it provides a reliable, scalable, and well-structured foundation for building robust applications. Java’s object-oriented design allows us to organize code into reusable components, making the system easier to maintain and extend as the project grows.

Another key reason is platform independence. With the Java Virtual Machine (JVM), the application can run on different operating systems without modification, ensuring flexibility during development and deployment.

Java also has a rich ecosystem of libraries and frameworks, which speeds up development and reduces the need to build everything from scratch. Its strong memory management and built-in security features help minimize errors and vulnerabilities.

Additionally, Java integrates well with tools like build systems and cloud platforms, making it ideal for modern development workflows. Overall, it ensures consistency, performance, and long-term maintainability.                               

---

## Create the Application

### What I did in this step

In this step, you are transitioning from basic configuration to active engineering by harnessing the power of the Maven build engine. By executing terminal commands, you will learn to automate the creation of a professional Java web application using industry-standard blueprints known as archetypes. This process teaches you to move beyond manual folder creation, utilizing a standardized directory structure recognized by developers and servers worldwide. You will gain a fundamental understanding of the Project Object Model, or POM, which acts as the application's central brain to manage libraries and dependencies.

Furthermore, this step builds proficiency with the Command Line Interface, a critical skill for backend development. You will see firsthand how Maven handles the build lifecycle, from compiling source code to packaging your project into a Web Application Archive. By the end, you will have mastered scaffolding a scalable, organized project ready for enterprise-level logic.    

### Creating the Java web app

To create a Java web app using Maven, you invoke the Archetype plugin through your terminal. This command tells Maven to use a predefined template to automatically generate a standard project structure, including directories for your Java source code, resources, and web configuration files. A core part of this setup is the Project Object Model (POM.xml), which serves as the manifest for your application. It manages external libraries and build instructions, eliminating the need to manually download dependencies.

Once the structure is generated, you use the Maven lifecycle to compile your code and package it into a WAR (Web Application Archive) file. This file contains everything your server needs to run your application.                                                                                                                                                                                                                                                                             

### Installing Remote - SSH

I installed Remote - SSH to securely connect to a remote server and manage it directly from my local development environment. Using the Remote - SSH extension in Visual Studio Code allows me to open and work on files stored on a remote machine as if they were on my own computer. This is especially helpful when working with cloud services like an EC2 instance.

It makes development more efficient because I can edit code, run commands, and install dependencies without switching between different tools or interfaces. Instead of using a separate terminal for everything, I get a full development experience inside VS Code.

Another benefit is that the heavy processing happens on the remote server, not on my local machine, which improves performance. It also keeps my environment consistent across different devices. Overall, Remote - SSH simplifies remote development, making it more organized, faster, and easier to manage.                                                                        

### SSH configuration details

The configuration file contained the connection details required to access the remote server using SSH. Specifically, it defined a host alias, which is a short and easy name used instead of typing the full connection command every time. It also included the hostname, which is the public IP address or domain name of the remote server, along with the user that is allowed to log in, such as “ec2-user” or “ubuntu.”

Additionally, the file specified the path to the private key file used for authentication. This key ensures a secure connection without needing a password. In some cases, the port number is also included if it differs from the default SSH port.

When using Remote - SSH in Visual Studio Code, this configuration file allows the extension to quickly recognize and connect to the remote machine. Overall, it simplifies the connection process by storing all necessary details in one place, making remote access faster, consistent, and easier to manage.                                   

![Image](http://learn.nextwork.org/warm_vermilion_kind_finger_lime/uploads/aws-devops-vscode_2939cf01)

---

## Create the Application

### Exploring the project structure

In your project opened with Visual Studio Code, the src folder is the main directory that contains all the source code and essential resources for the application. Inside it, the main folder holds the actual production code that will be used when the application runs. Within src/main, the resources folder is used for configuration files and other supporting assets needed during execution, such as properties files or environment settings.

The webapp folder, also located inside src/main, is responsible for the web layer of the application. It contains all the frontend components like HTML, CSS, JavaScript, and JSP files. In your project, the index.jsp file indicates that Java Server Pages are used to generate dynamic content for users.

Additionally, the WEB-INF folder inside webapp contains important configuration files like web.xml. This folder is protected from direct browser access, ensuring better security and proper server-side configuration management.                            

From the file explorer in Visual Studio Code, you can see the structure of your project named nextwork-web-project, which is connected remotely through SSH. The explorer displays files and folders in a clear hierarchical layout, making it easy to navigate and manage your project.

At the top level, you can see the pom.xml file, which shows that the project uses Apache Maven for build and dependency management. Inside the src/main directory, there are two important folders: resources and webapp, representing backend resources and frontend web content.

Within the webapp folder, you can see WEB-INF and index.jsp. The WEB-INF contains the web.xml file, which is used for configuring the web application, while index.jsp serves as the main entry point for users accessing the application through a browser.                                                                                                                                                                                              

![Image](http://learn.nextwork.org/warm_vermilion_kind_finger_lime/uploads/aws-devops-vscode_45f91fd7)

---

## Using Remote - SSH

### What I did in this step

To set up this connection, you will primarily use the Remote - SSH extension in VS Code. This tool allows you to treat a remote Amazon EC2 instance as if it were a local development environment. By configuring your SSH credentials—specifically your private key file (.pem or .ppk)—you establish a secure tunnel that opens a dedicated VS Code window directly inside your Linux instance.

Once connected, you can explore your Java web app’s files using the standard VS Code sidebar. This eliminates the need for complex terminal commands like nano or vi to edit code. You can drag and drop files, use IntelliSense for Java, and modify your pom.xml or web.xml files with a modern graphical interface. This workflow is essential for cloud development, as it allows you to write code on your local machine while the actual application logic and Maven build processes run on the powerful EC2 hardware in the cloud.                                                                                            

### Updating the web app

index.jsp is a default entry page in Java-based web applications that use JavaServer Pages (JSP). It works similarly to index.html, but with the added ability to generate dynamic content using Java code embedded within HTML.
In projects built with frameworks like Apache Tomcat, index.jsp is often the first page users see when they access the root URL of the application. The server automatically looks for this file and renders it if no specific page is requested.
What makes index.jsp powerful is that it allows developers to mix HTML for structure and Java for logic. This means you can display dynamic data such as user information, database results, or application states directly on the page.
When a client requests index.jsp, the server converts it into a servlet, compiles it, and then executes it to produce an HTML response sent back to the browser.
Overall, index.jsp serves as a starting point for building interactive, server-driven web interfaces in Java web applications.             

I edited index.jsp by accessing the project files within the Java web application structure and modifying it directly using a code editor. Typically, this file is located inside the webapp or WebContent directory, depending on how the project is set up in tools like Apache Maven projects.
First, I opened the project in an editor such as Visual Studio Code or an IDE like IntelliJ IDEA. Then, I navigated to index.jsp and updated its content by adding or modifying HTML and JSP elements. This could include inserting Java expressions, updating page directives, or improving the layout.
After making changes, I saved the file and redeployed or refreshed the application on a server like Apache Tomcat. The server automatically recompiles the JSP into a servlet, so the updates reflect immediately when the page is reloaded in the browser.                                                                                                                                                                  

![Image](http://learn.nextwork.org/warm_vermilion_kind_finger_lime/uploads/aws-devops-vscode_7a1de541)

---

## Using nano

### Additional improvements

### Terminal vs IDE

### Verifying my work

---

---
