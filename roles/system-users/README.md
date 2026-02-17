system-users
=========
Rol de Ansible para la gestión de **usuarios y grupos del sistema**.
Permite crear, modificar o eliminar usuarios y crear los grupos necesarios
a partir de variables externas al rol.

Requirements
------------
Acceso con privilegios de administrador (`become: true`) en los hosts destino

Role Variables
--------------
Variables definidas en `defaults/main.yml`:

```yaml
grupos:
  - operadores
  - dba

Dependencies
------------
Este rol no tiene dependencias con otros roles de Ansible Galaxy.

Example Playbook
----------------
- name: Gestion de usuarios y grupos
  hosts: servidores
  become: true

  vars_files:
    - inventario/users_vars/usuarios.yml

  roles:
    - system-users

License
-------
MIT-0

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
