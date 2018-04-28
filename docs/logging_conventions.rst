Logging Conventions
===================

* https://github.com/dapplo/Dapplo.Log should be used in class
    * Install-Package Dapplo.Log
* Finally it should be wrapped up by NLog https://github.com/NLog/NLog
* Log messages should be in english language

Using Loglevel
--------------

In most projects there will be no direct requirements concerning log level.
Therfor we shall follow this guidelines published by Microsoft:

* https://docs.microsoft.com/en-us/aspnet/core/fundamentals/logging/?view=aspnetcore-2.1&tabs=aspnetcore2x#log-level
* https://docs.microsoft.com/en-us/dotnet/api/microsoft.extensions.logging.loglevel?view=aspnetcore-2.0

ASP.NET Core defines the following log levels, ordered here from least to highest severity.

Trace = 0
^^^^^^^^^^

For information that's valuable only to a developer debugging an issue. These messages may contain sensitive application data and so shouldn't be enabled in a production environment. Disabled by default. Example: Credentials: {"User":"someuser", "Password":"P@ssword"}

Debug = 1
^^^^^^^^^^

For information that has short-term usefulness during development and debugging. Example: Entering method Configure with flag set to true. You typically wouldn't enable Debug level logs in production unless you are troubleshooting, due to the high volume of logs.

Information = 2
^^^^^^^^^^^^^^^

For tracking the general flow of the application. These logs typically have some long-term value. Example: Request received for path /api/todo

Warning = 3
^^^^^^^^^^^

For abnormal or unexpected events in the application flow. These may include errors or other conditions that don't cause the application to stop, but which may need to be investigated. Handled exceptions are a common place to use the Warning log level. Example: FileNotFoundException for file quotes.txt.

Error = 4
^^^^^^^^^^

For errors and exceptions that cannot be handled. These messages indicate a failure in the current activity or operation (such as the current HTTP request), not an application-wide failure. Example log message: Cannot insert record due to duplicate key violation.

Critical = 5
^^^^^^^^^^^^

For failures that require immediate attention. Examples: data loss scenarios, out of disk space.


