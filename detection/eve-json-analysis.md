# Structured Log Analysis (eve.json)

Suricata logged detection events to `eve.json`, which served as the authoritative data source for analysis.

Observed fields included:
- Source and destination IPs
- TCP port information
- Flow identifiers
- Application-layer metadata

Threshold-based detection logic resulted in informational classification rather than escalation.
