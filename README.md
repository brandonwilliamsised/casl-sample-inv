# ised-ocp-casl-inv

## General Instructions for a new environment {env}
- copy an existing environment
    - ie: `dev.ocp.ised-isde.canada.ca.d` -> `{env}.ocp.ised-isde.canada.ca.d`
- edit `ec2.ini`
	- instance_filters (set to {env}, ie: prod)
- edit `all.yml`
	- set `env_id` (environment name)
	- set infrastructure variables (instance sizes)
	- set vpc cidr (to avoid collisions when peering)
- edit OSEv3.yml (optional - for non-github auth) 
	- configure `openshift_master_identity_providers` (see OpenShift docs)
