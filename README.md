# Simulator-Program
A program that simulates the minute-by-minute operation of a checkout line, such as one you might find in a retail store

Customers arrive at the checkout line and stand in line until the cashier is free.
When they reach the front of the line, they occupy the cashier for some period of time (referred to as ServiceTime) measured in minutes.
After the cashier is free, the next customer is served immediately.
Customers arrive at the checkout line at ArrivalRate per minute. Use the function included below (randomChance()) to return the number of customers arriving in a given minute, determined randomly.
The line can only hold so many people, MaxLineSize, until new arriving customers get frustrated and leave the store without purchasing anything.
ServiceTime is determined at the point the customer reaches the cashier, and should be taken from the random interval MinServiceTime and MaxServiceTime -- use the function randomInt() provided.
The overall time of the simulation is SimulationTime, measured in minutes.
The program should take 6 inputs (to be read from a text file named simulation.txt, as numbers only, one per line, in this order):

SimulationTime - total number of minutes to run the simulation (whole number).
ArrivalRate - per-minute arrival rate of customers (a floating point number greater than 0 and less than 1). This number is the "percent chance" that a customer will arrive in a given minute. For example, if it is 0.4, there is a 40% chance a customer will arrive in that minute.
MinServiceTime - the minimum expected service time, in minutes (whole number).
MaxServiceTime - the maximum expected service time, in minutes (whole number).
MaxLineSize - the maximum size of the line. If a new customer arrives and the line has this many customers waiting, the new customer leaves the store unserviced.
TargetWaitingTime - the customer service target for all customers. Use this to keep track of the number of customers who were serviced within the target time.
At the end of each simulation, the program should output:

The total number of customers serviced
The total number of customers who found the line too long and left the store.
The average time per customer spent in line
The average number of customers in line
The percentage of customers served within TargetWaitingTime (how many customers had to wait TargetWaitingTime or less, divided by the number of customers served, ignoring customers who left).
You are free to use any STL templates as needed (queue, vector, etc.).

