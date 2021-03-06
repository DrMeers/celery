.. _changelog:

================
 Change history
================

This document contains change notes for bugfix & new features
in the 5.0.x series, please see :ref:`whatsnew-5.0` for
an overview of what's new in Celery 5.0.

.. _version-5.0.1:

5.0.1
=====
:release-date: 2020-10-18 1.00 P.M UTC+3:00
:release-by: Omer Katz

- Specify UTF-8 as the encoding for log files (#6357).
- Custom headers now propagate when using the protocol 1 hybrid messages (#6374).
- Retry creating the database schema for the database results backend
  in case of a race condition (#6298).
- When using the Redis results backend, awaiting for a chord no longer hangs
  when setting :setting:`result_expires` to 0 (#6373).
- When a user tries to specify the app as an option for the subcommand,
  a custom error message is displayed (#6363).
- Fix the `--without-gossip`, `--without-mingle`, and `--without-heartbeat`
  options which now work as expected. (#6365)
- Provide a clearer error message when the application cannot be loaded.
- Avoid printing deprecation warnings for settings when they are loaded from
  Django settings (#6385).
- Allow lowercase log levels for the `--loglevel` option (#6388).
- Detaching now works as expected (#6401).
- Restore broadcasting messages from `celery control` (#6400).
- Pass back real result for single task chains (#6411).
- Ensure group tasks a deeply serialized (#6342).
- Fix chord element counting (#6354).
- Restore the `celery shell` command (#6421).

.. _version-5.0.0:

5.0.0
=====
:release-date: 2020-09-24 6.00 P.M UTC+3:00
:release-by: Omer Katz

- **Breaking Change** Remove AMQP result backend (#6360).
- Warn when deprecated settings are used (#6353).
- Expose retry_policy for Redis result backend (#6330).
- Prepare Celery to support the yet to be released Python 3.9 (#6328).

5.0.0rc3
========
:release-date: 2020-09-07 4.00 P.M UTC+3:00
:release-by: Omer Katz

- More cleanups of leftover Python 2 support (#6338).

5.0.0rc2
========
:release-date: 2020-09-01 6.30 P.M UTC+3:00
:release-by: Omer Katz

- Bump minimum required eventlet version to 0.26.1.
- Update Couchbase Result backend to use SDK V3.
- Restore monkeypatching when gevent or eventlet are used.

5.0.0rc1
========
:release-date: 2020-08-24 9.00 P.M UTC+3:00
:release-by: Omer Katz

- Allow to opt out of ordered group results when using the Redis result backend (#6290).
- **Breaking Change** Remove the deprecated celery.utils.encoding module.

5.0.0b1
=======
:release-date: 2020-08-19 8.30 P.M UTC+3:00
:release-by: Omer Katz

- **Breaking Change** Drop support for the Riak result backend (#5686).
- **Breaking Change** pytest plugin is no longer enabled by default (#6288).
  Install pytest-celery to enable it.
- **Breaking Change** Brand new CLI based on Click (#5718).

5.0.0a2
=======
:release-date: 2020-08-05 7.15 P.M UTC+3:00
:release-by: Omer Katz

- Bump Kombu version to 5.0 (#5686).

5.0.0a1
=======
:release-date: 2020-08-02 9.30 P.M UTC+3:00
:release-by: Omer Katz

- Removed most of the compatibility code that supports Python 2 (#5686).
- Modernized code to work on Python 3.6 and above (#5686).
