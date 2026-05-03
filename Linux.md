Linux Commands
This document provides a comprehensive list of commonly used Linux commands for file management, system monitoring, networking, and more. Each command is accompanied by examples to help you understand its usage.

1. File and Directory Management
ls – List directory contents
ls          # List files in the current directory
ls -l       # Long format listing (includes file permissions, size, date)
ls -a       # Show hidden files (files starting with a dot)
cd – Change directory
cd /path/to/directory   # Change to a specific directory
cd ..                   # Move one directory up (parent directory)
cd ~                    # Move to the home directory
pwd – Print working directory
pwd        # Show the full path of the current directory
mkdir – Create a directory
mkdir new_directory       # Create a new directory
mkdir -p dir1/dir2/dir3   # Create nested directories
rm – Remove files or directories
rm file.txt             # Remove a file
rm -r directory_name    # Remove a directory and its contents
rm -f file.txt          # Force delete (without confirmation)
cp – Copy files or directories
cp source.txt destination.txt        # Copy a file
cp -r source_dir/ destination_dir/   # Copy a directory
mv – Move or rename files and directories
mv file.txt new_location/          # Move a file to another location
mv old_name.txt new_name.txt       # Rename a file
touch – Create an empty file
touch new_file.txt      # Create a new empty file
2. File Permissions and Ownership
chmod – Change file permissions
chmod 755 file.txt       # Set read, write, execute permissions for the owner; read, execute for others
chmod +x script.sh       # Add execute permission to a script
chown – Change file ownership
chown user:group file.txt   # Change ownership of a file
chown -R user:group dir/    # Change ownership of a directory recursively
3. Viewing and Editing Files
cat – Concatenate and display file contents
cat file.txt              # Display the contents of a file
less – View file contents page by page
less file.txt             # View file contents with scrolling
tail – View the last lines of a file (useful for logs)
tail -n 10 log.txt        # Show the last 10 lines of a file
tail -f log.txt           # Follow the live changes of a log file
head – View the first lines of a file
head -n 10 file.txt       # Show the first 10 lines of a file
nano – Simple text editor
nano file.txt             # Open a file for editing using nano
vim – Advanced text editor
vim file.txt              # Open a file for editing using vim
4. Disk Usage and System Information
df – Check disk space usage
df -h                    # Show disk usage in human-readable format (GB, MB)
du – Estimate file space usage
du -sh directory_name/    # Show the size of a directory
free – Check memory usage
free -h                  # Show free and used memory (RAM) in human-readable format
top / htop – Monitor system processes
top                      # Display real-time process information and system resources
htop                     # An enhanced version of top (if installed)
uname – Show system information
uname -a                 # Show all system information (kernel version, architecture, etc.)
lscpu – Display CPU architecture information
lscpu                    # View detailed CPU info (number of cores, architecture)
uptime – Show system uptime and load average
uptime                   # Show how long the system has been running
iostat – Display CPU and I/O statistics
iostat                   # Shows statistics related to CPU and input/output performance
5. Networking
ifconfig – Network interface configuration
ifconfig                 # Show network interface information (IP addresses, etc.)
ip – More modern tool to manage IP configurations
ip addr show             # Show IP addresses and network interfaces
ip link set eth0 up      # Bring up an interface
ip link set eth0 down    # Bring down an interface
ping – Check network connectivity
ping google.com          # Ping an external domain to test network connectivity
curl – Transfer data to or from a server
curl https://example.com   # Fetch content from a URL
wget – Download files from the web
wget https://example.com/file.zip   # Download a file from the internet
netstat – Network statistics and active connections
netstat -tuln            # Show all listening ports and services
ss – Another command for network statistics (faster than netstat)
ss -tuln                 # List open network ports and services
traceroute – Trace the path packets take to a network host
traceroute google.com    # Trace the route packets take to reach google.com
6. Process Management
ps – Display information about running processes
ps aux                    # Show all running processes
kill – Terminate a process by its PID
kill 1234                 # Terminate process with PID 1234
killall – Kill processes by name
killall nginx             # Kill all processes named 'nginx'
pkill – Kill processes based on name or attributes
pkill -f script.sh        # Kill a process running the script.sh
bg and fg – Control background/foreground jobs
bg                       # Resume a job in the background
fg                       # Bring a job to the foreground
nohup – Run a process that continues after logging out
nohup ./script.sh &       # Run a script in the background, even after logout
7. User and Group Management
adduser – Add a new user
adduser newuser           # Create a new user
usermod – Modify user accounts
usermod -aG sudo username   # Add a user to the sudo group (admin privileges)
passwd – Change a user password
passwd newuser           # Change the password for the specified user
su – Switch user
su - username            # Switch to another user
sudo – Execute commands as another user (usually root)
sudo command             # Run a command as superuser (root)
8. Package Management (based on the OS)
apt – Package manager for Debian/Ubuntu-based systems
sudo apt update          # Update the package list
sudo apt upgrade         # Upgrade installed packages
sudo apt install nginx   # Install a new package (nginx)
sudo apt remove nginx    # Remove a package
yum – Package manager for RHEL/CentOS-based systems
sudo yum update          # Update all packages
sudo yum install nginx   # Install a package (nginx)
sudo yum remove nginx    # Remove a package
9. Compression and Archiving
tar – Archive files
tar -cvf archive.tar file1 file2   # Create an archive
tar -xvf archive.tar               # Extract an archive
tar -czvf archive.tar.gz dir/      # Create a compressed archive (.tar.gz)
tar -xzvf archive.tar.gz

### **zip/unzip** – Create or extract ZIP archives

```bash
zip archive.zip file1 file2       # Create a ZIP file
unzip archive.zip                 # Extract a ZIP file
10. SSH and File Transfers
ssh – Securely log into a remote machine
ssh user@remote_host             # Connect to a remote machine via SSH
ssh -i /path/to/key user@remote   # Connect using an SSH key
scp – Securely copy files to/from a remote machine
scp file.txt user@remote:/path/   # Copy a file to a remote machine
scp user@remote:/path/file.txt .  # Copy a file from a remote machine to local
11. Miscellaneous Useful Commands
history – View command history
history                           # List all previously executed commands
alias – Create shortcuts for commands
alias ll='ls -l'                  # Create a shortcut for a long command
unalias ll                        # Remove an alias
whoami – Show current user
whoami                            # Display the current logged-in username
date – Display the current date and time
date                              # Show the current date and time
shutdown – Shutdown or restart the system
sudo shutdown now # Shutdown immediately sudo reboot # Reboot the system
