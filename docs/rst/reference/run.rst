run
===

.. program:: ansible-container run

The ``ansible-container run`` command launches the container orchestrator and runs
the built containers with the configuration found in ``container.yml``. For docker
deploys, this is roughly analogous to ``docker-compose run``.

.. option:: --production

By default, any `dev_overrides` specified in ``container.yml`` will be used and included in the orchestration playbook. Use this flag to ignore `dev_overrides`, and run containers using the production configuration.

.. option:: --remove-orphans

Remove containers for services not defined in ``container.yml``.

.. option:: --roles-path ROLES_PATH

If using roles not found in the ``roles`` directory within the project, use this option to specify the local path containing the roles. The specified path will be mounted to the conductor container, making the roles available.

.. option:: --with-variables WITH_VARIABLES [WITH_VARIABLES ...]

Define one or more environment variables in the Conductor container. Format each variable as a key=value string.

.. option:: --with-volumes WITH_VOLUMES [WITH_VOLUMES ...]

Mount one or more volumes to the Conductor container. Specify volumes as strings using the Docker volume format.
