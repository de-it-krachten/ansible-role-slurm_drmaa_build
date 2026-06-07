[![CI](https://github.com/de-it-krachten/ansible-role-slurm_drmaa_build/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-slurm_drmaa_build/actions?query=workflow%3ACI)


# ansible-role-slurm_drmaa_build

Create packages for Slurm DRMAA



## Dependencies

#### Roles
None

#### Collections
- community.general

## Platforms

Supported platforms

- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- RockyLinux 8
- RockyLinux 9
- OracleLinux 8
- OracleLinux 9
- AlmaLinux 8
- AlmaLinux 9
- Debian 11 (Bullseye)
- Debian 12 (Bookworm)
- Ubuntu 22.04 LTS
- Ubuntu 24.04 LTS
- Ubuntu 26.04 LTS

Note:
<sup>1</sup> : no automated testing is performed on these platforms


## Role Variables
### defaults/main.yml
<pre><code>
slurm_drmaa_version: "1.1.5"

slurm_drmaa_install_mode: "package"   # options: package, source

slurm_drmaa_cleanup: true

slurm_inc_dir: "/usr/include/slurm"
slurm_lib_dir: "/usr/lib64"

maintainer_name: "Mark van Huijstee"
maintainer_email: "mark.van.huijstee@de-it-krachten.nl"
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'slurm_drmaa_build'
  hosts: all
  become: 'yes'
  tasks:
    - name: Include role 'slurm_drmaa_build'
      ansible.builtin.include_role:
        name: slurm_drmaa_build
</pre></code>
