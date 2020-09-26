======
KubePI
======

KubePI CLI for easier k1s setup on Raspberry PIs. See `k1s on GitHub <https://github.com/nushkovg/k1s>`_.

Description
===========

KubePI is a custom tool for making the k1s management easier for the K3D setup, 
dependencies, submodules, and more. It needs at least Python 3.7. Please check 
that you have Python 3.7 or later by running:

.. code-block:: bash

    # Raspberry Pi OS (Raspbian) users
    python3 --version
    # Arch users
    python --version


If you are not running Python 3.7 or later, please upgrade your Python version.

Follow these steps to install `kubepi` by using `pip`:

.. code-block:: bash

    # Raspberry Pi OS (Raspbian) still shipping python2 by default
    pip3 install kubepi
    # Arch shipping python3 by default
    pip install kubepi


Now you should have the `kubepi` command in your path and you can run `kubepi` to display the help:

.. code-block:: bash

    pi@k1s:~$ kubepi
    Usage: kubepi [OPTIONS] COMMAND [ARGS]...

    KubePI CLI for easier k1s setup on Raspberry PIs.

    Options:
    --kube-context TEXT  The kubernetes context to use
    -v, --verbosity LVL  Either CRITICAL, ERROR, WARNING, INFO or DEBUG
    --help               Show this message and exit.

    Commands:
    apps       App commands
    k3d        Manage k3d clusters
    platform   Platform commands
    preflight  Preflight checks
    setup      Setup infrastructure services


To see the options of each command, just run:

.. code-block:: bash

    kubepi <COMMAND> --help

For example:

.. code-block:: bash

    pi@k1s:~$ kubepi k3d --help
    Usage: kubepi k3d [OPTIONS] COMMAND [ARGS]...

    Manage k3d clusters. The name of the cluster is taken from the option
    --kube-context which defaults to 'k1s'

    Options:
    --help  Show this message and exit.

    Commands:
    create  Create cluster
    delete  Delete cluster
    start   Start cluster
    status  Cluster status
    stop    Stop cluster
