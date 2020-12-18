勉強用のrepository
=======


.. image:: https://travis-ci.org/aws/aws-cli.svg?branch=develop

   :target: https://travis-ci.org/aws/aws-cli
   :alt: Build Status

.. image:: https://badges.gitter.im/aws/aws-cli.svg
   :target: https://gitter.im/aws/aws-cli
   :alt: Gitter


This package provides a unified command line interface to Amazon Web
Services.

Jump to:

-  `jump1 <#jump1>`__
-  `jump2 <#jump2>`__
-  `jump3 <#jump3>`__

jump1(ふと文字アンダーバー)
---------------

This README is for the AWS CLI version 1. If you are looking for
information about the AWS CLI version 2, please visit the `v2
branch <https://github.com/aws/aws-cli/tree/v2>`__.

ふと文字
~~~~~~~~~~~~

The aws-cli package works on Python versions:

-  ポチ

なんか説明とかかく

*ななめにかく*

*We recommend that all customers regularly monitor the* `リンク
website <https://リンクのURLかく>`__

Installation
~~~~~~~~~~~~

The safest way to install the AWS CLI is to use
`pip <https://pip.pypa.io/en/stable/>`__ in a ``virtualenv``:

::

   コードがかける

``くくれる``

.. note::

::

   $ aws configure
   AWS Access Key ID: MYACCESSKEY
   AWS Secret Access Key: MYSECRETKEY
   Default region name [us-west-2]: us-west-2
   Default output format [None]: json

To use environment variables, do the following:

::

   $ export AWS_ACCESS_KEY_ID=<access_key>
   $ export AWS_SECRET_ACCESS_KEY=<secret_key>

To use the shared credentials file, create an INI formatted file like
this:

::

   [default]
   aws_access_key_id=MYACCESSKEY
   aws_secret_access_key=MYSECRETKEY

   [testing]
   aws_access_key_id=MYACCESKEY
   aws_secret_access_key=MYSECRETKEY

and place it in ``~/.aws/credentials`` (or in
``%UserProfile%\.aws/credentials`` on Windows). If you wish to place the
shared credentials file in a different location than the one specified
above, you need to tell aws-cli where to find it. Do this by setting the
appropriate environment variable:

::

   $ export AWS_SHARED_CREDENTIALS_FILE=/path/to/shared_credentials_file

To use a config file, create an INI formatted file like this:

::

   [default]
   aws_access_key_id=<default access key>
   aws_secret_access_key=<default secret key>
   # Optional, to define default region for this profile.
   region=us-west-1

   [profile testing]
   aws_access_key_id=<testing access key>
   aws_secret_access_key=<testing secret key>
   region=us-west-2

and place it in ``~/.aws/config`` (or in ``%UserProfile%\.aws\config``
on Windows). If you wish to place the config file in a different
location than the one specified above, you need to tell the AWS CLI
where to find it. Do this by setting the appropriate environment
variable:

::

   $ export AWS_CONFIG_FILE=/path/to/config_file

As you can see, you can have multiple ``profiles`` defined in both the
shared credentials file and the configuration file. You can then specify
which profile to use by using the ``--profile`` option. If no profile is
specified the ``default`` profile is used.

In the config file, except for the default profile, you **must** prefix
each config section of a profile group with ``profile``. For example, if
you have a profile named "testing" the section header would be
``[profile testing]``.

The final option for credentials is highly recommended if you are using
the AWS CLI on an EC2 instance. `IAM
Roles <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html>`__
are a great way to have credentials installed automatically on your
instance. If you are using IAM Roles, the AWS CLI will find and use them
automatically.

In addition to credentials, a number of other variables can be
configured either with environment variables, configuration file
entries, or both. See the `AWS Tools and SDKs Shared Configuration and
Credentials Reference
Guide <https://docs.aws.amazon.com/credref/latest/refdocs/overview.html>`__
for more information.

For more information about configuration options, please refer to the
`AWS CLI Configuration Variables
topic <http://docs.aws.amazon.com/cli/latest/topic/config-vars.html#cli-aws-help-config-vars>`__.
You can access this topic from the AWS CLI as well by running
``aws help config-vars``.

Basic Commands
~~~~~~~~~~~~~~

An AWS CLI command has the following structure:

::

   $ aws <command> <subcommand> [options and parameters]

For example, to list S3 buckets, the command would be:

::

   $ aws s3 ls

To view help documentation, use one of the following:

::

   $ aws help
   $ aws <command> help
   $ aws <command> <subcommand> help

To get the version of the AWS CLI:

::

   $ aws --version

To turn on debugging output:

::

   $ aws --debug <command> <subcommand>

You can read more information on the `Using the AWS
CLI <https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-using.html>`__
chapter of the AWS CLI User Guide.

Command Completion
~~~~~~~~~~~~~~~~~~

The aws-cli package includes a command completion feature for Unix-like
systems. This feature is not automatically installed so you need to
configure it manually. To learn more, read the `AWS CLI Command
completion
topic <https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-completion.html>`__.

jump2
------------

The best way to interact with our team is through GitHub. You can `open
an issue <https://github.com/aws/aws-cli/issues/new/choose>`__ and
choose from one of our templates for guidance, bug reports, or feature
requests.

You may find help from the community on `Stack
Overflow <https://stackoverflow.com/>`__ with the tag
`aws-cli <https://stackoverflow.com/questions/tagged/aws-cli>`__ or on
the `AWS Discussion Forum for
CLI <https://forums.aws.amazon.com/forum.jspa?forumID=150>`__. If you
have a support plan with `AWS Premium
Support <https://aws.amazon.com/premiumsupport>`__, you can also create
a new support case.

Please check for open similar
`issues <https://github.com/aws/aws-cli/issues/>`__ before opening
another one.

The AWS CLI implements AWS service APIs. For general issues regarding
the services or their limitations, you may find the `Amazon Web Services
Discussion Forums <https://forums.aws.amazon.com/>`__ helpful.

jump3
--------------

-  `Changelog <https://github.com/aws/aws-cli/blob/develop/CHANGELOG.rst>`__
-  `AWS CLI
   Documentation <https://docs.aws.amazon.com/cli/index.html>`__
-  `AWS CLI User
   Guide <https://docs.aws.amazon.com/cli/latest/userguide/>`__
-  `AWS CLI Command
   Reference <https://docs.aws.amazon.com/cli/latest/reference/>`__
-  `Amazon Web Services Discussion
   Forums <https://forums.aws.amazon.com/>`__
-  `AWS Support <https://console.aws.amazon.com/support/home#/>`__

.. |Build Status| image:: https://travis-ci.org/aws/aws-cli.svg?branch=develop
   :target: https://travis-ci.org/aws/aws-cli
.. |Gitter| image:: https://badges.gitter.im/aws/aws-cli.svg
   :target: https://gitter.im/aws/aws-cli
