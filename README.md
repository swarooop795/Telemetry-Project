# Telemetry Data Format Converter

## Overview
This project converts two different telemetry JSON formats into a single unified format using Python.

The program reads:
- `data-1.json`
- `data-2.json`

and converts both into the structure defined in:
- `data-result.json`

---

## Features
- Converts telemetry data from two different formats
- Handles nested JSON objects
- Converts ISO 8601 timestamps into milliseconds since epoch
- Uses Python `unittest` for automated testing

---

## Implementation

### Format 1 Conversion
- Splits the `location` string using `/`
- Maps:
  - `operationStatus` → `status`
  - `temp` → `temperature`

### Format 2 Conversion
- Extracts nested device details
- Converts ISO timestamp format using `datetime.strptime()`
- Converts timestamp into milliseconds

---

## Technologies Used
- Python 3
- JSON
- datetime module
- unittest module

---

## How to Run

```bash
python main.py




