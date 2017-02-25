This base-server role installs a few packages I consider useful on any instance. 
It also configures a couple of users and groups by default, these are easily overridden by host/group/inventory/playbook vars etc.

I'd advise you to remove my public key from the role if you intend to reuse this code - and if using in a prod environment,
that you implement finer grained controls on sudo!