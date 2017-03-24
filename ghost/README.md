This is a role for the ghost.js blogging platform: https://github.com/TryGhost/Ghost.

This does not contain any actual ghost.js code, which this role assumes is handled another way (I use AWS Codedeploy, for instance). 
It does however contain a template config.js - this contains secrets for connecting to a postgres instance such as RDS. The defaults included here
are just dummy values - rather than storing these in plaintext in source control, I'd advise either an encrypted `vars/main.yml` using Ansible Vault
or passing in a vars file at the command line via the `--extra-vars "@some_file.json"` method. The ghost-config.js is meant to be symlinked into the main ghost directory after code checkout - this is a way to use the templating capability of Ansible with the somewhat inflexible appspec.yml used by AWS Codedeploy. If you intend to checkout your ghost.js repo via the Ansible git module, you can simply change the template dest directory to be inside that dir.

Assuming you lay down code via another method, ghost will run as a systemD service.
