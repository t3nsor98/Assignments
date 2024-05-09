### Q1)Write a shell script to use a switch statement to process a menu selection, using both upper and lower-case options.
Ans:

Here is an example of a shell script that uses a switch statement to process a menu selection, allowing for both upper and lower-case options:

```bash
#!/bin/bash

# Display the menu
echo "Menu Selection:"
echo "1. Option A"
echo "2. Option B"
echo "3. Option C"
echo "4. Exit"

# Read user input
read -p "Enter your choice: " choice

# Convert user input to lowercase
choice=$(echo $choice | tr '[:upper:]' '[:lower:]')

# Process the menu selection using a switch statement
case $choice in
    1 | a)
        echo "Option A selected"
        ;;
    2 | b)
        echo "Option B selected"
        ;;
    3 | c)
        echo "Option C selected"
        ;;
    4 | exit)
        echo "Exiting the menu"
        exit 0
        ;;
    *)
        echo "Invalid choice. Please select a valid option."
        ;;
esac
```

In this script:
- The menu options are displayed.
- The user is prompted to enter their choice.
- The user input is converted to lowercase using the `tr` command.
- A switch statement (`case`) is used to process the user's menu selection.
- Each case handles both upper and lower-case options for the menu selections.
- If the user enters an invalid choice, a default case is used to display an error message.

We can save this script to a file (e.g., `menu_script.sh`), make it executable (`chmod +x menu_script.sh`), and run it in a terminal to test the menu selection functionality.

### Q2. What is Fedora/RHEL configuration tools? Explain.

Ans:
Fedora and Red Hat Enterprise Linux (RHEL) provide a range of configuration tools that allow administrators to manage and configure various aspects of the operating system. These tools are designed to simplify the process of setting up and customizing the system for specific needs and environments.

Some of the key configuration tools available in Fedora and RHEL include:

1. **System-config-network**: This tool is used for configuring network settings, including IP addresses, DNS servers, and network interfaces. It provides a graphical interface for managing network configurations.

2. **System-config-firewall**: This tool is used for configuring the firewall settings in the system. It allows administrators to set up rules for incoming and outgoing network traffic based on IP addresses, ports, and protocols.

3. **System-config-services**: This tool is used for managing system services, such as starting, stopping, and restarting services. It provides a graphical interface for configuring services and their run levels.

4. **System-config-cluster**: This tool is used for managing cluster configurations, including defining cluster nodes, fencing methods, and managed resources. It provides a graphical interface for configuring cluster settings.

5. **Conga**: This is a comprehensive user interface for installing, configuring, and managing the Red Hat High Availability Add-On. It provides a graphical interface for managing cluster services and resources.

6. **Luci**: This is the application server that provides the user interface for Conga. It allows users to manage cluster services and provides access to help and online documentation when needed.

7. **Ricci**: This is a service daemon that manages the distribution of the cluster configuration. Users pass configuration details using the Luci interface, and the configuration is loaded into corosync for distribution to cluster nodes.

8. **Yum/DNF Packages for RHEL, CentOS, and Fedora**: These packages are used for installing and managing software packages on the system. They provide a way to easily install and update software packages using the yum or dnf commands.

These configuration tools are designed to make it easier for administrators to manage and customize their systems, and they are an essential part of the Fedora and RHEL ecosystems.
