Mail-sandbox
========

Role for setup mail-sandbox application

Requirements
------------

  - zzet.common
  - zzet.rbenv
  - zzet.postgresql
  - bennojoy.redis
  - bennojoy.nginx
  - zzet.runit

Role Variables
--------------

    project_name: mail_sandbox
    project_user: mail_sandbox
    project_path: mail_sandbox
    project_env: production
    project_port: 9001
    project_locale: 'UTF-8'
    project_repo: git@github.com:zzet/mail_sandbox.git
    project_uri: mail-sandbox.example.com
    vm: 1 # Setup for production or vm. If production = 0

    postgresql:
      version: 9.2
      encoding: 'UTF-8'
      locale: 'en_US.UTF-8'

      user: "{{ project_user }}"
      password: mysupersecretpassword

      production_name: "{{ project_user }}_production"
      development_name: "{{ project_user }}_development"
      test_name: "{{ project_user }}_test"

Dependencies
------------

  - zzet.common
  - zzet.rbenv
  - zzet.postgresql
  - bennojoy.redis
  - bennojoy.nginx
  - zzet.runit

License
-------

MIT

Author Information
------------------

[Andrew Kumanyaev](https://github.com/zzet)
