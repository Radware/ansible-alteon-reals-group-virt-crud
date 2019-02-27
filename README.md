# ansible-alteon-reals-group-virt-crud
Basic operations crud (create,read,update,delete) for reals, group, virt.

Important notes:

All Radware ansible modules require installation of vdirect-client. Installing it is as simple as running the command: 
sudo pip install vdirect-client. See vdirect_client parameters description here, you may want to modify their defaults while using this playbook.
Playbook parameters files should be reviewed and modified prior to using the playbook. See parameters files description below.

How to use:
vars/slb_params.yml defines all slb parameters for configuring reals, group, virt. 
action define the exact operation - create|update|delete.

Each of playbook's tasks have a tag

upload - for uploading the vDirect template file to vDirect. The default template name is real_servers_crud.vm.
reals - for real servers configuration
group - for group  configuration
virt - for virt  configuration
commit - for apply/save/sync changes
