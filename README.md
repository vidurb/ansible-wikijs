Role Name
=========

Wiki.js Role

Requirements
------------


Role Variables
--------------

Variable | Type | Default | Usage
--- | --- | --- | ---
`wikijs_unix_user` | string | wikijs | Unix username for Wiki.js user
`wikijs_dir` | string | `~/wiki` | Directory to install Wiki.js
`wikijs_subdomain` | string | shaastr | Subdomain for Wiki.js, must have trailing `.`, can be blank to install on root domain
`wikijs_domain` | string | getastra.dev | Domain for Wiki.js
`wikijs_bind_ip` | string | 127.0.0.1 | IP to bind Wiki.js node server to
`wikijs_bind_port` | int | 9001 | Port to bind Wiki.js node server
`wikijs_db_type` | string | postgres | Wiki.js database type
`wikijs_db_host` | string | 127.0.0.1 | Wiki.js database host
`wikijs_db_port` | int | 5432 | Wiki.js database port
`wikijs_db_user` | string | wikijs | Wiki.js database username
`wikijs_db_password` | string | insecurepassword | Wiki.js database password
`wikijs_db_name` | string | wikijs | Wiki.js database name
`wikijs_enable_local_postgres` | boolean | true | Install postgres locally
`wikijs_enable_cloudflare` | boolean | false | Update Cloudflare DNS 
`wikijs_cloudflare_api_token` | string | none | Cloudflare API token
`wikijs_cloudflare_account_email` | string | none | Cloudflare account email address
`wikijs_nginx_conf_options` | string | See `defaults/main.yml` | Nginx conf options


Dependencies
------------

- `geerlingguy.postgres`: required if `wikijs_enable_local_postgres` is true
- `geerlingguy.nginx`
- `geerlingguy.nodejs`

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
