# System Verification Report - SatAlphaV0

**Date:** 26/06/2025
**Version:** 0

## 1. System Configuration Summary

- **System ID:** SatAlphaV0
- **Description:** Satellite configuration for SatAlpha, Version 0
- **Components List:**
- **Calculated Total Mass:** 0 kg

## 2. Requirements Verification

| Requirement ID | Description | Parameter | Constraint | Actual | Value | Unit | Status |
|------------------------|-------------------|-----------------|----------------|-----------|----------|---------|-----------|
| REQ001 | Total system mass for system configuration must be acceptable | calculated_total_mass_kg | <=350 |  | kg | SATISFIED | 
| REQ002 | Maximum individual component mass | component_mass_max | <=200 |  | kg | SATISFIED | 

## 3. Conclusion

All checked requirements for the SatAlphaV0 system configuration have been **SATISFIED** based on the current data in system_config.json, and requirements.csv.