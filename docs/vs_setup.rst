XUnit - Disable namespaces in VS Test Explorer
==============================================

In root directory of your test project add a file called "xunit.runner.json".
Right-click the file, properties. Select "Copy if newer" for copy to Output directory.

Then in the file enter this json::

    {
        "methodDisplay": "method"
    }

`As found on StackOverflow <https://stackoverflow.com/questions/32351210/how-can-xunit-be-configured-to-show-just-the-method-name-in-the-visual-studio-20>`_