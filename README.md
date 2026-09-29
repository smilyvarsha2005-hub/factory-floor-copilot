# 🏭 AI Factory Floor Co-Pilot

An intelligent factory-floor assistant designed to help technicians diagnose machine anomalies using current machine data, sensor readings, incident history, and maintenance knowledge.

## 🎯 Problem

Factory technicians often depend on scattered maintenance records and personal experience when diagnosing machine problems.

A machine may show an abnormal sensor value, but the correct solution can depend on:

- Machine model
- Previous incidents
- Maintenance history
- Technician observations
- Historical machine-specific knowledge

This can lead to incorrect initial diagnoses and longer machine downtime.

## 💡 Solution

AI Factory Floor Co-Pilot brings factory data into one place and provides a foundation for AI-assisted troubleshooting.

The system combines:

- 🏭 Machine information
- 🌡️ Sensor readings
- 🚨 Incident history
- 🔧 Maintenance records
- 👨‍🔧 Technician information
- 🧠 Historical troubleshooting knowledge
- 🤖 AI reasoning layer

## 🔥 Demo Scenario

### PRESS-2018

The hydraulic press currently reports:

- Vibration: **8.4 mm/s**
- Temperature: **72°C**
- Humidity: **68%**
- Status: **WARNING**

The system also contains historical information showing that a previous high-vibration incident was initially suspected to be a calibration problem.

However, the technician discovered that:

> The residue trap was clogged.

After cleaning the residue trap, vibration returned to **3.1 mm/s**.

This historical knowledge can help prevent the same incorrect diagnosis in the future.

## 🏗️ Architecture

```text
Factory Floor
     │
     ├── Machines
     ├── Sensors
     └── Technicians
           │
           ▼
     Spring Boot REST API
           │
     ┌─────┴─────────┐
     │               │
     ▼               ▼
   MySQL        AI Memory Layer
     │               │
     └───────┬───────┘
             ▼
        AI Reasoning
             │
             ▼
       Web Dashboard
