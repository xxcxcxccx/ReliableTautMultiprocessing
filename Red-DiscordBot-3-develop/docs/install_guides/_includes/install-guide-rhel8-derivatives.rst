.. include:: _includes/supported-arch-x64+aarch64.rst

.. include:: _includes/linux-preamble.rst

-------------------------------
Installing the pre-requirements
-------------------------------

Red Hat Enterprise Linux (RHEL) 8.6-8.x and its derivatives have all required packages available in official repositories.
Install them with dnf:

.. TODO: Use Python 3.11 once RHEL 8.6 goes EOL in 2024.

.. prompt:: bash

    sudo dnf -y update
    sudo dnf -y group install development
    sudo dnf -y install python39 python39-devel java-17-openjdk-headless nano git

Set ``java`` executable to point to Java 17:

.. prompt:: bash

    sudo alternatives --set java "java-17-openjdk.$(uname -i)"

.. Include common instructions:

.. include:: _includes/create-env-with-venv3.9.rst

.. include:: _includes/install-and-setup-red-unix.rst
