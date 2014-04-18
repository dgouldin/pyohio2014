# Introduction
 * What is Celery?
 * When would I want to use it?

# Architecture of a Celery applicaiton
 * Architecture diagram
 * Message brokers
 * Worker pools
 * Advanced features
   * Multiple queues
   * Gevent workers

# Tasks
 * Decorator approach
 * Class-based approach
 * Best practices
   * Idempotent
   * Atomic
   * Simple arguments
     * (Reference Alex Gaynor pickle PyCon talk)
   * Versioning / migration of tasks

# Putting it all together
 * Setting up a Celery app
 * Running a broker
 * Starting a worker pool
 * Hello world! (CAUTION: LIVE DEMO)

# Celery <3 Django
 * Celery-specific Django settings
 * Management commands
 * Django view Celery example

# Logging
 * Standard Python logging library
 * Django settings based logging

# Testing
 * ALWAYS_EAGER
 * Integration testing

# Debugging
 * rdb
 * When in doubt, add more logging!
