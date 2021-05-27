=============
Track traffic
=============

Now that you've created a website with engaging content, it's time to see how well it performs with
your audience. That's why it's incredibly important to track your website's traffic. With Odoo,
users can track this vital information in a number of different ways.

Track traffic in Google Analytics
=================================

To follow your website's traffic with Google Analytics you need to `Create a Google Analytics
account <https://www.google.com/analytics/>`__ if you don't have one.

Then, you must complete the creation form and accept the conditions to get the tracking ID.

    .. image:: tracking_analytics/google_analytics_account.png
       :align: center
       :alt: google analytics account

Following that, copy the tracking ID to insert it in Odoo.

    .. image:: tracking_analytics/google_analytics_tracking_id.png
       :align: center
       :alt: google analytics tracking id

Now, go to :menuselection:`Configuration --> Settings` in the Website app. Then, you must turn on
Google Analytics, and paste the tracking ID here. Don't forget to hit *Save* when you're done.

      .. image:: tracking_analytics/google-analytics-setting.png
         :align: center
         :alt: google analytics setting

If you need help getting started with Google Analytics, you can refer to `Google Documentation
<https://support.google.com/analytics/answer/1008015?hl=en/>`_.

Track traffic from Odoo Dashboard
=================================

You can accurately track traffic statistics straight from your Odoo Website Dashboard, thanks to
Google Analytics.

First, you need to create a Google Analytics account. Then, copy and paste your tracking ID
in your website settings. Next, go to `Google APIs platform library <https://console.cloud.google
.com/apis/library?supportedpurview=project>`__ in order to generate Analytics API credentials.

Now, log in with your Google account, and create a new project with an appropriate name (e.g. Odoo).
You need this project to store your API credentials.

.. image:: tracking_analytics/google_analytics_create_project.png
   :align: center
   :alt: google analytics create project

In the API Library, select *Google Analytics API*.

.. image:: tracking_analytics/google-analytics-api.png
   :align: center
   :alt: google analytics api

Then, select *Enable* next to "Analytics API."

.. image:: tracking_analytics/google_analytics_enable.png
   :align: center
   :alt: google analytics enable api

In order to properly use this API, you need to create credentials to use in Odoo.

.. image:: tracking_analytics/google_analytics_create_credentials.png
   :align: center
   :alt: google analytics create credentials

Following that, you must select *Web browser (Javascript)* as the calling source and *User data* as
the kind of data.

.. image:: tracking_analytics/google_analytics_get_credentials.png
   :align: center
   :alt: google analytics api get credentials

Then, you can create a Client ID.

To do so, enter the name of the application (e.g. My Odoo Database) and the allowed pages that
trigger a redirection.

The *Authorized JavaScript origin* is your Odoo's database URL. The *Authorized redirect URI* is
your Odoo database URL followed by '/google_account/authentication', as showcased below.

.. image:: tracking_analytics/google_analytics_authorization.png
   :align: center
   :alt: google analytics authorization

Proceed to the Consent Screen, and enter a product name (e.g. Google Analytics in Odoo). You
can check the customizations options at this time, but it's not mandatory.

.. note::
   The Consent Screen will *only* show up when you enter the Client ID in Odoo for the **first**
   time.

Then, you are provided with your Client ID, which you then copy to paste in Odoo.

.. image:: tracking_analytics/google_analytics_client_id.png
   :align: center
   :alt: google analytics client id

Go to :menuselection:`Website application --> Configuration --> Settings`, activate *Google
Analytics Dashboard* and paste the Client ID in the fields that appear.

.. image:: tracking_analytics/google-analytics-dashboard.png
   :align: center
   :alt: google analytics dashboard setting

And finally, authorize Odoo to access your Google API.

.. image:: tracking_analytics/google_analytics_login.png
   :align: center
   :alt: google analytics login

Link Trackers
=============

Link Trackers allow you to easily track all your marketing campaigns (emails, banner ads, blog
posts, social media posts, affiliate links, etc.). With Link Trackers, you can quickly identify your
your best traffic sources. This valuable data helps you make more informed decisions about the
distribution of your marketing budget.

Set up
------

On the front-end of your website, go to :menuselection:`Promote --> Link Tracker`.

Here, you are able to get a specific tracked URL based on the campaign, medium, and source being
used.

.. image:: tracking_analytics/link_tracker_fields.png
   :align: center
   :alt: View of the link tracker fields for Odoo Website

- **URL**: URL of the page you want to track (e.g. the home page or a product page).
- **Campaign**: context of your link (e.g. a special promotion).
- **Medium**: channel used to share (deliver) your link (e.g. an email or a Facebook ad).
- **Source**: platform where the traffic originates (e.g. Google or Twitter).

Then, click *Get tracked link* to generate a URL that you can post (or send) by the source you have
decided on.

Follow-up on tracked links
--------------------------

On that same Link Tracker page, beneath the *Get tracked link* fields, you can look at statistics
in the *Your tracked links* section.

In addition to seeing the *Most Clicked* and *Recently Used* links, you can also see complete
statistics by clicking on *Stats* next to a link you want to analyze, including the number of
clicks.

.. image:: tracking_analytics/links_statistics.png
   :align: center
   :alt: View of the tracked list emphasizing the statistics buttons in Odoo Website

.. tip::
   #. You can also access the link tracker on *odoo.com/r* via your browser.
   #. Activate the developer mode (:menuselection:`Settings --> Activate the developer mode`) and
      get access to the *Link Tracker* module and its back-end functionalities.
   #. Integrated with Google Analytics, those trackers allow you to see the number of clicks and
      visitors to keep you on top of your marketing campaigns.

.. seealso::

   :doc:`../optimize/seo`
