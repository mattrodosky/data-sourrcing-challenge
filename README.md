# data-sourrcing-challenge
CME and GST Data Processing

Overview

This project retrieves, processes, and analyzes Coronal Mass Ejections (CMEs) and Geomagnetic Storms (GSTs) using data from NASA's DONKI API. The workflow includes fetching data, cleaning and transforming it, merging datasets, computing time differences, and exporting the final results.

Data Retrieval

The script fetches:

CME Data from https://api.nasa.gov/DONKI/CME

GST Data from https://api.nasa.gov/DONKI/GST

Data Processing Steps

Retrieve CME and GST Data via API requests.

Convert API response to JSON and store it in Pandas DataFrames.

Filter necessary columns (activityID, startTime, linkedEvents).

Expand linkedEvents to ensure each row represents a single event.

Extract activityID from linkedEvents.

Convert date columns to datetime format to enable calculations.

Merge CME and GST DataFrames based on their relationships.

Compute the time difference (timeDiff) between CME and GST occurrences.

Export final dataset to CSV for further analysis.

Key Features

Uses pandas for data transformation.

Handles missing data and ensures only relevant events are processed.

Computes time difference between CME and GST events.

Exports clean data for further analysis.

Requirements

Python 3

requests

pandas

json

NASA API Key (stored in an environment variable)