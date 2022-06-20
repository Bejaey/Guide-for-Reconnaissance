# Top 10 Hacker Tools and Techniques

By understanding how hackers gain access to systems, organizations can stay a step ahead and ensure information availability, integrity, and confidentiality. Listed below is Altius IT's list of the Top 10 Hacker Tools and Techniques:

1) Reconnaissance

Reconnaissance, also known as the preparatory phase, is where the hacker gathers information about a target before launching an attack and is completed in phases prior to exploiting system vulnerabilities. One of the first phases of Reconnaissance is dumpster diving. It is during this phase that the hacker finds valuable information such as old passwords, names of important employees (such as the head of the network department), and performs an active reconnaissance to know how the organization functions. As a next step, the hacker completes a process called footprinting to collect data on the security posture, reduces the focus area such as finding out specific IP addresses, identifies vulnerabilities within the target system, and finally draws a network map to know exactly how the network infrastructure works to break into it easily. Footprinting provides important information such as the domain name, TCP and UDP services, system names, and passwords. There are also other ways to do footprinting, including impersonating a website by mirroring it, using search engines to find information about the organization, and even using the information of current employees for impersonation. 

--------------------------------------------
# Top 10 Tools for Reconnaissance

1) Google

![Screenshotfrom2019-01-1814-52-15-5c521dcf46e0fb0001c0de50](https://user-images.githubusercontent.com/106522935/174527027-12642810-cf76-46c2-b7cb-f9aaf29b5119.png)


For every penetration tester, Google should be the first tool to use for continuous cyber recon. Google and other search engines like Bing are vital during reconnaissance because it provides vital data about individuals, companies, and data including leaked content. The obtained information is free and can help to determine the direction a penetration tester will take. 

For more details visit : https://www.google.com/

--------------------------------------------

2) Maltego CE

Maltego is a visual link analysis and data mining tool and it is the most famous software for performing Open Source Intelligence. It provides a library of plugins, called “transforms”, which are used to execute queries on open sources in order to gather information about a certain target and display them on a nice graph. In fact, differently from the command line tools seen until now, Maltego has a Graphical User Interface through which the user performs his research and analyzes results returned on the graph.

It is developed by Paterva which distributes three different versions: Maltego XL, Classic and CE. We are interested in Maltego CE which stands for Community Edition: this is the non commercial version and it is available for everyone after a quick registration.

Installation

Before proceeding with the installation it is a good idea to register at this link: https://www.paterva.com/web7/community/community.php. In fact, in order to use the software it is mandatory to have a Maltego account which is required at the startup of the application.

If you are using Kali Linux, Maltego CE is already installed. Moreover you will find that Kali has its own custom version called Maltego Chlorine, which has been made on purpose for this distro.
Otherwise you can download the package from https://www.paterva.com/web7/downloads.php#tab-3 and install it on your operating system (the software is available for Windows, Linux or Mac OSX).

# Installation

In Kali Linux, Maltego can be started by navigating in the applications menu by clicking on Applications > Information Gathering > maltegoce like shown in the following image:

![maltego_start](https://user-images.githubusercontent.com/106522935/174518274-3dccd0c4-df61-4379-8b67-e261512472a8.png)

Same thing can be done by clicking on the “Show application” menu:

![maltego_start2](https://user-images.githubusercontent.com/106522935/174518568-b5ffe9e3-bafa-43a7-a23e-eab9a882cc9e.png)

Maltego can also be started by opening the Terminal and typing maltegoce, but since it is not a command line tool, this is not the best choice.

At the start up, after all the modules are correctly loaded, we get prompted with the Startup Wizard which asks for Maltego account credentials:

![maltego_account](https://user-images.githubusercontent.com/106522935/174518641-b091eb7d-a44f-46bd-a8b7-9625b0f13104.png)


If you have inserted them and correctly solved the captcha, you will get a welcome message and the information about the validity of the API key. At the next prompt just leave “Install Transforms from Maltego public servers” which will install the transforms on the client.
At the final screen we get the correct initialization message with different possibilities for starting to use Maltego:

![maltego_ready](https://user-images.githubusercontent.com/106522935/174518705-a1051939-9f41-48cf-ab17-cd492173d4b8.png)

“Run a machine” allows you to run predefined searches, called “machines”: for example, the “Company Stalker” machine gets all email addresses it can find on the web for a certain domain and look for related account on social networks; it also gets documents and extract metadata from them.
Since we want to perform a custom search we need to select “Open a blank graph and let me play around” and then click on “Finish”. This action opens a new empty graph where we can start a new OSINT activity:

![maltego_new](https://user-images.githubusercontent.com/106522935/174518833-8cae6eb6-ca05-4914-b7b3-e010caff4154.png)

We could have also opened a new graph by simply clicking on Maltego icon on the top left choosing “New”.
As the image shows, on the top part we have six tabs:

•Investigate - offers options to quickly search through the graph or to select entities;
•Manage - allows to import/export configurations, manage entities and transforms;
•View - allows to choose which panels are active;
•Organize - sets the node layout mode and the alignment type;
•Machines - allows to run, stop, create and manage machines;
•Collaboration - offers options to share projects and results.

There is a big central window which is where the graph will be developed and on the tab it is reported the name of the graph (you can save the project and give it a proper name).
On the left side we have the “Palette” panel which contains the following categories:

•Devices - adds a node such as a phone or camera;
•Infrastructure - adds a node such as a domain, MX record or Website;
•Locations - adds a node such as a GPS coordinate or location name;
•Malware - adds a node as hash entity;
•Penetration Testing - adds a node which identifies a technology;
•Personal - adds a node such as a document, email address or person name;
•Social Network - adds a node related to social networks like Facebook or Twitter.
Each of them contains objects related to that category: these items can be dragged on the graph and, once placed there, it is possible to use them as starting point for a search activity. This can be done thanks to the application of transforms.

As done in the previous Information Gathering posts, we can use as target the National Institute of Standards and Technology (NIST). We can start by clicking on “Infrastructure” and dragging on the graph a “Domain” object; by double clicking on it we can change its name into “nist.gov”:

![maltego_nist (1)](https://user-images.githubusercontent.com/106522935/174519199-a30a3f62-43d8-4921-8d51-d739405308d4.png)

Now informations are displayed also in the other four panels:

•Run View - contains Transforms and Machines that it is possible to run against the selected object;
•Overview - shows a schematic graph where nodes are represented by colored circles;
•Detail View - displays informations about the selected object;
•Property View - shows properties regarding the selected object.

To run a transform on the object we can either access them through the “Run View” panel or by simply clicking on the object with the right mouse button. “All Transforms” contains all the possible transforms we can apply to that object type, which in this case is a Domain object.
The same transforms can also be found by looking inside the following four groups (of course they vary depending on the object type):

•DNS from Domain;
•Domain owner detail;
•Email addresses from Domain;
•Files and Documents from Domain.

![maltego_transforms](https://user-images.githubusercontent.com/106522935/174519337-00a7637e-243e-4132-9403-9973982b0bd0.png)

We can start by running the transform DNS from Domain > DomainToDNSNameSchema which tries various name schema’s against the object domain; once the disclaimer is accepted, we can run the transform:

![maltego_DomainToDNSNameSchema](https://user-images.githubusercontent.com/106522935/174519646-af973017-7644-4c52-bc77-5a5259f93523.png)

The execution of the transform can be verified in the “Output - Transform Output” panel: as reported, the tool searches for subdomains using lists of common names which are loaded on Paterva servers as files with extension “.bfdns”.
We can see that the graph is populated with subdomains found by the search; it is possible to switch from the Main View to the Bubble View or to the Entity List by simply clicking on the respective buttons on the top of the graph.
There is also the chance to change the layout mode by clicking on the icons on the upper part of the graph window; the default one is called “Block”.
Note that entities belonging to the same category are represented by circles of the same color in the Overview panel.

Suppose we want to find the IP address for a certain subdomain, then we right click on the object and run Resolve to IP; we can even select multiple objects using the “Shift” button and apply the transform to all of them:

![maltego_ResolveToIP](https://user-images.githubusercontent.com/106522935/174519711-485669da-ca4b-456d-8506-a5360c20f38a.png)


Once we have the IP addresses we can run a further transform that returns the geolocation for that IP; just right click on the object, then IP owner detail > toLocation and run it by clicking on the yellow arrow:

![maltego_ToLocation](https://user-images.githubusercontent.com/106522935/174519761-247ca855-b13e-4860-b7db-75a7184d8d7c.png)

The transform group “IP owner detail” is also really useful to find informations like email addresses, entities (person names) and phone numbers, so it is a good idea to take a look at the others transforms inside it.

Now suppose we want to check, in a passive way, which websites are associated to the target domain: DNS from Domain > To Website DNS [using Search Engines] is the transform we want to use. We can also choose which search engine we want to launch the query against (default is Bing); this can be done by clicking on the “Configure” icon near the yellow arrow key:
![maltego_configure](https://user-images.githubusercontent.com/106522935/174519825-a6b2b22c-212f-4a93-81ba-c835e73f61b7.png)

In this configuration menu there are also reported all the other transforms loaded in Maltego with their Status, Transform Server Location, Default Set, Input and Output informations.
Keep in mind that some transforms are more invasive than others: for example, it is possible to discover websites querying directly port 80 using the transform To Web site [Query port 80].

This is the resulting graph with a focus on the websites:

![maltego_ToWebsite](https://user-images.githubusercontent.com/106522935/174519996-99600215-578e-4dde-bca7-5386de84a704.png)


Note how Maltego automatically organizes nodes on the graph.

A really useful transform which can be applied to Website objects is ToServerTechnologiesWebsite; using the BuiltWith.com API it is able to retrieve informations about the technologies running on the target website:

![maltego_ToServerTechnologiesWebsite](https://user-images.githubusercontent.com/106522935/174520037-f547586a-c2f8-40d9-91e4-f4bf086b9c68.png)

If you think the graph is becoming heavy, it is possible to remove unwanted nodes by selecting them and pressing the “Canc” button.
Another interesting transform is the one named Files and Documents from Domain: this will search for files and documents inside the given domain with the extensions reported in the configuration menu; by clicking on the node representing a file we can get informations about the query used to find it with the document download link.

![maltego_ToFiles](https://user-images.githubusercontent.com/106522935/174520095-dcff9822-c07d-42c6-91b4-992ad11f9a9e.png)

The following step could be to find email addresses related to the target domain by using Email addresses from Domain transform on the “Domain” object; then we could run To Person transform on the “Email” object to get person identity related to that email address or To Phone number [using Search Engine] transform to try a phone number discovery.

Like seen before, another way to proceed is to use predefined search machines which are configured to run with a more or less invasive approach against the target; be aware that you can create your own machine so as to exactly perform the queries you need and nothing more.

You can even create your own transforms: http://dev.paterva.com/developer/getting_started/building_your_own_tds_transform.php.

# Conclusions

Maltego is a powerful graphical tool for OSINT and it can be customized depending on your own needs. Since it generates graphs it gives a rapid overview of the target structure, differently from command line tools. This is why it is always important to work with more than one tool so as to have a better picture of the target.
As always, experiment with the transforms by yourself (there is a very good amount of them) to make the most of Maltego potential.

--------------------------------------------

3)Recon-ng

![rekon_ng_bg_cyber](https://user-images.githubusercontent.com/106522935/174526568-a026c582-4a05-4d4f-8a55-6c0e60d1c74d.jpg)

Recon-ng is a full-featured Web Reconnaissance framework written in Python. Complete with independent modules, database interaction, built in convenience functions, interactive help, and command completion, Recon-ng provides a powerful environment in which open source web-based reconnaissance can be conducted quickly and thoroughly.

Recon-ng has a look and feel similar to the Metasploit Framework, reducing the learning curve for leveraging the framework. However, it is quite different. Recon-ng is not intended to compete with existing frameworks, as it is designed exclusively for web-based open source reconnaissance. If you want to exploit, use the Metasploit Framework. If you want to Social Engineer, use the Social Engineer Toolkit. If you want to conduct reconnaissance, use Recon-ng.
 
# Installation

Recon-ng is pre-installed in Kali Linux. But if you want to use it in another Linux distribution, the installation process is quite easy.

👉 Commands

$ sudo apt-get update && sudo apt-get upgrade

$ sudo apt-get install git

$ sudo apt-get install python-pip python-dev build-essential

$ sudo pip install --upgrade pip

$ sudo pip install --upgrade virtualenv

Next, clone Recon-ng from Github.

$ sudo git clone https://github.com/lanmaster53/recon-ng.git

$ cd recon-ng

$ sudo pip install –r REQUIREMENTS

At this point the installation is complete and the application can be started from the current recon-ng directory.

$ ./recon-ng

NOTE: If you are using Kali Linux you can start the application manually by typing recon-ng in your terminal or from the Information Gathering module which is present on the Applications tab.

--------------------------------------------

4) Shodan

![shodan-frontpage](https://user-images.githubusercontent.com/106522935/174528233-ae8a0852-065f-43fe-860b-af2717705111.png)


Shodan is among the first search engines for internet-connected devices. With servers located all over the world, it provides real-time intelligence regarding attest technological trends. It also has APIs that other recon tools like Nmap, Metasploit, Maltego, and FOCA use for analysis.

For more details visit : https://www.shodan.io/

--------------------------------------------

5) Censys

![introducing-search2](https://user-images.githubusercontent.com/106522935/174530506-ec3a10ae-a76f-4a6f-9334-19b4d72abfa2.gif)


Censys provides an avenue to gather data regarding all your assets to help you prevent target attacks. This tool provides actionable insights and helps you track changes in all your assets and identify potential vulnerabilities. 
Visit this sites 👉https://gbhackers.com/shoda-censys-internet/ to acess the user guides.

--------------------------------------------

6) Nmap

 ![Uploading nmap-thumbnail.jpg…]()
 
 Nmap is an open-source network mapping tool developed by Gordon Lyon. It is widely used as a port scanner and a host discovery tool by network administrators and hackers world-wide.

The reason for its popularity is that it allows users to perform powerful scans using a combination of a small set of options. Using only these options, you can run effective and powerful scans by running specifically crafted commands.

But even if you are not familiar with Nmap, you can still use it by executing simple commands. These will allow you to get a few good scan results. However, if you want your scans to be more accurate, then you need to learn more about Nmap and how to use it correctly.

This is precisely what this post aims to do. In it, I tried to share with you the different ways to use Nmap.

To fully understand the content of this post, you need to have a basic understanding of computer networks. You don’t need to be an expert, but you should at least understand the basic concepts like IP addresses, subnets, and TCP.

With that being said, let’s go ahead and start.

# Installation

$ sudo apt-get install nmap

or

$ sudo apt install nmap

$ git clone https://github.com/nmap/nmap.git

$ ./configure

$ make

$ make install

# What you’ll need

Nmap is a command-line tool that works best on Linux. If you are a Linux user, then you can easily download Nmap using your distribution’s package manager (dpkg, rpm, pacman…). It should be available in all Linux repositories, so you won’t have a hard time installing it.

If you have a pen-testing Linux distribution like Kali or Parrot, then Nmap should already be installed with your OS.

For non-Linux users, you can download Nmap here, although I recommend that you switch to Linux if you want to take advantage of all the Linux-based hacking tools.

During this post, we will be performing some of our tests on scanme.nmap.org. This is a test machine maintained by Nmap to help users learn and test their commands legally. You should make sure to not overwhelm this address with scans and only use it a few times a day. Alternatively, you can perform scans on your local network, provided, of course, that you have the proper rights to do so.

# The most basic commands

I think that we’ve had enough talk now, it is about time to perform our first scan.

Here is the syntax for all Nmap commands :

nmap [options] target

The target can be a domain name, an IP address, a range of IP addresses, or a combination of all these elements.

If you don’t specify options, then Nmap will perform a default port scan of the target.

![nmap1](https://user-images.githubusercontent.com/106522935/174541602-7d7a1fb5-1480-4a9b-83c7-7b6b34ef26c3.png)

Nmap Default Scan
As you can see, we have obtained some interesting information from the target host by using this simple command:

•Nmap does a DNS resolution and provides the IP address of the target.

•We know that the host is up.

•We have a list of all open ports and their corresponding service.

Not bad for a default scan, don’t you think?

# Host discovery

If you want to test for open ports in your local network, scanning the entire IP address range might take a lot of time. In this case, you should start first with a host discovery phase in which you detect the available machines.

For instance, if you had to scan the network associated with the IP address 192.168.1.1/24, and only three machines are available, then it wouldn’t make sense to test for open ports in every IP address in that range.

This is where host discovery can be useful. It helps you focus your scanning efforts and, instead of 255 addresses, you will only scan the three addresses belonging to the available machines.

To perform host discovery, simply add the -sn option.

In the following test, I used Nmap to scan for available hosts in my local network.

By providing 192.168.1.0-255 as the target, Nmap will scan all addresses ranging from 192.168.1.0 to 192.168.1.255.

![nmap-host-discovery](https://user-images.githubusercontent.com/106522935/174541926-a5715b53-407b-4865-b705-13c8301e335c.png)

Nmap – Host Discovery
As shown in this output, Nmap detected 5 hosts that are connected to my network.

This type of scan is also called a ping sweep.

# Port Scanning

When it comes to port scanning, Nmap offers numerous techniques that you can use.

The reason for this is that firewall rules in the target host can sometimes deny certain types of packets used in port scanning. As a result, in some cases, only one technique will be effective in detecting open ports, while all others will fail.

It is, therefore, important to have various types of scanning techniques that you can choose from and apply depending on the case.

By default, Nmap scan for the first 1000 ports. If you want to specify the exact ports to test, you can use the option -p followed by a number (or a group of numbers separated by a comma, or even a range of ports separated by a hyphen).

![nmap-ports-specification](https://user-images.githubusercontent.com/106522935/174542180-d3f38dcf-d5e0-4f01-83cd-d5b92d539461.png)

Nmap Port Specification

In this example, by using the -p option, the command limits the scan to ports 21, 22, 23, 53, 80, and 443.

Please note that you would need to have privileged access to perform most of the following scans. If you are on Linux, you would need to run these commands as root, and if you are on Windows, make sure that you run Nmap as an administrator.

# TCP SYN Scan

This is the default scan type when you don’t provide an option. It consists of sending a SYN packet to the target machine and waiting for a response. If the target machine sends back a SYN/ACK packet, then the port is open.

The testing host does not complete the three-way handshake. Once it receives the reply from the target host, it closes the connection before it is established. By doing so, the target machine will have a lower chance of detecting the scan. This is why this scanning technique is also known as Stealth Scan.

To perform a TCP SYN Scan, you can use the option -sS
![nmap-syn-scan](https://user-images.githubusercontent.com/106522935/174542361-8d035ae7-c49c-4fc9-b2a8-f1e5b7f21d6a.png)

TCP SYN Scan
As you can tell from the dash sign (#) in this command prompt, I switched to a superuser before running the command.

Notice that some ports are shown to be filtered. What this means is that there is a filtering software or device (Like a firewall) that is blocking packets from reaching those ports.

# TCP Connect Scan
The TCP Connect scan consists of asking the operating system to establish a connection to the specified remote port through a connect system call.

This technique does not require privileged access as opposed to other scanning techniques, and so, it can be useful when the user doesn’t have root access on the testing machine.

To perform a TCP Connect Scan, you can simply use the -sT option.
![nmap-tcp-connect-scan](https://user-images.githubusercontent.com/106522935/174542495-4eb3b2d7-8fd6-4fb6-9033-652e068c1aef.png)
TCP Connect Scan

# UDP Scan

As its name implies, this scanning technique uses UDP protocol instead of TCP.

Since UDP does not use a three-way handshake, a sent packet to an open port will not be acknowledged. However, when you send a UDP packet to a closed port, the target host will send back an ICMP port unreachable packet. Using this technique, Nmap can determine if a port is open or not.

To perform a UDP scan, you can use the -sU option.

![nmap-udp-scan (1)](https://user-images.githubusercontent.com/106522935/174543833-b130ad11-e9e9-41f1-92dc-6ae915cf57a0.png)
UDP Scan

# TCP Flag Scan
In most systems, if you send a packet without a SYN, ACK, or RST flag, the target host will not respond if the port is open. However, if the port is closed, then it sends back an RST packet.

You can determine which ports are open by sending packets not containing these three flags, but instead containing a combination of the other flags(FIN, URG, and PSH) or no flag at all (NULL).

To perform this scanning technique, Nmap offers three options :

-sN : NULL (All flag bits are equal to 0)
![nmap-null-scan (1)](https://user-images.githubusercontent.com/106522935/174543968-07bab2c3-561d-4051-92a2-eaa0e0f99c0b.png)
TCP Null Scan

-sF : FIN (Only the FIN bit is set to 1)

![nmap-fin-scan (1)](https://user-images.githubusercontent.com/106522935/174544074-607fa3c5-a1cb-48b7-bbbb-a7cbbe3dae50.png)
TCP FIN Scan

-sX : Xmas (URG, PSH and FIN bits are all set to 1)
![nmap-xmas-scan (1)](https://user-images.githubusercontent.com/106522935/174544176-349c7821-508a-4f6e-abcf-1beb00867d93.png)
TCP Xmas Scan

# OS Identification

Nmap can also identify the OS of the target machine by comparing its responses to a database of OS fingerprints.

To activate this functionality, you can use the -O option.
![nmap-os-detection](https://user-images.githubusercontent.com/106522935/174544805-d00171b7-bb95-49b9-b515-a5b224a10f18.png)
OS Detection

One other useful feature is version detection, which you can enable using the -sV option.
![nmap-version-detection](https://user-images.githubusercontent.com/106522935/174544911-36b20e20-4829-4846-9e33-77ccad418e74.png)
Version Detection

# Output

By default, Nmap displays the results of the scan in the standard output (stdout). But you can also specify other types of output.

If you add the option -oN followed by a file name, then the output will be saved to the given file name.
![nmap-output-file-768x393](https://user-images.githubusercontent.com/106522935/174545126-3534b755-d03b-4223-8a14-2f1ed0ab38a8.png)
Normal output to a file

The above command generates the following file:
![nmap-resulted-normal-file](https://user-images.githubusercontent.com/106522935/174545446-80ddf3e1-9888-4eea-8e1d-deb72a88fed4.png)
Resulted file

Although this is a good format for humans to read, it isn’t as easily understandable by scripts if you ever decide to send the output to another tool.

For this reason, Nmap also supports XML, which can be easily parsed by another program.

If you want to retrieve an XML file as an output, you can use the option -oX.
![nmap-xml-output (1)](https://user-images.githubusercontent.com/106522935/174545647-ffca05e7-ba84-45f7-bf2e-6769de522b09.png)
Output to an XML file

And here is the generated XML file:
![nmap-resulted-xml-file (1)](https://user-images.githubusercontent.com/106522935/174545757-c1778f4a-dab6-406b-84f8-f364e1d95fb9.png)
Generated XML file

You should now have a basic understanding of Nmap and how you can use it. You can perform your own scans and experiment by combining the options that you’ve learned here.

Of course, Nmap supports other options that we didn’t cover in this post. In fact, we’ve only scratched the surface here.

For further reading, you can refer to the official Nmap reference guide, and if you ever need help while typing a command, just type in the following command: nmap – -help.

--------------------------------------------

7) Spiderfoot

![spiderfoot](https://user-images.githubusercontent.com/106522935/174564081-a45675d1-3b9f-4c08-928a-dad7bb01370d.png)


This package contains an open source intelligence (OSINT) automation tool. Its goal is to automate the process of gathering intelligence about a given target, which may be an IP address, domain name, hostname, network subnet, ASN, e-mail address, person’s name, phone number, username.

SpiderFoot can be used offensively, i.e. as part of a black-box penetration test to gather information about the target, or defensively to identify what information you or your organisation are freely providing for attackers to use against you.

Now let's explore how to install Spiderfoot.

# Installation 

Install python3-pip:

$ sudo apt-get install python3-pip

Clone the project from its Github repository using git clone :

$ git clone https://github.com/smicallef/spiderfoot.git

Enter the project folder:

$ cd spiderfoot

Install the required libraries:

$ sudo pip3 install -r requirements.txt

Finally run the project using:

$ sudo python3 sf.py -l 127.0.0.1:

Voila! Now you can use it freely to perform your OSINT operation.

There is another option which is using a ready-to-go Spiderfoot instance. To do it check this link: https://www.spiderfoot.net/hx/

To start a new scan, click on " + Create a new scan"

![image5](https://user-images.githubusercontent.com/106522935/174563931-f5a4244b-5cab-4ce1-9f32-42232d996c40.png)

Enter your target and click on " Run scan now"

![image9](https://user-images.githubusercontent.com/106522935/174564243-d0f34826-bf97-48df-81b4-03cc5a231bec.png)

specific task. Spiderfoot comes with a long list of modules including:

•abuse.ch: Checks if a host/domain, IP or netblock is malicious according to abuse.ch.

•Accounts: Looks for possible associated accounts on nearly 200 websites like Ebay, Slashdot, reddit, etc.

•AlienVault OTX: Obtains information from AlienVault Open Threat Exchange (OTX)

The full list of modules can be found here: https://github.com/smicallef/spiderfoot

The tool gives you the ability to investigate data too:

![Screenshot_2020-03-01-SpiderFoot-HX1-1024x731](https://user-images.githubusercontent.com/106522935/174564785-1af62e4e-f6e1-4003-983b-2b7c85184cf6.png)

# Summary

In this module, we explored Open source intelligence and how to perform it using a powerful tool called "SpiderFoot"

--------------------------------------------

8) DataSploit

![Datasploit](https://user-images.githubusercontent.com/106522935/174572614-55d8e05a-cf34-4642-a37a-8a894e23cae5.png)


DataSploit is an OSINT Framework which allows you to perform various recon techniques (on phone numbers, bitcoin addresses, people, companies, etc.), to aggregate all the raw data, and give data in multiple formats. If you are pentester, cybersecurity researcher or bug hunter, you’ll find DataSploit very useful OSINT framework. It brings all useful and effective OSINT tools and techniques in one place, correlates the raw data captured and gives you all the relevant information about the target’s domain/email/IP, etc.It is a simple way to dump data for a domain or other piece of metadata.


# Features:

•Performs automated OSINT on a domain / email / username / IP and find out relevant information from different sources.

•Easy to contribute OSINT Framework.

•Code for Banner, Main and Output function. Datasploit automagically do rest of the things for you.

•Useful for Pen-testers, Bug Bounty Hunters, Cyber Investigators, Product companies, Security Engineers, etc.

•Collaborate the results, show them in a consolidated manner.

•Tries to find out credentials, api-keys, tokens, subdomains, domain history, legacy portals, usernames, dumped accounts, etc. related to the target.

•Can be used as library, automated scripts or standalone scripts.

•Can generate lists which can be feeded to active scan tools.

•Generates HTML, along with text files.


# Installation


$ git clone https://github.com/datasploit/datasploit 

$ cd datasploit

Then install all python libraries (requirements.txt) via pip:

$ pip install -r requirements.txt

Kali Linux users: install the requirements using the following command:

 $ pip install --upgrade --force-reinstall -r requirements.txt 

Install DataSploit using pip (this command will install all the dependencies:

$ pip install datasploit

$ python datasploit.py

-------------------------------------------

9) Aquatone

![AQUATONE](https://user-images.githubusercontent.com/106522935/174574501-c7b55c2c-88e8-4812-8f2f-b0c17a76ee3f.png)


Aquatone is a set of tools for performing reconnaissance on domain names. It can discover subdomains on a given domain by using open sources as well as the more common subdomain dictionary brute force approach. After subdomain discovery, Aquatone can then scan the hosts for common web ports and HTTP headers, HTML bodies and screenshots can be gathered and consolidated into a report for easy analysis of the attack surface.

# Instructions to Install Aquatone on Kali Linux

▶ Requirement : Google Chrome or Chromium Browser (Chromium is recommended)

▶ Download the latest release of Aquatone : https://github.com/michenriksen/aquatone/releases/

▶ Run : unzip aquatone_filename.zip (example : unzip aquatone_linux_amd64_1.7.0.zip)

▶ Run : mv aquatone /usr/bin/

▶ Run (Check) : aquatone -version

▶ Run (Check/Usage) : cat list.txt | aquatone [list.txt contains the list of domains]

▶ View : Open file manage, point to the html report of aquatone and open it with any browser.

▶ More Info : https://github.com/michenriksen/aquatone


-------------------------------------------

