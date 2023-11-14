Getting Started with OMERO
==========================

The Basics
==========

Before You Begin
----------------

Read through the documentation listed here:

https://www.openmicroscopy.org/omero/institution/getting-started.html
https://omero-guides.readthedocs.io/en/latest/

https://docs.alliancecan.ca/wiki/Technical_documentation

https://github.com/WU-BIMAC/W-IDM_OmeroImporter

What You Will Need
------------------

1. Compute Canada account

   a. PI needs to sponsor you to get this

2. Submit a request to get associated with the ``rpp-steveogg`` project

   a. This will allow you to login to the Arbutus open stack dashboard
      `here <https://arbutus.cloud.computecanada.ca/auth/login/>`__. The
      dashboard is where we can manage instances, volumes, etc.

3. Before you can ssh into the VMs, you need to whitelist your IP on the
   dashboard. Do so by adding your IP to the ssh group with the
   appropriate labels.
4. Someone will make an admin account for you for each of the OMERO
   instances so that you can manage groups/users.
5. In order to ssh into the servers, you need the identity key
   (``arbutus-key``, ``omero-dev``) associated with the server. It will
   be provided to you.

Managing Groups/Users
---------------------

Rule of Thumb:

-  A PI or Lab gets their own group
-  Anybody working under the PI or in the Lab becomes a member of the
   lab (there is no difference between an undergraduate student vs a
   postdoc in roles)
-  Each publication gets its own public group with the Public user as 
   a member and the authors as the owners

All of this management can be done through your admin account on
OMERO.web through the Admin tab.

It is also possible to send out emails to users from the Admin tab. The
email will be sent out from omero.notifications@gmail.com to the
specified users. Use this feature to let the users know when the server
may be down for updates, etc.

Logging into an Instance
------------------------

Any installations or config updates can be done by logging in directly
into the server, or through ansible playbooks
`here <https://github.com/stephenogg/playbooks>`__. All of the playbooks
are forked from the OME playbooks
`here <https://github.com/ome/prod-playbooks>`__ and
`here <https://github.com/ome/omero-deployment-examples>`__.

Use command ``ssh -i [PATH TO KEY] ubuntu@[IP]`` to login.

The available instances are:

+-----------------------+-----------------------+
| Description           | Key                   |
+=======================+=======================+
| Production            | arbutus_key,          |
| (National_OMERO)      | omero_dev             |
+-----------------------+-----------------------+
| Training (Replica of  |                       |
| Dundee’s training     |                       |
| with already uploaded |                       |
| data)                 |                       |
+-----------------------+-----------------------+
| Daily Backup          |                       |
+-----------------------+-----------------------+
| Grafana               |                       |
+-----------------------+-----------------------+

If you ever need to add a new key to an instance, append the public key
to ``.ssh/authorized_keys``

Any OMERO configuration changes that need to be made through the CLI can
be done with ``/opt/omero/server/OMERO.server/bin/omero`` or
``/opt/omero/web/OMERO.web/bin/omero`` as the ``omero`` command shown on
the official OMERO docs.

Useful Links
============

https://forum.image.sc/

https://ccdb.computecanada.ca/security/login

https://idr.openmicroscopy.org/

https://www.openmicroscopy.org/index.html

https://www.youtube.com/c/OpenMicroscopyEnvironment

https://github.com/stephenogg/playbooks

check status of DRAC resources here: https://status.alliancecan.ca/

nextcloud storage: https://nextcloud.computecanada.ca/index.php/s/Ji7SHA5W6mJjsxz

`Architecture/architecture-omero-irods.svg · architecture-omero-irods ·
FBI data / Documentation and web / OmeroDeployments ·
GitLab <https://gitlab.in2p3.fr/fbi-data/websites/OmeroDeployments/-/blob/architecture-omero-irods/Architecture/architecture-omero-irods.svg>`__
