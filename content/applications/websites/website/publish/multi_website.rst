========================
Manage multiple websites
========================

Odoo helps users to build, customize, and manage multiple websites in one easy-to-use platform.

Having multiple websites opens up the possibilities of diversification and customer segmentation
for any business. Multiple websites are also a great way to multiply your audience and boost
revenue!

Each Odoo website can work in a fully independent way, with its very own theme, branding, domain
name, pages, languages, products, blogs, forums, events, live chat channels, and so much more.

Setup
=====

To create a new website, go to :menuselection:`Website --> Configuration --> Settings`.

.. image:: multi_website/config-settings.png
   :align: center
   :alt: website application configuration settings

To start building a new website, simply click on *+New* located next to the title of the "Website"
section on the *Website* settings page.

.. image:: multi_website/new-website-button.png
   :align: center
   :alt: new website button on the settings page

When clicked, a pop-up appears. In this pop-up, you input the name of your new website, its domain,
and a logo (if you have one).

.. image:: multi_website/new-website-pop-up.png
   :align: center
   :alt: new website pop-up with empty information fields

.. note::
   If you want to publish this new website under the default domain of your Odoo database, simply
   leave the domain field blank.

Once all the necessary fields have been filled, you may click *Pick a Theme* to select how you
want your new website to look.

.. image:: multi_website/pick-theme-button.png
   :align: center
   :alt: website pick a theme button on the pop-up window

Clicking that, takes you to a catalog of professional-grade website themes that Odoo has to
choose from.

Remember, this new website may have an entirely different purpose (and/or audience) than your
initial site. So, feel free to choose a completely new theme to fit your needs. And, don't
forget, you can change themes at any time.

.. image:: multi_website/multi-website-theme-selection.png
   :align: center
   :alt: various website themes

To select a theme, hover the cursor over your desired theme, and click *Use This Theme*. You can
also preview what that theme would look like, by selecting *Live Preview*.

.. image:: multi_website/theme-live-preview-hover.png
   :align: center
   :alt: website theme live preview hover over options

Once a theme is selected, you can start building your website. Not sure where to begin? Simply
follow the "purple drops" located on the screen. They will help get your started.

.. image:: multi_website/purple-drops.png
   :align: center
   :alt: website builder purple drops

When the cursor hovers over them, they explain the function and purpose of that particular
feature.

.. image:: multi_website/purple-drops-explanation.png
   :align: center
   :alt: website builder purple drops with explanation of function

Then, you can start dragging and dropping any of Odoo's "Building Blocks" (on the right) to create
your design. Remember to hit *Save* once you are done.

.. image:: multi_website/partially-built-homepage.png
   :align: center
   :alt: partially built website with building blocks

.. note::
   If you run Odoo Online, don’t forget to redirect any new domain name to your Odoo database
   (``CNAME``) and to authorize it on the Odoo-side. See :doc:`domain_name`.

Create the menu
===============

By default, this new website has a default menu with all the installed applications.

To edit it, click :menuselection:`Pages --> Edit Menu`.

.. image:: multi_website/pages-edit-menu.png
   :align: center
   :alt: pages edit menu on header

When selected, a pop-up appears, in which you can modify the header menu of your website.

.. image:: multi_website/edit-menu-pop-up.png
   :align: center
   :alt: edit header menu pop-up window

.. note::
   Moving forward, you only edit the menu of the website you are currently on.

Switching websites
==================

In the upper-right corner, there is a "Website Switcher" drop-down menu. It will show the website
that you are currently on. When clicked, it will reveal your other websites, which you can instantly
jump to with one click.

If you use another domain for the website, the user is requested to sign in.

.. image:: multi_website/multi_website03.png
   :align: center
   :alt: website switcher button in the corner

.. note::
   When switching, you are redirected to the same domain path on the other website
   (e.g., ``/shop/myproduct``). If this URL is not used, you will be redirected to a 404 page, and
   prompted to create a new page from there.

Add features
============

