==============
Product images
==============

The integration with **Google Custom Search API** is a feature that allows finding images
automatically for your product, based on their barcode.

.. _product_images/configuration:

Configuration
=============

This functionnality requires configuration both on Google and on Odoo.

Google includes 100 free requests per day (about 100 images if all of them are found). To enable
up to 10K requests per day, you need to configure your Google account to do so.

.. seealso::
   - `Create, modify, or close your Cloud Billing account
     <https://cloud.google.com/billing/docs/how-to/manage-billing-account>`_

.. _product_images/google-api-dashboard:

Google API dashboard
--------------------

#. Go to `Google Cloud Platform <https://console.developers.google.com/>`__ API & Services page
   to generate Google Custom Search API credentials. Log in with your Google account.

#. Select or create an API project to store the credentials if not yet done
   before. Give it an explicit name (e.g. Odoo Images).

#. In the credentials section, click on Create Crendentials and select **API Keys**.

   .. image:: product_images/google-images-credentials00.png
      :align: center

#. Save it, you'll need it for the next step in Odoo !

#. Use the search bar to find for *Google Custom Search API* and select it.

   .. image:: product_images/google-images-credentials01.png
      :align: center

#. Enable the API.

   .. image:: product_images/google-images-credentials02.png
      :align: center

.. _product_images/google-pse-dashboard:

Google Programmable Search dashboard
------------------------------------

#. Go to `Google Programmable Search Engine <https://programmablesearchengine.google.com/>`__ and
   click on Get Started. Log in with your Google account.

   .. image:: product_images/google-images-credentials03.png
      :align: center

#. Fill the language and the name of the search engine. Give it an explicit name
   (e.g. Odoo Images).

   .. note::
      Google doesn't allow to create a search engine without having entered at least one specific
      site to search on. You can put any website (e.g. www.google.com) for this step, we will
      remove it later.

#. Validate the form by clicking on Create. Then, go to the edition mode of the search engine
   that you created (either by clicking on Control Panel button on the confirmation page or by
   clicking on the name of your Search Engine on the Home page).

#. In the basics tab, make sure to enable Image search, SafeSearch and Search the entire web.

   .. note::
      Once Search the entire web enabled, you can safely delete the site that you previously
      entered at the previous step.

#. Save your **Search Engine Id**.

   .. tip::
      You can easily save your Search Engine ID by clicking on the Copy to clipboard button next to
      it.

.. _product_images/setup-in-odoo:

Odoo
----

#. Go to :menuselection:`Settings --> General Settings --> Integrations`,
   activate **Google Images** and save.

#. Go back to :menuselection:`Settings --> General Settings` and enter your **API Key** and
   **Search Engine ID** in Google Images option.

#. The setup is now ready.

.. _product_images/get-product-images:

Automatically get your product images in Odoo
=============================================

The action to automatically get your product images in Odoo appears in any Products or Product
Variants list view. Here is a step-by-step guide from the Inventory app.

#. Go to :menuselection:`Inventory --> Products --> Products` or :menuselection:`Inventory -->
   Products --> Product Variants`.

#. On the list view, select the products that needs an image.

   .. important::
      Only the 10K first products or product variants selected will be processed.

   .. note::
      Only the products or product variants with a barcode and without an image will be processed.
      If you select a product that has one or more variants from the Products view, each variant
      matching the previous criteria will be processed.

#. In the action menu, select the option *Get Pictures from Google Images* and validate by clicking
   on *Get picture*.

#. You should see your images appearing in the next few minutes.

   .. note::
      Only the 10 first images are fetched immediatly. If you selected more than 10, the rest will
      be fetched as a background job, so you can continue doing your work while illustrating your
      products.

      The background job process about 100 images in a minute. If you reach the quota authorized
      by Google (either with a free or a paid plan), the background job will put itself on hold
      for 24 hours and continue right where he stopped the day before. Any other background task
      with a more important weight (e.g. payment post-processing job) will be executed in priority
      and might extend the processing time.

.. _product_images/faq:

Troubleshooting
===============

Here are the most frequently asked questions about this feature. Feel free to add more questions
(with their answers, of course !) by editing this page on Github.
See :ref:`contributing/github-interface` for additional help.

.. _product_images/less-quality-or-not-found:

Images have less quality than I expected, or are not found
----------------------------------------------------------

* Check if the barcode is correct (Avoid whitespaces, hypen, dots...).

* Do manually a research on Google Images and compare the results. If you find better results than
  in Odoo, also check your `Google Programmable Search Engine
  <https://programmablesearchengine.google.com/>`__.

.. note::
   The first picture found that corresponds with our criteria is saved. No matter how many times
   you execute the action, you should get each time the same picture, unless results have changed
   on Google's side. There are the criteria used when making a request to Google:

   * Safe mode is activated
   * Image size is large
   * Image type is photo
   * Search type is image

   Currently, you can't change those variables. They can impact the result for less popular
   products but should greatly improve results on a large scale.

.. _product_images/errors:

Possible errors
---------------

Most of the errors that you might encounter are very explicit and should be easy to resolve.
However, here are a few tips on what you can do in those cases.

.. _google-cs-api: https://console.cloud.google.com/marketplace/product/google/customsearch.googleapis.com

+----------------------------+--------------------------------------------------------------------+
|        UserError           |                         Solution                                   |
+============================+====================================================================+
| Another task is already    | It means that for some reason, the job is scheduled but has been   |
| scheduled to pick the      | delayed. In that case, your selection is saved and images will be  |
| images on Google on *Date*.| fetched on *Date*. If you want to cancel the task, you have to go  |
|                            | into debug mode. Then, go to :menuselection:`Settings -->          |
|                            | Technical --> Scheduled Actions Triggers` and delete it. Keep in   |
|                            | mind that, by deleting the trigger, you will cancel the task but   |
|                            | not erase the selection. If you launch the task again with more    |
|                            | than 10 Products or Product Variants selected, the old selection   |
|                            | will also be processed at the same time.                           |
+----------------------------+--------------------------------------------------------------------+
| You didn't configure       | You may have forgotten to save after entering the parameters in    |
| properly your **API Key**  | the Settings.                                                      |
| or **Search Engine ID**.   |                                                                    |
+----------------------------+--------------------------------------------------------------------+
| There isn't any product    | Check your selection of Products. If any Products or their variants|
| without a picture and      | already have a picture, they won't be processed. Also, check if you|
| with a barcode.            | well entered a barcode.                                            |
+----------------------------+--------------------------------------------------------------------+
| Custom Search API is not   | Check that you have enabled the Custom Search API in your Google   |
| enabled in your Google     | project either by visiting the link displayed in the error in Odoo |
| project.                   | or by checking the `Google Cloud Platform <google-cs-api_>`_ Custom|
|                            | Search API page.                                                   |
+----------------------------+--------------------------------------------------------------------+
| Your **API Key** or        | Check if you properly configured the **API Key** and/or the        |
| your **Search Engine ID**  | **Search Engine ID** in Odoo. A common mistake is to invert these  |
| is incorrect.              | variables.                                                         |
+----------------------------+--------------------------------------------------------------------+
