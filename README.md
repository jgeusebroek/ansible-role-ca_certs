[![Build Status](https://travis-ci.org/jgeusebroek/ansible-role-ca_certs.svg?branch=master)](https://travis-ci.org/jgeusebroek/ansible-role-ca_certs)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-jgeusebroek.ca__certs-blue.svg)](https://galaxy.ansible.com/jgeusebroek/ca_certs)

# Ansible role: ca_certs

An Ansible Role that adds additional certificate authorities to RedHat/CentOS or Debian/Ubuntu.

## Requirements

None

## Dependencies

None

## Example Playbook

    ---
    - hosts: all
      sudo: yes

      roles:
         - { role: jgeusebroek.ca_certs, tags: ["ca_certs"] }

## Example Variables

    # This expects a certificate in the files/ca-certs directory named ca-custom.crt
    ca_certs_install:
      [ 'ca-custom.crt' ]

    # Location where the certificates can be found can be changed with:
    ca_certs_default_cert_location: "{{ playbook_dir }}/files/ca-certs/"

## License

MIT / BSD

## Author Information

By [Jeroen Geusebroek](http://jeroengeusebroek.nl/) 2016 - 2018.
