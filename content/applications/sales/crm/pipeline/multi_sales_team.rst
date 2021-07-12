====================
Multiple sales teams
====================

In Odoo, you can manage several sales teams, departments, or channels with each having their own
specific sales processes. These can be managed using *Sales Teams*.


Create a new sales channel
==========================

To create a new *Sales Team*, go to :menuselection:`CRM --> Configuration --> Sales Teams` then
click **Create**.

Once on the creation page, you can set an email alias for your team, and every message sent to that
email address will create a lead/opportunity in your pipeline. You can also choose whether you
accept emails from *Everyone*, *Authenticated Partners*, or *Followers Only*.

Additionally, you can set up a domain if you want your team to receive leads/opportunities based on
specific filters, such as country, language, etc. Set an invoicing target if your team has specific
monthly revenue targets they need to achieve.

.. image:: multiple_sales_teams/sales-team-creation.png
   :align: center
   :alt: Creating a Sales Team

.. tip::
   A team name, who you accept emails from, and a minimum score are all required form fields.

Add members to your Sales Team
------------------------------

Team members can be added directly to the Sales Teams creation template when creating a new team or
at a later time via editing. Click on *Add* under the *Assignment* tab, and choose a salesperson by
typing in their name, selecting them from the drop down, or adding in a new name. If your team wants
to ensure that your salespeople are not overdoing it, you can set a maximum number of leads in a 30
day period.

.. image:: multiple_sales_teams/add-a-salesperson.png
   :align: center
   :alt: Adding a Salesperson

Assigning a *Team Leader* to your Sales Team follows a similar process as a adding a salesperson.
Type in the leader's name or choose their name from the dropdown menu.

Both team members and Team Leaders can be added to multiple Sales Teams, which allows them to easily
check all of the pipelines they need access to.

Sales Team Overviews
====================

To head over to the overview, go to :menuselection:`CRM --> Configuration --> Sales Teams`. Any
teams you are a part of will appear as overview tiles.

Each tile shows:

- All of the open and overdue opportunities, quotations, and orders needing an invoice and the
  revenue associated with each.
- Graphs showing new opportunities broken down by week
- An invoicing progress bar to show your team’s progress towards the invoicing goal set in the team
  settings

.. image:: multiple_sales_teams/sales-team-overview.png
   :align: center
   :alt: Sales Team Overview

Clicking on the three little dots opens another menu where you can quickly access information,
such as viewing quotations, creating a new opportunity, or opening a report. Additionally, you can
choose a color for your team as well as access the team configuration template.

.. image:: multiple_sales_teams/team-overview-three-dot-menu.png
   :align: center
   :alt: Three Dot Menu

If you are a sales manager managing multiple teams, you can easily tap on *Pipeline*, and Odoo will
take you directly to that team’s pipeline without having to access the Sales menu.


