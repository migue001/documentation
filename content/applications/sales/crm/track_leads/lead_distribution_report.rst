========================
Lead distribution report
========================

A *lead distribution report* can be used to see if active leads are being assigned equitably
across sales members, view the distribution of good or `quality leads <https://www.odoo.com/
documentation/17.0/applications/sales/crm/track_leads/quality_leads_report.html>`_, and see how
frequently each salesperson is receiving (and keeping) leads.

Lead distribution reports can be run each week to help keep salespeople on track, while
providing them with ample good leads. These reports can also be used to see whether sales members
are staying productive, if good leads are being lost too often by one salesperson, and what
percentage of good leads are being retained overall.

Create lead distribution reports
================================

To create a lead distribution report, first navigate to :menuselection:`CRM app --> Reporting -->
Pipeline`, which reveals the :guilabel:`Pipeline Analysis` dashboard.

Remove all the default filters in the :guilabel:`Search...` bar at the top of the page. Doing so
displays data related to *all* leads.

Custom filters can now be added by clicking the :icon:`fa-caret-down` :guilabel:`(down caret)`
icon, to the right of the :guilabel:`Search...` bar, to reveal a drop-down menu of search and filter
options.

Three columns will be displayed: :guilabel:`Filters`, :guilabel:`Group By`, and
:guilabel:`Favorites`.

.. image:: lead_distribution_report/filters-dropdown.png
   :align: center
   :alt: Clicking the dropdown arrow in the search bar will display filters, groups, and favorites.

To begin, navigate to the bottom of the :guilabel:`Filters` column, and click :guilabel:`Add Custom
Filter`. This opens an :guilabel:`Add Custom Filter` pop-up window, where a custom filter can be
created.

.. image:: lead_distribution_report/add-custom-filters.png
   :align: center
   :alt: The Add Custom Filter pop-up window allows custom filtering rules to be created.

Custom filters
--------------

The following conditions are provided as an example of a *good* but *not comprehensive*
set of rules for finding good leads. These filters should be applied in the order specified to
achieve a heavily-detailed filter.

:ref:`creation-date`

:ref:`team-location`

:ref:`phone-number`

:ref:`active-status`

:ref:`referred-by`

:ref:`source`

:ref:`notes`

:ref:`tags`

:ref:`email`

:ref:`salesperson`

These conditions can be added, removed, or modified to best fit the desired information in
the report.

.. _creation-date:

1. Lead creation date
~~~~~~~~~~~~~~~~~~~~~

Click the first field, under :guilabel:`Match any of the following rules:`, that has the value
:guilabel:`Country` in it. A pop-up window appears. In that pop-up window, type `Date` in the
:guilabel:`Search...` bar, or scroll to search through the list to locate and select it.

Then, in the second field of the :guilabel:`Add Custom Filter` pop-up window, select :guilabel:`>=`
from the drop-down menu. This operator **only** includes values greater than (or equal to) the value
in the third, rightmost field.

The third field on the :guilabel:`Add Custom Filter` pop-up window should contain the earliest date
leads are selected from.

For example,
setting `01/01/2024 00:00:00` only includes leads created from, and including, the first day of
2024.

.. image:: lead_distribution_report/created-on.png
   :align: center
   :alt: Add a Created On rule for the start of the year onward.

.. _team-location:

2. Sales team location
~~~~~~~~~~~~~~~~~~~~~~

Click :guilabel:`New rule` to add a new set of rule fields to the :guilabel:`Add Custom Filter`
pop-up window. Click the first field for the new rule, and set it to :guilabel:`Sales Team`. Then,
click the second field of the new rule, and select :guilabel:`contains` from the drop-down menu.
Selecting this operator filters for any records that contain the words in the third, rightmost
field.

In this third field, enter the name of the desired sales team(s). For example, setting `us direct sf
northam` **only** includes sales teams assigned to the U.S., direct, San Francisco, and North
America.

.. image:: lead_distribution_report/sales-team-location.png
   :align: center
   :alt: Use Sales Team to filter the location the lead is associated with.

.. _phone-number:

3. Phone number
~~~~~~~~~~~~~~~

Click :guilabel:`New rule` to add a new rule to the filter. Set the first field to
:guilabel:`Phone`. Then, select :guilabel:`is set` from the drop-down menu in the second field.
Selecting this operator **only** filters for records that have a phone number associated with the
lead.

.. image:: lead_distribution_report/phone-set.png
   :align: center
   :alt: Report only leads with an associated phone number with the Phone field.

.. _active-status:

