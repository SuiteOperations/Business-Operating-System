## Operational Concepts 

### Internal Customers

One of my favorite concepts is that of the internal customer.

An internal customer is someone within the organization that comes after you in a process or flow. They are the direct "customer" of your job.

Everyone at the company should approach internal customer satisfaction like external customers. Speak with internal customers to see what they need, what they want, and on what criteria they judge your outputs. Understand their frustrations and consider what you might innovate in order to alleviate these frustrations. How can you make their job easier? Get inside the head of your internal customer's similar to how a product manager might try to get inside the head of potential external customers. Understand their pains and what benefits would be attractive to them. If one person does this, they can become overloaded. If everyone does it, you end up with a streamlined culture of excellence in operations.

### Working Backwards

When streamlining operations, I have always found it helpful to work backwards. 

1. What is the ideal state?
2. What are the individual components needed for that ideal state?
3. Where are they created or stored?
4. How can we capture and maintain those components until we need them?
5. How do we make them available for use when needed?

By working backwards, you start with an ideal, and create only steps that are needed to accomplish that ideal state.

An example of this was when I was involved in streamlining our internal demand planning process.

It always took hours to collect and analyze all the data to figure out what we needed to order, and what we needed to transfer. By working backward, we were able to turn this into a an almost automated process.

Until the below process, was created a planner would have to request inventory numbers from each division, calculate usage, and make a list of open orders that were outstanding. They would usually have to check on important orders to see when they were going to be shipped. Finally, a large number of calculations were done to figure out what needed to be ordered.

This was then passed to a buyer who would look up the approved supplier for a part and get the part on order.

#### Ideal State

The ideal state for demand planning is to end up with actions which will result in all customers supplied with parts, without overstocking our own inventory.

#### Individual Components

In order to accomplish this, we need to understand what we have, how long it will last, and how we get more of it. This creates the following components in order to calculate the proper orders:

* List of parts
* Part supplier
* Part lead-time
* Inventory for each part in each location
* Usage for each part in each location
* Open purchase orders for all parts

Many demand plans will look at inventory and usage. However, the end goal for the internal customer is "What orders need to be placed?", not "What parts need to be ordered?". By approaching the problem with an internal customer mindset, we know that once a buyer knows what needst to be ordered, they need to figure out the where and when (supplier and order dates). Why not alleviate this frustration and make it part of the deman planning? We are looking for internal customer service and satisfaction as much as external.

#### Data Creation and Capture

Understanding how to capture data at the point of creation is a huge leverage point for streamlining operations. This is especially true if you can do this without interupting the doing of an activity (even better if you can streamline in the process).

* The list of parts should be stored somewhere in company systems. At worst, you can export a sales history, remove duplicates, and obtain a list of parts sold... a catalog so to speak.
* Parts suppliers can be obtained from purchase history. Grab a history of all purchase orders, and remove duplicate item entries to see where you order each item from.
* Lead time is a bit trickier. If you track this, then great. Otherwise, here are some ideas:
  * Take the date the item was received and subtract the date the Purchase Order was created.
  * Assume all suppliers have set leadtime.
  * Calculate distance using zip codes from your facility to a supplier facility and create a lead-time based on distance.

* Cycle counts are done each quarter at each facility. We built a small application that was basically a digital interface of the sheets they used to count by hand each quarter. This sheet than auto subracted any shipments and gave us a rough, real-time idea of inventory at each locations.
* Using the same shipment data, we could calculate usage.
* Each time we send an order, we created an auto link which would ask the supplier to enter when they expect an order to be delivered. This fullfilled our lead-time, as well as open order data point.

#### Available

Finally, we set scripts to grab part lists, sales history, and purchase history, and auto create the lists for parts and suppliers. We also had an export for the inventory and usage application we built. All open Purchase Order responses were auto saved to another file.

Last, we set a timed script to pull, combine, and do our calculations on what needed to be ordered, and from whom. 

#### Results

The result was a nearly automated process with continually updated demand plans full of the exact actions needed.

> "Order this part from that supplier on this day"

The process is quite intuitive when followed from a *working backward* framework. Using this approach will create streamlined processes, as well as change how you caputure and utilize data for company use. Consider the time saved by moving cycle counts to a digital platform accessable by anyone. Because we moved it to a digital process, we actually made cycle counts easier by using scanners instead of manual counts. We made it more accurate, more available, and real-time by using shipment modifications. 

Working backwards from an ideal state, and noting what you need for that ideal state and where you can get it easily will reduce administrative burden and increase accuracy throughout the firm.