# housecalm-wazuh-resources

Curated collection of GitHub repositories useful for optimizing HouseCalm's Wazuh environment and related cyber tasks (endpoint monitoring, detection rules, validation, plain-English reporting).

HouseCalm is a quiet watch for household computers that uses Wazuh as the underlying open-source watcher. These repos help with better detections, software inventory, validation of alerts, and complementary tools.

## Core Wazuh / Endpoint Monitoring
- [wazuh/wazuh](https://github.com/wazuh/wazuh) — Main platform: agents for software inventory/vuln detection, log analysis (logins, Defender), FIM, malware checks, config assessment.
- [wazuh/wazuh-docker](https://github.com/wazuh/wazuh-docker) — Easy deployment of the manager.
- [socfortress/Wazuh-Rules](https://github.com/socfortress/Wazuh-Rules) — Advanced, higher-quality rules (Sysmon, Defender, Osquery, etc.).
- [BeardedTinker/wazuh-homelab-security](https://github.com/BeardedTinker/wazuh-homelab-security) — Practical rules/decoders for home environments (UniFi, Synology, Home Assistant).
- [heraclescap/wazuh-custom-dashboards](https://github.com/heraclescap/wazuh-custom-dashboards) — Dashboards for software hygiene and vulnerability panorama (great for letter content).
- [sankaHQ/monitor](https://github.com/sankaHQ/monitor) — Lightweight local scanner for out-of-support software and security settings.

## Complementary Visibility & Detection
- [osquery/osquery](https://github.com/osquery/osquery) — SQL-powered endpoint querying; integrates with Wazuh.
- [Velocidex/velociraptor](https://github.com/Velocidex/velociraptor) — Deeper host collection and forensics (VQL).
- [SigmaHQ/sigma](https://github.com/SigmaHQ/sigma) — Generic detection rules (convertible to Wazuh).
- [crowdsecurity/crowdsec](https://github.com/crowdsecurity/crowdsec) — Behavior detection + community IP reputation.

## Validation / Purple Team (defensive use of offensive tools)
- [redcanaryco/atomic-red-team](https://github.com/redcanaryco/atomic-red-team) — Portable MITRE ATT&CK technique tests to validate detections.

## Optimization ideas for HouseCalm Wazuh
1. Deploy or enhance custom rules from socfortress and BeardedTinker focused on household signals (outdated software, odd logins, Defender events, FIM for key paths).
2. Use software inventory + vulnerability detection output to generate plain-English “what to do this week” letters.
3. Integrate osquery for richer inventory and ad-hoc checks.
4. Validate detections with Atomic Red Team in a lab environment.
5. Consider custom dashboards or alert enrichment (e.g., local LLM summaries) for non-technical output.
6. Review active response carefully — HouseCalm monitors/alerts; it does not stop attacks.

Starred or referenced for easy access. Fork and adapt rules as needed for your stack.
