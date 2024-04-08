# Prolog Flight PLanner
 I am making a project using Prolog. The application domain for this project will be researching airline flights from and to various airports. 

# Airline Flights Prolog Program

This Prolog program models airline flights between various airports. It includes facts about flights and rules to answer specific questions about the flights.

## Facts about Flights

- `flight(6711, bos, ord, 815, 1005).`
- `flight(211, lga, ord, 700, 830).`
- `flight(203, lga, lax, 730, 1335).`
- `flight(92221, ewr, ord, 800, 920).`
- `flight(2134, ord, sfo, 930, 1345).`
- `flight(954, phx, dfw, 1655, 1800).`
- `flight(1176, sfo, lax, 1430, 1545).`
- `flight(205, lax, lga, 1630, 2210).`
- `flight(111, lga, bos, 645, 745).`
- `flight(222, bos, ewr, 750, 845).`

## Questions and Queries

### 1. Where does the flight from PHX go?
- **Question:** Where does the flight from PHX go?
- **Query:** `?- destinations_from(phx, Destinations).`
- **Result:** `Destinations = [dfw]`

### 2. Is there a flight to PHX?
- **Question:** Is there a flight to PHX?
- **Query:** `?- flight_to(phx).`
- **Result:** `false`

### 3. What time does the flight from BOS land?
- **Question:** What time does the flight from BOS land?
- **Query:** `?- arrival_time(bos, ArrivalTime).`
- **Result:** `ArrivalTime = 1005` or `ArrivalTime = 845`

### 4. Does the flight from ORD to SFO depart after the flight from EWR to ORD lands?
- **Question:** Does the flight from ORD to SFO depart after the flight from EWR to ORD lands?
- **Query:** `?- departs_after(2134, 92221).`
- **Result:** `true`

### 5. What time do the flights to ORD arrive?
- **Question:** What time do the flights to ORD arrive?
- **Query:** `?- arrival_times_to(ord, ArrivalTimes).`
- **Result:** `ArrivalTimes = [1005, 830, 920]`

### 6. What are all the ways to get from LGA to LAX?
- **Question:** What are all the ways to get from LGA to LAX?
- **Query:** `?- route(lga, lax, Route).`
- **Result:** Multiple routes displayed

