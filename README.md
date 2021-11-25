Ansible Role Harness
=========

Role to setup harness integration

See more: [Harness Documentation](https://ngdocs.harness.io/)



Role Variables
--------------

```
    - "{{ HARNESS_ACCOUNT_ID }}"
    - "{{ HARNESS_ACCOUNT_SECRET }}"
    - "{{ HARNESS_DELEGATE_NAME }}"
    - "{{ HARNESS_DELEGATE_PROFILE }}"
    - "{{ HARNESS_ACCOUNT }}"

```

Example Playbook
----------------


```
- hosts: all
  become: no
  remote_user: "root"

    - role: ansible-role-harness
      HARNESS_ACCOUNT_ID: "{{ lookup('env', 'HARNESS_ACCOUNT_ID') }}"
      HARNESS_ACCOUNT_SECRET: "{{ lookup('env', 'HARNESS_ACCOUNT_SECRET') }}"
      HARNESS_DELEGATE_NAME: "{{ lookup('env', 'CLUSTER_NAME')}}"
      HARNESS_DELEGATE_PROFILE: "{{ lookup('env',  HARNESS_DELEGATE_PROFILE ) }}"
      HARNESS_ACCOUNT: "{{ lookup('env', 'HARNESS_ACCOUNT') }}"
```


Author Information
------------------

- [César vergara](mailto:cvergarae@smu.cl)