4. Active status
~~~~~~~~~~~~~~~~

Click the :guilabel:`Branch` icon to the right of `Phone is set` line, to add a new rule that
branches from the rules above.

Two horizontal sets of fields appear below a line showing :guilabel:`all of:` with a
:icon:`fa-caret-down` :guilabel:`(down caret)`. Click the down caret, then select
:guilabel:`any` from the resulting list.

Set the first field to :guilabel:`Active`. Then, select :guilabel:`is set` in the next field.

.. image:: lead_distribution_report/add-branch.png
   :align: center
   :alt: Click the second button to the right of phone is set labeled add branch.

Next, click the :icon:`fa-plus` :guilabel:`New Rule` button next to :guilabel:`Active is set` to
create a new line of fields beneath it.

Set the first field to :guilabel:`Active`. Then, select :guilabel:`is not set` in the next field.
This rule will add the activity status of the lead to the report.

.. image:: lead_distribution_report/active-set.png
   :align: center
   :alt: Use Active to include active status in the report.

.. _referred-by:

1. Referred by
~~~~~~~~~~~~~~

Click the :guilabel:`Branch` icon to the right of :guilabel:`any of:` field to add a new set of
rules. These appear as a new line of fields on a separate branch from the rules above. Change
:guilabel:`all of:` to :guilabel:`any of:`.

Next, set the first field to :guilabel:`Referred By`. In the second field, select
:guilabel:`contains` from the drop-down menu. In the last field, type `appointment`. This adds
any leads that were referred by an appointment.

.. image:: lead_distribution_report/referred-by.png
   :align: center
   :alt: Add referred by as a branch to filter appointments.

.. _source:

1. Source
~~~~~~~~~

Click the :icon:`fa-plus` :guilabel:`New Rule` button next to the line for `Referred by
appointment`. Set the first field to :guilabel:`Source`. Select :guilabel:`contains` from the
drop-down menu in the second field. Type `livechat` in the third field. This rule adds any leads
that came from livechat to the report.

.. image:: lead_distribution_report/add-source.png
   :align: center
   :alt: Adding a rule for source to filter for livechat.

.. _notes:

7. Notes
~~~~~~~~

Click the :icon:`fa-plus` :guilabel:`New Rule` button next to line for `Source contains livechat`.
Set the first field to :guilabel:`Notes`. Click the second field, and select :guilabel:`contains`
from the drop-down menu. Type `mrp` in the third field.

Click the :icon:`fa-plus`
:guilabel:`New Rule` icon next to the line for `Notes contains mrp`, and add a new rule for notes
containing `stock`. Repeat the process to create new rules containing the following terms:

#. purchase
#. plm
#. crm
#. sales
#. project
#. fsm

.. image:: lead_distribution_report/add-notes.png
   :align: center
   :alt: Add rules that contain the 8 terms listed above.

This includes any leads with the above terms in the attached notes to the report.

.. _tags:

8. Tags
~~~~~~~

Click the :icon:`fa-plus` :guilabel:`New Rule` icon next to line for `Notes contains fsm`.
Set the first field to `Tags`. Select :guilabel:`contains` from the drop-down menu in the second
field. Then, type `20` in the third field. This adds any leads that are tagged as a size of 5-20 or
20-50.

.. image:: lead_distribution_report/add-tags.png
   :align: center
   :alt: Add a rule for "20" to filter size.

.. _email:

9. Email
~~~~~~~~

Click :guilabel:`New rule` at the bottom of the pop-up menu to add a new rule. This new rule is
created outside the :guilabel:`any of:` group. Set the first field to :guilabel:`Email`. Select
:guilabel:`does not contain` from the drop-down menu in the next field. Next, type `hotmail` into
the rightmost field.

Repeat the previous steps to add rules for the following contents:

#. aol.com
#. icloud.com
#. yahoo

.. image:: lead_distribution_report/add-email.png
   :align: center
   :alt: Add rules to filter out the above four email domains.

.. _salesperson:

10. Salesperson
~~~~~~~~~~~~~~~

Click :guilabel:`New rule` to add a new rule. Click the first field, and locate
:guilabel:`Salesperson`. Click the :icon:`fa-chevron-right` :guilabel:`(right chevron)` button to
the right. A new list of salespeople attributes appears. Select :guilabel:`Active` from the list.
In the second field, select :guilabel:`is` from the drop-down menu. In the third drop-down menu,
select :guilabel:`set`.

.. image:: lead_distribution_report/add-salesperson.png
   :align: center
   :alt: Add a salesperson's activity status to ensure an active salesperson is selected.