The website apps you install (like *Blogs*) are made available on all your websites. Of course,
you can keep them hidden in one website by removing the menu item, as previously mentioned.

Each website comes with a wide array of features and options that can be found on the *Settings*
page (:menuselection:`Website app --> Configuration --> Settings`).

To modify those features and options, you first need to select which website you want to
customize. In order to do that, you need to select your desired website from the first section of
settings, titled: "Select the Website to Configure."

.. image:: multi_website/multi_website15.png
   :align: center
   :alt: selecting which website should be configured

Once a website is selected, take a look at the options on the rest of the page, particularly the
ones flagged with an Earth icon.

This icon means that those features will only impact the very website you are currently working on.

.. image:: multi_website/multi_website12.png
   :align: center
   :alt: earth icon in the website settings menu

You can, for instance, set specific:

-  Languages

-  Domain names

-  Social media links

-  Dedicated live chat channels

-  And so much more...

The other options are global and will apply to *all* your websites.

Customize the visitor experience
================================

Thanks to Odoo's *Customize* menu, there are plenty of ways you can customize (and enhance) the
overall user experience for your visitors.

All the visual-related options in this drop-down menu are specific to each page you are
customizing.

For example, the options available for your blogs won't be the same as the options available for
your online store because each page serves a different purpose. Odoo provides the user with the
professional-grade options and features to enhance every single page, no matter what.

So, while building your website, be sure to go through the different pages, and adapt them to fit
this new audience/purpose. Focus on workflows and automatic pages (eCommerce checkout, blogs,
events, etc.), as there more options to be found there.

.. image:: multi_website/customize-drop-down.png
   :align: center
   :alt: customize drop-down menu on the front-end of the website

Publish specific content per website
------------------------------------

Like static pages, any content created from the front-end (product page, blog post, etc.) is always
*only* published on that current website.

You can change that by editing the form in the back-end, and leaving the *Website* field blank.
This will publish it on all your websites.

.. image:: multi_website/multi_website06.png
   :align: center
   :alt: publishing content on a specific website

Here are all the objects you can link to *any (or all)* websites:

1. Products

2. Product Categories (for eCommerce)

3. Blogs

4. Pages

5. Forums

6. Events

7. Job Positions

8. eLearning Courses

Publish on all websites
-----------------------

When a new static page is created, it's only made available on that current website. However, you
can duplicate it to other websites by going to :menuselection:`Website --> Configuration --> Pages`.

Then, select the page you wish to duplicate, click *Edit*, and leave the *Website* field empty.

If you want to duplicate it in just *one* other website, duplicate the page, and select your
desired website in the the *Website* field of the newly duplicated page.

.. image:: multi_website/multi-website-pages.png
   :align: center
   :alt: placing a page onto another website

To efficiently (and quickly) manage your pages, you can click
:menuselection:`Pages --> Manage Pages` found on the front-end of the website.

.. image:: multi_website/manage-pages-drop-down.png
   :align: center
   :alt: manage pages drop-down menu option

That takes you to a page with all your web pages and you can edit/modify them in a number of
different ways.

.. image:: multi_website/multi-website-manage-pages.png
   :align: center
   :alt: the manage pages section on the front-end

.. tip:: 
   By grouping pages by URL in the page manager, you quickly find the original page behind
   each edited page.

.. image:: multi_website/multi_website10.png
   :align: center
   :alt: detailed look at the manage pages section

Multiple companies
==================

If you are working in a multi-company environment, each website can be linked to a specific
company in your system.

To link each website to a specific company, go to
:menuselection:`Website application --> Configuration --> Settings` and select which company
you'd like to link to this website, located in the *Website* section.

.. image:: multi_website/multi_website16.png
   :align: center
   :alt: choose which website to designate to a company

With such a configuration in place, only company-related data will appear on that website (products,
jobs, events, etc.).

Website editors can only view and edit pages of records they have access to, which is typically
only the ones that belong to their current company (and to their subsidiaries, or child companies
in Odoo language).

