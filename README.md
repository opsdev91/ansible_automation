# Ansible Collections for Automating Proxmox VMs and Server Applications

This repository contains Ansible collections for automating the deployment of Proxmox VMs and server applications, including Jira and Confluence servers. These collections are designed to simplify the process of setting up and managing your infrastructure, while providing a flexible and extensible framework for customization and scaling.

## Getting Started

To use this repository, you will need to have Ansible installed on your local machine. You can download and install Ansible from the official website: [https://www.ansible.com/](https://www.ansible.com/)

Once you have installed Ansible, you can clone this repository to your local machine and navigate to the root directory:

```bash
git clone https://github.com/opsdev91/ansible_collection
cd ansible_collection
```


## Folder Structure

The repository is organized into the following directories and files:

- `ansible.cfg`: Ansible configuration file
- `confluence_playbook.yml`: Ansible playbook for creating a VM with installed Confluence
- `delete_vm.yml`: Ansible playbook for deleting a VM from Proxmox
- `inventories`: Directory containing inventory files for different environments
- `jira_playbook.yml`: Ansible playbook for creating a VM with installed Jira
- `proxmox_playbook.yml`: Ansible playbook for creating a VM with common apps (nginx, java, mysql, postgres, mssql)
- `requirements.yml`: Ansible requirements file
- `roles`: Directory containing Ansible roles for different applications and services
- `test_playbook.yml`: Ansible playbook for testing the infrastructure
- `vars`: Directory containing variable files for different environments and applications
- `windows_server.yml`: Ansible playbook for creating a Windows Server VM

## Usage

To use the Ansible collections in this repository, you can simply run the desired playbook with the `ansible-playbook` command, specifying the inventory file and any necessary variables:

```bash
ansible-playbook -i inventories/dev -e @vars/proxmox.yml proxmox_playbook.yml
```

This command will create a new VM on your Proxmox server with the specified apps installed.

## Contributing

If you would like to contribute to this repository, please feel free to submit a pull request with your changes or suggestions. We welcome any feedback or ideas for improving this project!

## License

This repository is licensed under the [MIT License](LICENSE). Feel free to use and modify the code as needed.