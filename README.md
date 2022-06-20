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
