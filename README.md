# ADENIYI
OOP HMEWORK
Stage 1: Architecture
Classes:
1. Sensor
• Attributes: sensor_id, sensor_type, zone, status
• Methods: read_value(), get_info()
2. Measurement
• Attributes: sensor, value, timestamp
3. EnvironmentZone
• Attributes: zone_id, sensors, measurements
• Methods: register_sensor(), add_measurement(), get_daily_average(),
get_min_max_mean(), sort_measurements()
4. DataLogger
• Attributes: zones, log
• Methods: add_zone(), register_sensor(), record(), get_zone_reports()
5. AlertSystem
• Attributes: thresholds, alerts
• Methods: generate_threshold_alert(), moving_average(), predict_next_value(
