# cashier-system
The Cashier System is a ROS-based application that emulates a cashier process. It comprises three nodes: ```publisher```, ```subscriber```, and ```printer```. Each node has a specific responsibility within the system.

# Nodes

## Publisher Node
The ```publisher``` node is responsible for publishing bill messages to ```bill_topic```. It generates and sends bill information to other nodes, allowing them to update the inventory and income accordingly.
## Subscriber Node
The ```subscriber``` node plays a crucial role in the Cashier System. It subscribes to the ```bil_topic``` published by the publisher_node and processes them. Upon receiving a bill message, the subscriber_node updates the inventory, keeping track of the items sold, and adjusts the income accordingly.
## Printer Node
Lastly, the ```printer``` node handles the printing tasks in the system. It receives the last bill message from the ```subscriber``` node and prints it. Additionally, the ```printer``` node provides up-to-date information about the current inventory and income, ensuring that the cashier process is accurately documented.
## ROS Services and ROS Parameters
Inventory and Income are ROS parameters stored on the rosparameter server.
A ROS service must be called from the ```subsciber``` node to update these parameters.

Together, these three nodes work collaboratively to simulate a cashier system within the ROS framework. By leveraging the capabilities of each node, the system successfully handles bill publishing, inventory tracking, income management, and printing functionalities.

# RQT GRAPH
![Screenshot from 2023-06-17 18-14-26](https://github.com/nimbusmustafa/cashier-system/assets/117943931/c4612ed5-e337-4aa1-b299-e5f893ca7989)
# YouTube link
https://youtu.be/tQI-d4NKqPI
