Ansible Role Harness
=========

Role to setup new relic integration

See more: [Kubernetes integration: install and configure](https://docs.newrelic.com/docs/integrations/kubernetes-integration/installation/kubernetes-integration-install-configure/)



Role Variables
--------------

```
    - "{{ HARNESS_ACCOUNT_ID }}"
    - "{{ HARNESS_ACCOUNT_SECRET }}"
    - "{{ HARNESS_DELEGATE_NAME }}"
```

Example Playbook
----------------


```
- hosts: all
  become: no
  remote_user: "root"

# Uncomment "aws-eks-setup" role only if you are upgrading the cluster
    - role: ansible-role-harness
      HARNESS_ACCOUNT_ID: "{{ lookup('env', 'HARNESS_ACCOUNT_ID') }}"
      HARNESS_ACCOUNT_SECRET: "{{ lookup('env', 'HARNESS_ACCOUNT_SECRET') }}"
      HARNESS_DELEGATE_NAME: "{{ lookup('env', 'CLUSTER_NAME')}}"
```

License
-------

BSD

Author Information
------------------

- [César vergara](mailto:cvergarae@smu.cl)

