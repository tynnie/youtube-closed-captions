Youtube Closed Captions
-----------------------

Downloads the closed captions(subtitles) from Youtube videos
============================================================

.. image:: https://circleci.com/gh/mkly/youtube-closed-captions.svg?style=svg
  :target: https://circleci.com/gh/mkly/youtube-closed-captions

Requirements
~~~~~~~~~~~~

* Currently requires python >= 3.5

To Use
~~~~~~

.. code:: python

   from ytcc.download import Download

   video_id = 'jNQXAC9IVRw'
   download = Download()
   # Language is optional and default to "en"
   # YouTube uses "en","fr" not "en-US", "fr-FR"
   captions = download.get_captions(video_id, 'en')


Output Data Type
~~~~~~~~~~~~~~~~

data with timestamp 

* columns : ``start,end,text``
* data type : ``Pandas DataFrame``



Development
===========

Run Tests
~~~~~~~~~

*Note:* Functional tests do download directly from Youtube

.. code:: bash

   ## All tests
   python -m unittest discover

   ## Unit tests
   python -m unittest discover test/unit

   ## Functional tests
   python -m unittest discover test/functional

