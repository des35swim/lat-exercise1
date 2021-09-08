# lat-exercise1
Coding challenge from Lat

### Solution
Self contained in a docker container.

### Pre-requisites
You have docker installed

### How to build
To build the container run:
```
docker build -t lat-exercise-1 .
```
### How to run
1. Customise the yesterdays_prices.csv with a comma separated list of yesterdays prices
2. Run command:
```
docker run -v <fully qualified path>/yesterdays_prices.csv:/latitude/yesterdays_prices.csv lat-exercise-1
```
It returns an array with three elements:
  ```[<buyTime>, <sellTime>, <profit>]```

### How to test
The container also contains a suite of unit tests.  If I had more time I wouldn't bundle them in a separate container.
```
docker run lat-exercise-1 /latitude/testit.sh
```
