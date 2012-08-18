Description
===========

Install and configure the [CloudFoundry](http://www.cloudfoundry.org/) MongoDB service.

Requirements
============

Cookbooks
---------

* cloudfoundry
* cloudfoundry\_service
* mongodb

Platform
--------

* Ubuntu

Tested on:

* Ubuntu 11.10

Attributes
==========

# MongoDB gateway

* `node['cloudfoundry_mongodb_service']['gateway']['log_level']` - Controls the amount of details that is logged. Defaults to `info`
* `node['cloudfoundry_mongodb_service']['gateway']['node_timeout']` - How long (in seconds) should the gateway wait for an answer from a node on provisioning requests. Defaults to `30`
* `node['cloudfoundry_mongodb_service']['gateway']['timeout']` - How long (in seconds) should the cloud_controller wait for an answer from the gateway. Defaults to `15`

# MongoDB node

* `node['cloudfoundry_mongodb_service']['node']['index']` - Unique index of the given service node. This *must* be unique among all nodes in a single cluster. Defaults to `0`
* `node['cloudfoundry_mongodb_service']['node']['capacity']` - Maximum number of service instances for this node. Defaults to `200`
* `node['cloudfoundry_mongodb_service']['node']['log_level']` - Controls the amount of details that is logged. Defaults to `info`
* `node['cloudfoundry_mongodb_service']['node']['port_range']['first']` / `['last']` - Range of ports assigned to service instances on this node. Defaults to `25000-40000`
* `node['cloudfoundry_mongodb_service']['node']['op_time_limit']` = Time limit (in seconds) for the node to complete the provisioning of a new instance. Defaults to `6`

Usage
=====

License and Author
==================

Author:: Andrea Campi (<andrea.campi@zephirworks.om.com>)
Author:: Trotter Cashion (<cashion@gmail.com>)

Copyright:: 2012 ZephirWorks
Copyright:: 2012 Trotter Cashion

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
