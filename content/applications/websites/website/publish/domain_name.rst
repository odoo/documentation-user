==================
Custom domain name
==================

By default, your Odoo database (and website) have an *.odoo.com* domain name, which is seen in the
URL and emails.

However, you can change it to a custom URL (e.g. *www.yourcompany.com*) at any time.

Good domain qualities
=====================

Choosing the right domain name for your business is extremely important for your branding.

That's why it's vital to consider the following aspects when creating a custom URL for your business
(or organization).

Make sure your domain name is:

- Simple and obvious
- Easy to remember (*and* spell)
- Concise: the shorter, the better
- Avoid special characters
- Aim for a ".com" and/or your country extension

Read more: `How to Choose a Domain Name for Maximum SEO <https://www.searchenginejournal.com/choose-a-domain-name-maximum-seo/158951/>`__

Buy a domain name
=================

Buy your domain name at a popular registrar site, like:

- `GoDaddy <https://www.godaddy.com>`__  
- `Namecheap <https://www.namecheap.com>`__  
- `OVH <https://www.ovh.com>`__ 

.. note:: Steps to buy a domain name are pretty straight-forward. If you have any issues, check out
   this easy-to-follow tutorial:

   - `GoDaddy <https://roadtoblogging.com/buy-domain-name-from-godaddy>`__

   Feel free to buy an email server to have email addresses using your domain name. However,
   *don't* buy any extra service to create (or host) your website - that's Odoo's job!

.. _custom_domain:


Apply domain name to Odoo
=========================

First, you must authorize the URL redirection (*yourcompany.com --> yourcompany.odoo.com*):

To do that, open your Odoo.com account from the homepage.

.. image:: domain_name/odoo-account.png
   :align: center
   :alt: opening odoo.com account from homepage

Then, select *My Databases* page under the same drop-down menu.

.. image:: domain_name/my-databases.png
   :align: center
   :alt: manage databases page

That redirects to the *Manage Your Databases* page. Here, you need to click on *Domains* to the
right of the database you want to redirect.

.. image:: domain_name/manage-databases.png
   :align: center
   :alt: clicking domains of the database

Then, a database domain prompt appears, wherein you enter your custom domain:
(e.g. *www.yourcompany.com*).

.. image:: domain_name/enter-domain.png
   :align: center
   :alt: domain name database prompt

At this point, you can apply the redirection from your domain name's manager account:

In order to do that, log in to your account, and search for the DNS Zones management page.

Then, create a CNAME record (*www.yourdomain.com*) pointing to *mywebsite.odoo.com*. If you want to
use the naked domain (e.g. *yourdomain.com*), you need to redirect *yourdomain.com* to
*www.yourdomain.com*.

.. note:: Here are some specific guidelines to create a CNAME record:

   - `GoDaddy <https://be.godaddy.com/fr/help/add-a-cname-record-19236>`__
   - `Namecheap <https://www.namecheap.com/support/knowledgebase/article.aspx/9646/10/how-can-i-set-up-a-cname-record-for-my-domain>`__
   - `OVH <https://www.ovh.co.uk/g1519.exchange_20132016_how_to_add_a_cname_record>`__

Enable SSL (HTTPS) for Odoo
===========================

Odoo no longer requires users to use a third-party CDN service provide (like, CloudFlare) to
enable SSL. Odoo generates the certificate for you automatically, using integration with
`Let's Encrypt Certificate Authority and ACME protocol <https://letsencrypt.org/how-it-works/>`__.

In order to enable SSL, simply add your domain name in your customer portal. A separate certificate
is generated for each domain name specified.

.. warning::
  **The certificate generation may take up to 24h.**

.. note::
   If you already use CloudFlare (or a similar service), you can keep using it, or simply change to
   Odoo.

Website indexed twice by Google
===============================

If you set up a custom domain name (*mydomain.com*) for *mydatabase.odoo.com*, Google indexes your
website under *both* names.

This is a minor limitation of the Odoo cloud platforms.

.. seealso::

   :doc:`../publish/essentials`

   :doc:`../publish/geo_ip_installation`

   :doc:`../publish/multi_website`

   :doc:`../publish/translate`
