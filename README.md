# Splunk Setup Lab
This repository documents a hands-on Splunk Enterprise setup lab on Kali Linux / Debian-based Linux on a virtualbox. It demonstrates practical experience with installing Splunk, starting and stopping the service from the command line, accessing Splunk Web, and completing the initial administrator setup.
## Project goals
- Install Splunk Enterprise on a Linux system.
- Start, stop, restart, and verify the Splunk service from the CLI.
- Access Splunk Web locally and confirm the platform is working.
- Record the setup process in a clean, recruiter-friendly format on GitHub.

## Lab environment
Item                 ==> 	Details
Operating system     ==>	Kali Linux / Debian-based Linux
Platform	           ==>  Splunk Enterprise 
Default install path ==>	/opt/splunk for package-based Linux installs 
Web interface        ==>	http://localhost:8000 after startup 

## Installation notes
Splunk Enterprise on Linux can be installed using a DEB package, an RPM package, or a '.tgz' tar file, depending on the distribution and installation preference.
​On Debian-based systems such as Kali, a common package installation method is:

'sudo dpkg -i splunk_package_name.deb'

A tar-based installation can also be performed by extracting the package into '/opt'.

'sudo tar xvzf splunk_package_name.tgz -C /opt'

### First startup
To start Splunk Enterprise for the first time and accept the license from the command line, run:

'sudo /opt/splunk/bin/splunk start --accept-license'

During the initial startup flow, Splunk prompts for license acceptance and creation of administrator credentials.
​After startup completes, Splunk Web becomes available locally on port 8000.

#### Service management commands
Splunk documents the main Linux service controls through the splunk CLI in '$SPLUNK_HOME/bin'.

### Start Splunk

'sudo /opt/splunk/bin/splunk start'

* if it says use '--run-as-root' the we use
  
'sudo /opt/splunk/bin/splunk start --run-as-root'

### Stop Splunk

'sudo /opt/splunk/bin/splunk stop'

### Restart Splunk

'sudo /opt/splunk/bin/splunk restart' 

* if it asks for 'run-as-root' then we use this too.

#### Check status

'sudo /opt/splunk/bin/splunk status'

### Accessing Splunk Web
Open the local Splunk Web interface in a browser after the service starts:

'http://localhost:8000'

Sign in with the administrator 'username' and 'password' created during the first startup process.

## Basic admin setup
This lab covers the basic post-installation admin tasks below:

* Confirm Splunk starts successfully from the terminal.
* Verify the web interface loads on localhost:8000.
​* Log in with the newly created admin account.
* Open server controls in Splunk Web and review available management options.