.. note::
   If websites are multi-companies, you don’t change the company when switching websites. To
   change the company, and see the related content, use the company selector in the menu.

   .. image:: multi_website/different-company-drop-down.png
      :align: center
      :alt: company selector drop-down menu

Configure eCommerce website
===========================

eCommerce is a crucial feature for any online business, especially one with multiple websites. Odoo
allows users to customize the entire flow (and shopping experience) to cater to the specific
audience found on each website.

Products only available on one website
--------------------------------------

Above, you learned how to publish a specific record on only one website. The process is similar
for eCommerce products, as well.

Simply modify the *Website* field in the eCommerce tab of the product form. And remember, an
empty field means it will be available on all websites.

.. image:: multi_website/multi-website-ecommerce-tab.png
   :align: center
   :alt: the ecommerce tab of a pricelist template

Products available on select websites
-------------------------------------

To make a product available on some websites, but not all of them, you can duplicate the product,
and assign it to each website you want it to appear on.

If you need a unique reference to manage in your inventory, you should install *Manufacturing*
and create *Kits* BoMs (Bills of Materials).

Each kit will link each published “virtual” product to the main reference managed in your inventory.
That way, any item sold from your website will be converted into the storable item in the delivery
order.

Pricelists
----------

To manage specific prices by website, go to :menuselection:`Website app --> Configuration -->
Settings` and activate *Pricelists* and *Multiple Prices per Product* in the *Pricing* section.
Then, hit *Save*.

.. image:: multi_website/pricelists-setting.png
   :align: center
   :alt: specific pricelists setting

Following that, go to :menuselection:`Website --> Products --> Pricelists` to create additional
pricelists. Or you can click on *--> Pricelists* located beneath the *Pricelists* option in the
*Pricing* section of the *Website* settings.

.. image:: multi_website/various-routes-to-pricelists.png
   :align: center
   :alt: various routes to get to the pricelists page

See :doc:`../../ecommerce/maximizing_revenue/pricing` if you need more information.

After clicking a pricelist you wish to modify, simply select a website in the *Website* field
(found in the *Configuration* tab of the pricelist detail form), and that pricelist becomes
exclusively available on that website only.

.. image:: multi_website/multi-website-pricelist.png
   :align: center
   :alt: designate which website is linked to which pricelist

Leaving the field empty means this pricelist will be available on *all* websites, but it will
only be visible to customers if *Selectable* is activated in the pricelist detail form, as well.

Otherwise, it's only available for backend operations in the *Sales* and *Point of Sale*
applications.

Payment Acquirers and Delivery Methods
--------------------------------------

By default, published payment acquirers and delivery methods are deployed in all websites.

You could use specific payment acquirers per country (using Geo IP) by defining countries in their
configuration. Or, you can do it per website by filling in the *Website* field.

Customer accounts
-----------------

You can choose how to manage your customer accounts in the settings of the *Website* application.
Go to :menuselection:`Website --> Configuration --> Settings` and select *Specific User Account*
in the *Website* section.

Activating this feature forces your user to create a specific account for each of your websites.
This comes in handy if your websites shouldn't be related to each other in the visitor's mind.
However, you can allow customers to use one account for all your websites, by simply
deactivating that feature.

.. image:: multi_website/multi_website17.png
   :align: center
   :alt: specific user account in website settings

Technical hints for customization
=================================

If you want to publish custom objects on the website, here are a few tips to make it work with
multiple websites:

-  **Sitemap**: don’t forget the domain in the route to only publish available records in each
   website's sitemap.

-  **Access**: you should call the method *can_access_from_current_website* in the controller to
   make sure the visitor can see a record in the current website.

-  **Search**: when a list of records is displayed, don’t forget to specify the domain to *only*
   display records available for the current website.

.. image:: multi_website/multi_website11.png
   :align: center
   :alt: coding language of technical customization

.. seealso::

   :doc:`../publish/essentials`

   :doc:`../publish/geo_ip_installation`

   :doc:`../publish/domain_name`

   :doc:`../publish/translate`
