# Deploy

Deploys will only happen on the second Thursday of the current sprint.

The deploy process itself is automated based on a few simple steps:

- Clone project's upstream repository
- Remove `.git` folder (search for `git as deployment tool`)
- Install project dependencies
- Change folders and files ownership according to system setup
- Sync execution path with clone path
- Restart daemons if needed

When working on a project, there are a few moving parts that require more attention and have different requirements.

- Front-end: Front-end changes usually require support from back-end systems, as such, follow coding style and standards when creating new endpoints/controllers, making sure new changes are done in the right place and fit within context
- Back-end: Back-end systems integrate with multiple daemons, such as `PostgreSQL`, `redis`, `memcached`, `MongoDB`, `Gearman` and so on, so make sure that any changes made don't affect current sub-systems.
- Workers: Worker daemons rely heavily on `Gearman` and `supervisord` to receive tasks and to be executed, so make sure to test properly your daemons with both services. It's also a recommended practice to output errors and status messages to stderr/stdout respectively, making it easier to debug workers.

## Side notes

- Remember to check if your isn't using any resources (e.g. tables) that aren't available in the production environment.
- If you need to add new resources (e.g. tables) to the production environment, make sure you've provided clear instructions on how to add it.
