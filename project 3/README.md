# Vagrant Installation
## 1 .step one
To start using Vagrant, you first need to install it on your machine.

Visit the Vagrant Downloads Page:

Click on the following link to access the official Vagrant download page: Vagrant Downloads.

Choose the appropriate version for your operating system (Windows, macOS, or Linux) and follow the installation instructions provided.
![alt text](<vagrant site download.png>)


## 2. Verify the Installation
After installation, it’s important to confirm that Vagrant was installed correctly.

Open Command Prompt or Terminal:

On Windows, search for “Command Prompt” in the Start menu and open it.
On macOS/Linux, open the Terminal application.
Check Vagrant Installation:

In your command prompt or terminal, type the following command and press Enter:
$ vagrant
Expected Output: You should see a list of Vagrant commands and options as shown in the image below . If you see an error saying "Vagrant not found," try logging out and back in (especially on Windows) to refresh your system’s environment variables.
![alt text](<vagrant version.png>)
![alt text](<vagrant installed.png>)



## 3. Create a Directory for Your Project
Create a New Directory:

Use the following command to create a new directory named vagrant_getting_started and check if its there : bash $ mkdir vagrant_getting_started
![alt text](<mkdir vagrant.png>)
Navigate into Your New Directory:

Change into your newly created directory with:
$ cd vagrant_getting_started
![alt text](<cd vagrant.png>)

## Now that you're in your project directory, you need to initialize Vagrant.

Run the Initialization Command:

Use the following command to initialize your Vagrant project:
$ vagrant init
![alt text](<vagrant init.png>)
What This Does: This command creates a Vagrantfile, which is a configuration file that defines your virtual machine settings.

4. Initialize the Vagrant Project

Take a moment to open the Vagrantfile in a text editor to explore its structure.

## 5. Configure Your Vagrantfile
To set up your virtual machine, you need to specify which base box to use in your Vagrantfile.

Open the Vagrantfile:

Use any text editor (like Notepad, VSCode, or Atom) to open the Vagrantfile.
Modify the Vagrantfile:

Replace the existing contents with the following code:

Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/bionic64"
end
Explanation: The line config.vm.box = "hashicorp/bionic64" tells Vagrant to use the hashicorp/bionic64 box as the base for your virtual machine. If this box isn’t already downloaded, Vagrant will automatically fetch it when you start the VM.
![alt text](<proof of vagrant file.png>)


## 6. Start Your Virtual Machine
Before starting your virtual machine make sure your oracle virtual box is running in your machine

With your Vagrantfile configured, you can now start your virtual machine.

Run the Command:

Type the following command in your terminal:

$ vagrant up
![alt text](<vagrant up.png>)
What This Command Does: This command will download the specified base box (if it’s not already on your machine) and create a new virtual machine instance based on your configuration. This process usually takes less than a minute.


Accessing Your Virtual Machine:

Once the VM is up and running, you can log into it using:
$ vagrant ssh
What This Command Does: This opens a secure shell (SSH) session inside the virtual machine, allowing you to run commands and interact with the VM as if you were using it directly.
![alt text](<proof of the vm running.png>)


## 7. Stopping and Destroying the Virtual Machine
When you’re finished working with your virtual machine, you can stop or remove it to free up resources.

To Stop the Virtual Machine:

Open a new terminal of the same directory run the following command:

$ vagrant halt
![alt text](<stopping the vm.png>)
Explanation: This command gracefully shuts down the virtual machine without deleting it, allowing you to start it again later.

To Completely Remove the Virtual Machine:

If you want to free up all resources and delete the VM, use:
$ vagrant destroy
![alt text](<vagrant destroy.png>)
Confirmation: You’ll be prompted to confirm that you want to destroy the VM. Type y (yes) to proceed.
![alt text](<proof of the vm destroyed.png>)