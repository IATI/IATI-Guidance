How is the data updated?
========================

Updates
-------

Every night two processes take place.

- Firstly the IATI Registry reviews and updates all its information, checking that all items in its catalogue still exist (or are accessible), and whether the data stored on the publishers’ websites has changed.
- Secondly the Datastore reviews all changes in the Registry. New activities are added to the database and changed activities are reloaded. Any database records of activities that have been removed from the Registry are also deleted.
- Warning! Note that this is an overnight job so it can take up to 24 hours or more for new publishers’ data to appear in the store.

Cleaning
--------

When the data is imported into the Datastore, certain fields are cleaned to ensure consistent output without altering the meaning of the data. Date and money formats are standardised, as are country, currency and language codes.
