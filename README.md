Ansible role CA-Certs
=========

Add additional trusted certificate authorities to Rhel / Debian based hosts

Requirements
------------

None

Example Playbook
----------------

    ---
    - hosts: all
      sudo: yes

      vars_files:
        - vars.yml

      roles:
         - { role: jgeusebroek.ca_certs, tags: ["ca_certs"] }

Example Variables
----------------

    # This expects a certificate in the files/ca-certs directory named ca-custom.crt
    ca_certs_install:
    [ 'ca-custom.crt' ]

License
-------

BSD

Author Information
------------------

Jeroen Geusebroek
me@jeroengeusebroek.nl