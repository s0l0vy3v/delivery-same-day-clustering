# delivery-same-day-clustering
Easy clustering model which calculates number of couriers delivery service needs to perform all the deliveries on the same-day using historical data

## Short intro
This code was written in order to launch same-day delivery for delivery clients. Originally it was using retro-data of usual deliveries but the main idea is that future deliveries will be distributed the same. The logic is simple: 
1) I calculated courier speed, km and hours from one to next point from retro-data.
2) Then I've set all the parameters like courier workday, minute costs, etc. 
3) At this step clustering of all the retro-data deliveries begins followed by randomizing the same number of deliveries around cluster centers.
4) After which I've calculated how many couriers company will need to deliver all the orders if the routes would be prepared only a day before.
5) It all ends with calculating how much money is spent for 1 delivery and how courier performance historically could change.

## Usage
Currently model needs two datasets: a) deliveries data (containing dates, addresses and clients' ids) b) courier data (containing start/end timestamps of deliveries and employees' ids).
Also, during the step II you are to set:
- Courier's workday start & end;
- Number of delivery hub visits & its frequency;
- Cost of courier's minute.

## Credits
[s0l0vy3v](https://github.com/s0l0vy3v)
