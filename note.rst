Ironic note
-----------

Deploy use
==========

- **RESTful API** in *ironic/api/controllers/v1/*

- **Conductor service** created within the *ironic-conductor*. Functionality 
    is exposed via API servive in *ironic/conductor*

- **Database and DB API** sotre the state of the conductor and drivers in
    *ironic/db*

- **Deployment Ramdisk or Deployment Agent** provide control over hardware
  which cannot controll by condoctor. The agent is not run inside a tenant 
  instance

- **Driver** use to controll to hardware

juno --> kilo
=============

Kilo add a new feature is **Node Cleaning**. Node can clean the node for the 
new work load.

If you configured with cleaning enable and use Nutron as DHCP provider, you 
need to set the *cleaning_network_uuid* opeiton in ironic.conf before start the
kilo ironic service.
