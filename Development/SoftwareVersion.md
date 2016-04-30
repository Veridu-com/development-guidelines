# Software Version
All server fleet run in the same operating system version, thus dev/prod environment share the same standard package versions.

The current OS is Ubuntu 14.04 LTS (Long Term Support, supported until 2019) and most daemons/software in use are based on standard packages.

## Exceptions

- nginx: all router/application servers run mainline version based on nginx.org's package
- php: all worker servers run the latest 5.6 branch with pthreads enabled
