# Ansible LEMP Playbook

This repository contains an Ansible playbook and role for setting up a LEMP stack (Linux, Nginx, MySQL, PHP) along with phpMyAdmin on your servers.

## Repository Structure

- `ansible.cfg`: Ansible configuration file.
- `inventory.yml`: Inventory file defining the hosts.
- `web.yml`: Main playbook file.
- `LEMP/`: Directory containing the LEMP role with tasks, templates, handlers, etc.

## Prerequisites

1. **Ansible**: Ensure Ansible is installed on your local machine. You can install it using pip:

    ```bash
    pip install ansible
    ```

2. **SSH Access**: Ensure you have SSH access to the target servers.

## Setting Up

1. **Clone the repository**:

    ```bash
    git clone https://github.com/karthigeyanbaskaran/Ansible-LEMP-Stack.git
    cd Ansible-LEMP-Stack
    ```

2. **Inventory Configuration**:

    Edit the `inventory.yml` file to include your target servers.

    ```yaml
    all:
      hosts:
        your_server:
          ansible_host: your.server.ip
          ansible_user: your_user
    ```

## Running the Playbook

Execute the playbook using the following command:

```bash
ansible-playbook web.yml

This command will use the `inventory.yml` file to target the specified hosts and run the `web.yml` playbook.

## Role Structure
The `LEMP` role is structured as follows:

- `tasks/`: Contains the main tasks to set up the LEMP stack.
  - `main.yml`: Main task file.
- `templates/`: Contains the Jinja2 templates.
  - `nginx.conf.j2`: Nginx configuration template.
- `handlers/`: Handlers to restart services.
  - `main.yml`: Main handlers file.
- `vars/`: Variables for the role.
  - `main.yml`: Main variables file.
- `defaults/`: Default variables for the role.
  - `main.yml`: Default variables file.
- `meta/`: Metadata about the role.
  - `main.yml`: Main metadata file.
- `tests/`: Test files for the role.
  - `test.yml`: Test playbook.
  - `inventory`: Test inventory file.

## Customization
You can customize the role by editing the variables in `vars/main.yml` and `defaults/main.yml`, as well as modifying the templates in `templates/`.


## Authors
- Karthigeyan - [your-username](https://github.com/karthigeyanbaskaran)
