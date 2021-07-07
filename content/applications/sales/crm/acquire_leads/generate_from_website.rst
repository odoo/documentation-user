==============================
Generating leads/opportunities
==============================

Automating the lead/opportunity generation will considerably improve your team's efficiency.
Utilizing email aliases and a contact form in your database can aid in that improvement.

By default, any email sent to *sales@your_database_domain.ext* will create an opportunity in the
default sales channel's pipeline associated with that particular email.

Configuring email aliases
=========================

Each sales team can use their own email alias to automatically filter generated
leads/opportunities into their pipeline. This functionality can be useful when managing several
sales teams with specific individual business processes. You can find Sales Team configurations
under :menuselection:`CRM --> Configuration --> Sales Teams`.

.. image:: generate_from_website/sales-team-config.png
   :align: center
   :alt: Configuring Sales Teams

Using the Contact Us page on your website
=========================================

By default, your website's *Contact Us* page displays both your stored company information and
Odoo’s ready-to-use contact form to generate leads/opportunities.

.. image:: generate_from_website/default-contact-us-page.png
   :align: center
   :alt: Default Contact Us page

This can be activated or deactivated at any time by going to :menuselection:`Website --> Go to
Website --> Customize --> Contact Form` on your website and toggling the option on or off.

.. image:: generate_from_website/contact-form-toggle.png
   :align: center
   :alt: Contact Form toggle

When the form is toggled off, the *Contact Us* page lets visitors know that they can contact your
company by email contact and display a button to send one directly. Any emails sent this way will
generates a lead/opportunity.

.. image:: generate_from_website/default-contact-us-page-no-form.png
   :align: center
   :alt: Contact Us Page using email

To change the form to a specific sales channel, go to :menuselection:`Website --> Configuration -->
Settings.` Under *Communication,* you can change which *Sales Team* or *Salesperson* is assigned
to any incoming leads or opportunities from your Contact Form.

.. image:: generate_from_website/contact-form-settings.png
   :align: center
   :alt: Contact Form settings

Creating a custom Contact Form
==============================

Wanting more info from visitors using the Contact Form? Contact Forms can be customized for the
specific information your team needs. They can generate multiple types of records in the
system, such as emails, leads/opportunities, project tasks, helpdesk tickets, and more.

The free *Form Builder* module can be installed from either the apps page or automatically when
adding a form to a page in the Website Builder. Adding a whole new form can be great if you are
soliciting certain information that needs filtering, such as suggestions, bug reports, etc.

.. image:: generate_from_website/form-building-block.png
   :align: center
   :alt: Form Builder building blocks

However, if the Contact Us Page's available predefined form options can work with some editing,
editing these options is the fastest way to customize the form to fit your needs.

Editing contact form fields
---------------------------
In edit mode, click on the field to change, and you can edit any of the following information for
the specific field:

- **Type**: Choose a custom field option or an existing field. Examples include phone, file
  upload, language, etc.
- **Input Type**: This determines the type of entry customers should input. Available options are
  text, email, telephone, and URL.
- **Input Placeholder**: Type in an example to guide users how to input information where
  formatting is important, such as a phone number or email address.
- **Label Name**: Type in the display name to show users what information is needed from them.
- **Label Position**: Choose the way the label is aligned with the rest of the form. The label
  can be hidden, above the field, to the far left of the field, or right adjusted and closer to the
  field.
- **Required**: Toggleable option for information that you absolutely need entered.
- **Hidden**: Toggleable option to hide the given field for this form or not.
- **Shown on Mobile**: Toggleable option to show the field to users on mobile devices.

.. image:: generate_from_website/editable-field-options.png
   :align: center
   :alt: Editable field options

A completed form's default action is to send you the customer's inputted information by
email. You can change this to lead/opportunity generation in edit mode by clicking any of the
form’s fields, and under the form options, selecting **Create an Opportunity** as the action.

.. tip::
   If leads are activated in your CRM settings, selecting **Create an Opportunity** generates a
   lead instead. To learn more about activating leads in the CRM settings, head over to
   :doc:`convert`.

