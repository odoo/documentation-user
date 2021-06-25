=============================
Assign leads based on scoring
=============================

.. important::
   This feature will be completely replaced by **Predictive Lead Scoring** with Version 14.3's
   release.

With *Lead Scoring* you can automatically rank your leads based on selected criteria.

For example, you could score customers higher if coming from the same country as your company over a
customer from a different country.

Configuration
=============

To use scoring, go to :menuselection: 'Apps', remove the *Apps* filter, search for *Lead Scoring*,
and install the module.

.. image:: lead_scoring/lead-scoring-module.png
   :align: center
   :alt: Lead Scoring module installation

Create scoring rules
====================

To manage your scoring rules, go to :menuselection: 'CRM --> Leads --> Scoring Rules'.

Here's an example of a scoring rule for English-speaking Canadian users. You can modify your rules
to match whatever criteria you want to score leads on, and you can add as many criteria as you would
like.

.. image:: lead_scoring/scoring-example.png
   :align: center
   :alt: Score Rule example

Every hour, leads without a score are scanned and are then assigned a score according to your
configured rules.

.. image:: lead_scoring/scoring-section-on-lead.png
   :align: center
   :alt: Scoring section on a lead

Assign leads
============

Once the score is computed, leads can be assigned to specific teams. To do so, head to
:menuselection:`CRM --> Leads --> Team Assignment` and apply a specific domain to each team. This
domain can include scores.

.. image:: lead_scoring/team-assignation.png
   :align: center
   :alt: Team Assignments using domains

If you want more granularity, you can assign leads to a specific salesperson on the team using
further refined domains.

To do so, go to :menuselection:`CRM --> Leads --> Leads Assignment` and add the specific domains.

.. image:: lead_scoring/lead-assignment-filters.png
   :align: center
   :alt: Lead Assignments

.. note::
   The Team and Leads Assignments are assigned to unassigned leads once per day.

Evaluate & use the unassigned leads
===================================

Once your scoring rules are in place, you likely still have some unassigned leads. Some of these
leads could still transition into an opportunity, so ensuring they are handled is both useful and
important.

On your leads overview page, you filter for your unassigned leads.

.. image:: lead_scoring/unassigned-filter.png
   :align: center
   :alt: Filtering for unassigned leads

.. note::
   You can also easily find unassigned leads by using the **Email Marketing** or **Marketing
   Automation** apps to create a re-engagement campaign.
