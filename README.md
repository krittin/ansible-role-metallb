Metal LB
=========

Install [Metal LB](https://metallb.universe.tf/) on Kubernetes cluster with configuration to announce service IPs via [Layer 2 configuration](https://metallb.universe.tf/configuration/#layer-2-configuration)

Requirements
------------

* Kubeconfig file placed on Ansible controller host
* ```K8S_AUTH_KUBECONFIG``` pointing to your kubeconfig file and set as environment variable in your playbook

Role Variables
--------------
```ip_pool``` as list of ip addresses for cluster to assign to workloads' loadbalancer service 


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      environment:
        K8S_AUTH_KUBECONFIG: /path/to/your/kubeconfig
      roles:
        - role: krittin.metallb
          ip_pool:
            - "192.168.0.101-192.168.0.110"


License
-------

MIT

