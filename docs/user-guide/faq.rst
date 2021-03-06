FAQ
===

What version of the Python Client should I use?
-----------------------------------------------

If you are starting a new project or your existing project does not yet use the
Python Client, we encourage you to use the **latest stable version** of the Python
Client.

----

If you are already using the Python Client, you have 3 options:


1. **"I like my project's code the way it is."**

  Keep using the version you are on.

2. **"I want some new features released in versions with the same major version that I'm currently using."**

  Upgrade to the latest stable version *with the same major version* as what
  you currently use.

3. **"I want all new features and I'm willing to modify my code to get those features!"**

  Upgrade to the latest stable version *even* if it has a different major
  version from what you currently use.

Note that you do not need to reason about the Unify API version nor the the Unify version.

----

**How does this the Python Client accomplish this?**

The short answer is that the Python Client just cares about features, and will
try everything it knows to implement those features correctly, independent of
the API version.

We'll illustrate with an example.

Let's say you want to get a dataset by name in your Python code.

**1.** If no such feature exists, you can file a Feature Request. Note that the Python
Client is limited by what the Unify API enables. So you should check if the Unify
API docs to see if the feature you want is even possible.

**2.** If this feature already exists, you can try it out!

E.g. ``unify.datasets.by_name(some_dataset_name)``

  **2.a** It works! 🎉

  **2.b** If it fails with an HTTP error, it could be for 2 reasons:

    **2.a.i** It might be impossible to support that feature in the Python Client
    because your Unify API version does not have the necessary endpoints to
    support it.

    **2.a.ii** Your Unify API version *does* support this feature with some endpoints,
    but the Python Client know how to correctly implement this feature for this
    version of the API. In this case, you should submit a Feature Request.

  **2.c** If it fails with any other error, you should submit a Bug Report. 🐛


.. note::
  To see how to submit Bug Reports / Feature Requests, see :ref:`bug-reports-feature-requests`.

  To check what endpoints your version of the Unify API supports, see `docs.tamr.com/reference <https://docs.tamr.com/reference>`_
  (be sure to select the correct version in the top left!).
