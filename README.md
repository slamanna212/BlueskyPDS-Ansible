# BlueskyPDSAnsible
Ansible playbooks to manage my Bluesky PDS server, phase.social. 

# Features
 - Handles general maintence tasks for the Ubuntu 22 host

# Requirements
 - Your Bluesky PDS on DigitalOcean. You can use this with servers in other locations but you will need to make modifications to commands for your different inventory. 

# Setup
1. This repo requires some Galaxy Modules, install them with:

     `ansible-galaxy install -r collections/requirements.yml`

2. Copy extra_vars_TEMPLATE.yml , name it extra_vars.yml and fill it out. All values are required.

3. Run checklist.yml. It will export API keys and make sure the system is ready for the other playbooks. Be sure to include extra vars, more info below.
     `ansible-playbook --extra-vars "extra_vars.yml" checklist.yml`

4. Reload your shell
     `exec bash`

## Playbooks

- `checklist.yml` Makes sure localhost is ready to run these playbooks

## Need to Know
Initial provisioning is not yet coded. 