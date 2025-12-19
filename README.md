# ADENIYI
OOP HMEWORK STAGE 1
1. Sensor Class
The Sensor class represents a physical device used to collect environmental data such as
temperature, air quality, or water quality. It is responsible for identifying the sensor, knowing what
type of data it measures, and producing measurements.
Typical attributes include sensorId, type, unit, and zone. Typical methods include taking a
measurement and returning sensor information.
2. Measurement Class
The Measurement class represents a single data reading collected from a sensor. Each
measurement contains a value, a timestamp, and the ID of the sensor that produced it. Separating
measurements from sensors allows historical data analysis and trend detection.
3. EnvironmentZone Class
The EnvironmentZone class represents a monitored area such as an industrial zone, residential
area, or river basin. It groups sensors and measurements belonging to the same area. It typically
contains a list of sensors and a list of measurements, and methods to add and analyze them.
4. DataLogger Class
The DataLogger class manages data collection and storage. It registers sensors, logs
measurements, and organizes data by zones. This separation improves maintainability and
scalability of the system.
5. AlertSystem Class
The AlertSystem class monitors measurements and generates alerts when values exceed defined
thresholds. It is responsible for environmental safety and early warning notifications.
6. Use of Composition
Composition is used to model “has-a” relationships: EnvironmentZone has sensors and
measurements, Sensor has measurements, DataLogger has zones. This accurately reflects
real-world ownership and lifecycle dependency.
7. Summary of Class Relationships
Sensors generate measurements.
Measurements belong to sensors.
Sensors are grouped into environment zones.
Zones are managed by the data logger.
Alerts are generated based on logged data


STAGE 2
1. Sensor Registration
Sensor registration allows the system to keep track of all sensors deployed in different environment
zones. When a sensor is registered, it is assigned to a specific zone and stored in the DataLogger.
This ensures that every measurement collected can be traced back to its sensor and zone.
2. Measurement Logging
Measurement logging involves recording data readings from sensors over time. Each time a sensor
takes a reading, a Measurement object is created and stored. The DataLogger assigns the
measurement to the appropriate EnvironmentZone based on the sensor’s location.
3. Aggregate Daily Averages per Sensor Zone
This algorithm calculates the average measurement value for each sensor type within a zone for a
given day. Steps include grouping measurements by zone and date, summing the values, and
dividing by the total number of readings. Daily averages help in understanding overall
environmental conditions.
4. Dynamic Min, Max, and Mean Detection
The system continuously tracks minimum, maximum, and mean values as new data arrives. This
avoids reprocessing all past data each time. It improves efficiency and allows real-time monitoring
of environmental changes.
5. Sorting and Viewing Highest Pollution Zones
Zones are sorted based on pollution levels derived from average or peak values. This allows quick
identification of the most affected areas. Sorting can be done in descending order to highlight
critical zones first.
6. Importance of Stage 2
Stage 2 transforms the system from a static design into a working application. It enables meaningful
data analysis and prepares the foundation for alerts and forecasting in Stage 3.
Conclusion
By completing Stage 2, the system can now collect, store, analyze, and rank environmental data
efficiently. This stage bridges system architecture and advanced intelligent features
