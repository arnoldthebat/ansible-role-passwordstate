<!-- cspell:ignore Ansible, hostvars, boto, apicall, passwordstate, vars, playbook -->

Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: localhost

  tasks:
  - name: GetFolders
    vars:
      apicall: GetFolders
    include_role:
        name: ansible-role-passwordstate
  - debug:
      var=GetFolders.json
```

Example execution of the tests:

In order to run the samples from within the role directory for testing, use the following command line example to set the roles path:

```bash
export ANSIBLE_ROLES_PATH=$HOME/dev && \
ansible-playbook "${HOME}/dev/ansible-role-passwordstate/tests/samples.yml" \
--extra-vars="@/${HOME}/passwordstate.yml" \
--vault-id ~/vault_password -v
```

```bash
export ANSIBLE_ROLES_PATH=$HOME/dev && \
ansible-playbook "${HOME}/dev/ansible-role-passwordstate/tests/password_update_sample.yml" \
--extra-vars="@/${HOME}/passwordstate.yml" \
--vault-id ~/vault_password -v
```

```bash
export ANSIBLE_ROLES_PATH=$HOME/dev && \
ansible-playbook "${HOME}/dev/ansible-role-passwordstate/tests/password_create_sample.yml" \
--extra-vars="@/${HOME}/passwordstate.yml" \
--vault-id ~/vault_password -v
```

License
-------

GNU

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
