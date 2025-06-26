# System Verification Report - SatAlphaV2

**Date:** 26/06/2025
**Version:** 2

## 1. System Configuration Summary

- **System ID:** SatAlphaV2
- **Description:** Satellite configuration for SatAlpha, Version 2
- **Components List:**
    - CommAntenna001 (ANT001): 1 unit(s) at 20.0 kg/unit
    - CommAntenna002 (ANT002): 1 unit(s) at 20.0 kg/unit
    - SolarPanel_A (SP001A): 1 unit(s) at 75.2 kg/unit
    - SolarPanel_B (SP001B): 1 unit(s) at 75.2 kg/unit
    - MainThruster001 (T001): 1 unit(s) at 165.0 kg/unit
- **Calculated Total Mass:** 355.4 kg

## 2. Requirements Verification

| Requirement ID | Description | Parameter | Constraint | Actual | Value | Unit | Status |
|------------------------|-------------------|-----------------|----------------|-----------|----------|---------|-----------|
| REQ001 | Total system mass for system configuration must be acceptable | calculated_total_mass_kg | <=360 | 355.4 | kg | SATISFIED | 
| REQ002 | Maximum individual component mass | component_mass_max | <=200 | 165.0 | kg | SATISFIED | 

## 3. Conclusion

All checked requirements for the SatAlphaV2 system configuration have been **SATISFIED** based on the current data in system_config.json, and requirements.csv.