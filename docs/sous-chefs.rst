
Sous Chefs
-------------
**newslynx-sc-facebook** provides access to the following Sous Chefs

Facebook Page to Event
~~~~~~~~~~~~~~~~~~~~~~

-  Extracts events from a facebook page.
-  This Sous Chef runs the python module
   ``newslynx_sc_facebook.events.Page``.
-  API Slug: ``facebook-page-to-event``

Usage
^^^^^

Standalone
''''''''''

Run this Sous Chef via the api, passing in arbitrary runtime options,
and stream it's output.

.. code:: shell

    $ newslynx api sous-chefs cook -d=newslynx_sc_facebook/facebook_page_to_event.yaml --passthrough **options

Run this Sous Chef via the api, and if applicable, send it's output to
bulkload.

.. code:: shell

    $ newslynx api sous-chefs cook -d=newslynx_sc_facebook/facebook_page_to_event.yaml **options

Do either of the above two, but pass in a recipe file

.. code:: shell

    $ newslynx api sous-chefs cook -d=recipe.yaml

Recipes
'''''''

Add this Sous Chef to your authenticated org

.. code:: shell

    $ newslynx api sous-chefs create -d=newslynx_sc_facebook/facebook_page_to_event.yaml

Create a Recipe with this Sous Chef with command line options.

.. code:: shell

    $ newslynx api recipes create sous_chef=facebook-page-to-event **options

Alternatively pass in a recipe file.

.. code:: shell

    $ newslynx api recipes create sous_chef=facebook-page-to-event --data=recipe.yaml

Save the outputted ``id`` of this recipe, and execute it via the API.
**NOTE** This will place the recipe in a task queue.

.. code:: shell

    $ newslynx api recipes cook id=<id>

Alternatively, run the Recipe, passing in arbitrary runtime options, and
stream it's output: **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: shell

    $ newslynx api recipes cook id=<id> --passthrough **options

Development
'''''''''''

Pass runtime options to ``facebook-page-to-event`` and stream output.
**NOTE** Will not execute the SousChef's ``load`` method.

.. code:: shell

    $ newslynx sc-run newslynx_sc_facebook/facebook_page_to_event.yaml option=value1

Alternatively pass in a recipe file

.. code:: shell

    $ newslynx sc-run newslynx_sc_facebook/facebook_page_to_event.yaml --recipe=recipe.yaml

Options
^^^^^^^

In addition to default recipe options, ``facebook-page-to-event`` also
accepts the following

-  ``page_id``

   -  This is what comes after the "facebook.com/" in the url for your
      facebook page. Do not include the full URL.

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``string``

-  ``must_link``

   -  Only create an event if there is a link to an existing content
      item.

   -  **Required**
   -  Should be rendered with a ``checkbox-single`` form.
   -  Choose from:

      -  ``False``

   -  Accepts inputs of type:

      -  ``boolean``

   -  Defaults to ``False``

-  ``search_query``

   -  A search query to apply to the text and urls of posts on the page

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``searchstring``

   -  Defaults to ``None``

-  ``set_event_title``

   -  Set's the title of the resulting events. This can be a python
      format string which has access to all of an event's top-level
      keys: IE: "Content from {authors} at {created}."

   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``None``

-  ``set_event_description``

   -  Set's the description of the output events. This can be a python
      format string which has access to all of an event's top-level
      keys: IE: "{title}."

   -  Should be rendered with a ``paragraph`` form.
   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``None``

-  ``event_status``

   -  Set the status of the resulting events. Choose from pending and
      approved. Defaults to pending.

   -  Should be rendered with a ``select`` form.
   -  Choose from:

      -  ``pending``
      -  ``approved``

   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``pending``

-  ``set_event_tag_ids``

   -  A list of Tag IDs or slugs to automatically apply to events
      created by this recipe.

   -  Should be rendered with a ``checkbox`` form.
   -  Choose from:

   -  Accepts inputs of type:

      -  ``string``
      -  ``numeric``

   -  Defaults to ``[]``

-  ``set_event_content_items``

   -  A list of Content Item IDs and Titles to automatically apply to
      events created by this Recipe.

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

Usage
^^^^^

Standalone
''''''''''

Run this Sous Chef via the api, passing in arbitrary runtime options,
and stream it's output.

.. code:: shell

    $ newslynx api sous-chefs cook -d=newslynx_sc_facebook/facebook_page_to_org_timeseries.yaml --passthrough **options

Run this Sous Chef via the api, and if applicable, send it's output to
bulkload.

.. code:: shell

    $ newslynx api sous-chefs cook -d=newslynx_sc_facebook/facebook_page_to_org_timeseries.yaml **options

Do either of the above two, but pass in a recipe file

.. code:: shell

    $ newslynx api sous-chefs cook -d=recipe.yaml

Recipes
'''''''

Add this Sous Chef to your authenticated org

.. code:: shell

    $ newslynx api sous-chefs create -d=newslynx_sc_facebook/facebook_page_to_org_timeseries.yaml

Create a Recipe with this Sous Chef with command line options.

.. code:: shell

    $ newslynx api recipes create sous_chef=facebook-page-to-org-timeseries **options

Alternatively pass in a recipe file.

.. code:: shell

    $ newslynx api recipes create sous_chef=facebook-page-to-org-timeseries --data=recipe.yaml

Save the outputted ``id`` of this recipe, and execute it via the API.
**NOTE** This will place the recipe in a task queue.

.. code:: shell

    $ newslynx api recipes cook id=<id>

Alternatively, run the Recipe, passing in arbitrary runtime options, and
stream it's output: **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: shell

    $ newslynx api recipes cook id=<id> --passthrough **options

Development
'''''''''''

Pass runtime options to ``facebook-page-to-org-timeseries`` and stream
output. **NOTE** Will not execute the SousChef's ``load`` method.

.. code:: shell

    $ newslynx sc-run newslynx_sc_facebook/facebook_page_to_org_timeseries.yaml option=value1

Alternatively pass in a recipe file

.. code:: shell

    $ newslynx sc-run newslynx_sc_facebook/facebook_page_to_org_timeseries.yaml --recipe=recipe.yaml

Options
^^^^^^^

In addition to default recipe options,
``facebook-page-to-org-timeseries`` also accepts the following

-  ``page_id``

   -  This is what comes after the "facebook.com/" in the url for your
      facebook page. Do not include the full URL.

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



