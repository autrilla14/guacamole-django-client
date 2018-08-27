=======================
guacamole-django-client
=======================

A django project, python version of project guacamole-client, for communication with `Guacamole <http://guac-dev.org/>`_ server (guacd)

Support Python 2.7

Installation
============

After cloning the project, run:

    $ pip install -r requirement.txt

    $ python manage.py runserver


Configuration
=============

...



Development
===========

Please refer to `Official guacamole document <http://guacamole.incubator.apache.org/doc/0.9.13-incubating/gug/>`_


Notes
=====

guacamole-django-client is licensed under the `Apache License 2.0 <https://github.com/heisaman/guacamole-django-client/blob/master/LICENSE>`_ and is based on efforts by Rescale `django-guacamole <https://github.com/rescale/django-guacamole>`_ project and Mohab Usama `pyguacamole <https://github.com/mohabusama/pyguacamole>`_ project.

In views.py
===========

SSH:
    client.handshake(protocol='ssh',
                     hostname=settings.SSH_HOST,
                     port=settings.SSH_PORT,
                     username=settings.SSH_USER,
                     password=settings.SSH_PASSWORD)
RDP:
    client.handshake(protocol='rdp',
                     hostname=settings.RDP_HOST,
                     port=settings.RDP_PORT,
                     width= 1920,
                     height=900,
                     security='nla',
                     ignore_cert='true',
                     username=settings.RDP_USER,
                     password=settings.RDP_PASSWORD
                     )
VNC:
    client.handshake(protocol='vnc',
                     hostname=settings.VNC_HOST,
                     port=settings.VNC_PORT,
                     password=settings.VNC_PASSWORD)

