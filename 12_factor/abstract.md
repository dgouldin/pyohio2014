# Twelve-Factor Apps
 * Use declarative formats
 * Have a clean contract with the underlying OS
 * Are deployable on cloud platforms
 * Minimize differences between environments
 * Scale up without any significant changes

# The Twelve Factors

1. Codebase
 * One codebase tracked in revision control, many deploys.
 * If there are multiple codebases, it’s not an  app – it’s a distributed
   system.

2. Dependencies
 * Explicitly declare and isolate dependencies.
 * A twelve-factor app never relies on implicit existence of system-wide
   packages.
 * Do not rely on the implicit existence of any system tools.
 * pip + virtualenv + requirements.txt

3. Config
 * Store conﬁg in the environment.
 * Resource handles to the database, Memcached, and other backing services.
 * Per-deploy values such as the canonical hostname for the deploy.
 * Django & Flask make this simple.

4. Backing Services
 * Treat backing services as attached resources.
 * Make no distinction between local and third party services.

5. Build, Release, Run
 * Strictly separate build and run stages.
 * It is impossible to make changes to the code at runtime.
 * This allows for rollbacks and other release management suites.

6. Processes
 * Execute the app as one or more stateless processes.
 * `$ python app.py`
 * A production deploy of a sophisticated app may use many process types,
   instantiated into zero or more running processes.

7. Port Binding
 * Export services via port binding.
 * The web app exports HTTP as a service by binding to a port, and listening to
   requests coming in on that port.
 * Gunicorn, Gevent, Eventlet.

8. Concurrency
 * Scale out via the process model.
 * Using this model, the developer can architect their app to handle diverse
   workloads by assigning each type of work to a process type.
 * Rely on the operating system's process manager.

9. Disposability
 * Maximize robustness with fast startup and graceful shutdown.
 * They can be started or stopped a moment’s notice.

10. Dev/Prod Parity
 * Keep development, staging, and production as similar as possible.
 * Failing to do so increases: the time gap, personnel gap, and the tools gap.

11. Logs
 * Treat logs as event streams.
 * Apps never concern themselves with routing or storage of the output stream.

12. Admin Processes
 * Run admin/management tasks as one-off processes in an identical environment.
 * Run against a release, using the same code and conﬁg as any process run
   against that release.
 * `$ manage.py syncdb`
