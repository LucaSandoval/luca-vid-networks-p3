high-level approach:

Using the starter code as a jumping off point, we implement a main method that processed the various types of messages. Each message type
has a case in the main switch statement that executes its custom logic. Our program keeps track of all recieved route updates, and rebuilds
its forwarding table each time a new update or withdraw message is recieved.

challenges you faced:

The many features and nuances of said features proved a large task to understand. It took us a long time to read through the instructions
and formulate a plan. The most difficult challenge we faced was debugging the route aggregation code, which ended up being a simple fix
at the end of the day.

properties/features of your design:

The logic for breaking ties between routes in our program we feel is particularly good. It uses a method of sorting routes in a pool
of route options by a specific paremeter (selfOrigin or localPref for example), where the routes are kept in dictonary using that parameter
as a key. Then, we sort them and check how many entries fall under the 'highest' or 'preffered' key. If there is only one, its the best route
and is returned. Otherwise, we work on that reduced group for the next round of criteria.

overview of how you tested:

Testing was greatly aided with the provided test suite and config libraries. Using the output from the tests to the console and cross-referencing it
with the expected output we were able to debug efficiently.
