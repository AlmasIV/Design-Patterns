# Singleton Pattern

The Singleton creational pattern makes sure that you can initialize only one instance of your class. You can use it in these cases:

* When you need to control actions across your system using one single point of access. Logging, or connection pooling are good examples of this case.
* When you need to share resources like file system, or network connection.
* When you want to prevent multiple instantiations.

This pattern also violates the SRP principle, because the class itself must to make sure that it has only one instance, at the same time the class needs to do its primary job.
