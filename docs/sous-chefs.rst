
Sous Chefs
-------------
**newslynx-sc-facebook** provides access to the following Sous Chefs

Facebook Page to Event
~~~~~~~~~~~~~~~~~~~~~~

-  Extracts events from a facebook page.
-  This Sous Chef runs the python module
   ``newslynx_sc_facebook.events.Page``.
-  API Slug: ``facebook-page-to-event``

Development
^^^^^^^^^^^

Pass runtime options to ``facebook-page-to-event`` and stream output.
**NOTE** Will not execute the SousChef's ``load`` method.

.. code:: bash

    $ newslynx sc newslynx_sc_facebook/facebook_page_to_event.yaml option=value1

Alernatively pass in a recipe file

.. code:: bash

    $ newslynx sc newslynx_sc_facebook/facebook_page_to_event.yaml --recipe=recipe.yaml

API Usage
^^^^^^^^^

Add this Sous Chef to your authenticated org

.. code:: bash

    $ newslynx api sous-chefs create -d=newslynx_sc_facebook/facebook_page_to_event.yaml

Create a Recipe with this Sous Chef with command line options.

.. code:: bash

    $ newslynx api recipes create sous_chef=facebook-page-to-event **options

Alerternatively pass in a recipe file.

.. code:: bash

    $ newslynx api recipes create sous_chef=facebook-page-to-event --data=recipe.yaml

Save the outputted ``id`` of this recipe, and execute it via the API.
**NOTE** This will place the recipe in a task queue.

.. code:: bash

    $ newslynx api recipes cook id=<id>

Alernatively, run the Recipe, passing in arbitrary runtime options, and
stream it's output: **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx api recipes cook id=<id> --passthrough **options

Options
^^^^^^^

In addition to default recipe options, ``facebook-page-to-event`` also
accepts the following

-  ``page_id``

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``string``

-  ``must_link``

   -  **Required**
   -  Should be rendered with a ``checkbox-single`` form.
   -  Choose from:

      -  ``False``

   -  Accepts inputs of type:

      -  ``boolean``

   -  Defaults to ``False``

-  ``search_query``

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``searchstring``

   -  Defaults to ``None``

-  ``set_event_title``

   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``None``

-  ``set_event_description``

   -  Should be rendered with a ``paragraph`` form.
   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``None``

-  ``event_status``

   -  Should be rendered with a ``select`` form.
   -  Choose from:

      -  ``pending``
      -  ``approved``

   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``pending``

-  ``set_event_tag_ids``

   -  Should be rendered with a ``checkbox`` form.
   -  Choose from:

   -  Accepts inputs of type:

      -  ``string``
      -  ``numeric``

   -  Defaults to ``[]``

-  ``set_event_content_items``

   -  Should be rendered with a ``search`` form.
   -  Choose from:

   -  Accepts inputs of type:

      -  ``json``

   -  Defaults to ``[]``



Facebook Page Timeseries Metrics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Computes a timeseries of of metrics for one or more facebook pages.
-  This Sous Chef runs the python module
   ``newslynx_sc_facebook.metrics.Page``.
-  API Slug: ``facebook-page-to-org-timeseries``

Development
^^^^^^^^^^^

Pass runtime options to ``facebook-page-to-org-timeseries`` and stream
output. **NOTE** Will not execute the SousChef's ``load`` method.

.. code:: bash

    $ newslynx sc newslynx_sc_facebook/facebook_page_to_org_timeseries.yaml option=value1

Alernatively pass in a recipe file

.. code:: bash

    $ newslynx sc newslynx_sc_facebook/facebook_page_to_org_timeseries.yaml --recipe=recipe.yaml

API Usage
^^^^^^^^^

Add this Sous Chef to your authenticated org

.. code:: bash

    $ newslynx api sous-chefs create -d=newslynx_sc_facebook/facebook_page_to_org_timeseries.yaml

Create a Recipe with this Sous Chef with command line options.

.. code:: bash

    $ newslynx api recipes create sous_chef=facebook-page-to-org-timeseries **options

Alerternatively pass in a recipe file.

.. code:: bash

    $ newslynx api recipes create sous_chef=facebook-page-to-org-timeseries --data=recipe.yaml

Save the outputted ``id`` of this recipe, and execute it via the API.
**NOTE** This will place the recipe in a task queue.

.. code:: bash

    $ newslynx api recipes cook id=<id>

Alernatively, run the Recipe, passing in arbitrary runtime options, and
stream it's output: **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx api recipes cook id=<id> --passthrough **options

Options
^^^^^^^

In addition to default recipe options,
``facebook-page-to-org-timeseries`` also accepts the following

-  ``page_name``

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``string``

Metrics
^^^^^^^

``facebook-page-to-org-timeseries`` generates the following Metrics

-  ``fb_page_likes``

   -  Display name: ``Facebook Page Likes``

   -  Type: ``cumulative``

   -  Org Levels:

      -  ``timeseries``
      -  ``summary``



