==========================================
Geo IP installation (on-premises database)
==========================================

Installation
============

.. warning::
   Please note that the installation depends on your computer's operating system and distribution.
   In this instance, we will assume that a Linux operating system is being used.

First, install `geoip2 <https://pypi.org/project/geoip2/>`__ Python library

    .. code-block:: bash

      pip install geoip2

Following that, you need to download the
`GeoLite2 City database <https://dev.maxmind.com/geoip/geoip2/geolite2/>`_.

You will end up with a file called ``GeoLite2-City.mmdb``. Then, move the file to the folder
``/usr/share/GeoIP/``

    .. code-block:: bash

        mv ~/Downloads/GeoLite2-City.mmdb /usr/share/GeoIP/

At this point, you need to restart the server.

.. note::
   If you can't/don't want to locate the GeoIP database in ``/usr/share/GeoIP/``, you can use the
   ``--geoip-db`` option of the Odoo command line interface. This option takes the absolute path to
   the GeoIP database file, and uses it as the GeoIP database. For example:

   .. code-block:: bash

      ./odoo-bin --geoip-db= ~/Downloads/GeoLite2-City.mmdb

   .. seealso::
      - `CLI documentation <https://www.odoo.com/documentation/14.0/reference/cmdline.html>`_.

.. warning::
   ``GeoIP`` Python library can also be used. However, this version is discontinued since January
   2019. See `GeoLite Legacy databases are now discontinued
   <https://support.maxmind.com/geolite-legacy-discontinuation-notice/>`_

Test GeoIP Geolocation on Odoo website
======================================

Go to your website, and open the web page you want to test ``GeoIP``. Then, select
:menuselection:`Customize --> HTML/CSS/JS Editor`, and add the following piece of XML in the page:

.. code-block:: xml

    <h1 class="text-center" t-esc="request.session.get('geoip')"/>

That leaves you with a dictionary indicating the location of the IP address.

.. image:: geo_ip_installation/on-premise_geo-ip-installation01.png
   :align: center
   :alt: on premise geo-ip installation

.. note::
   If the curly braces are empty ``{}``, it can be for any of the following reasons :

   - The browsing IP address is the localhost (``127.0.0.1``) or a local area network one
     (``192.168.*.*``)
   - If a reversed proxy is used, make sure to configure it correctly. See `--proxy-mode
     <https://www.odoo.com/documentation/14.0/reference/cmdline
     .html#cmdoption-odoo-bin-proxy-mode>`__
   - ``geoip2`` is not installed, or the GeoIP database file wasn't found
   - The GeoIP database was unable to resolve the given IP address

.. seealso::

   :doc:`../publish/essentials`

   :doc:`../publish/domain_name`

   :doc:`../publish/multi_website`

   :doc:`../publish/translate`
