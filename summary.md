Lab-Logging Answer:
Part 1:
1/ Discussion: Why is logging important in backend systems?
Answer: By capturing and analyzing critical data points, logging and monitoring enable developers and operations teams to gain insights into system behavior, detect anomalies, and respond proactively to potential issues.

2/ Research:
We have 6 levels of logging commonly used in software development:
_TRACE is the most detailed log level, used to track what's happening at a very granular level. It’s great for troubleshooting tough bugs or analyzing specific system behavior.
_DEBUG provides detailed info for debugging but isn’t as detailed as TRACE. It’s perfect for getting insights into things like variable values, method calls, and the internal state of the app.
_INFO logs give you general information about the app’s operation, like successful database connections or completed processes. They help keep track of things but don’t indicate any issues.
_WARN logs are there to flag things that might not be ideal but aren’t causing immediate issues. They often point to something that could become a problem later or that needs attention.
_ERROR logs mean something went wrong, and the system couldn’t do what it was supposed to. These logs typically point to problems that impact the app's performance or functionality.
_FATAL logs are the most severe. They indicate a major failure that’s causing the app to crash or stop working. These are the issues where things are broken beyond repair and immediate action is needed.

Part 2:
4/ Observation:
_console.log displays only the ID of the order, no matter what was inside.
_console.info generates details about the items in the order, including their name, price, and quantity.
_console.warn displays a warning message when the quantity is too large.
_console.error displays an error message when the price is lower than 0.
_console.debug displays a message, but it won’t show in the browser by default.

5/ Discussion:
Console logs are often left in production code unintentionally, which can lead to security risks and performance issues. Logger services are designed to be production-ready, with features like log rotation and compression.

Part 3:
4/ Observation:
With the Winston dependencies, it is easier, safer, and more helpful to debug. The data doesn’t go to the browser or become visible to any person browsing the page. It’s also in JSON format, stored on the server, and includes timestamps so we know exactly when those logs were made.
Also, the JSON format shows us first the log type, then the message, and finally the timestamp.
We have two types of log files: the combined log file where every log message is stored regardless of its type, and another file that stores only error messages—making it easier to debug those errors.

