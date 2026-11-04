# housecalm-wazuh-resources

Curated collection of GitHub repositories useful for optimizing HouseCalm's Wazuh environment and related cyber tasks (endpoint monitoring, detection rules, validation, plain-English reporting, attack surface management).

HouseCalm is a quiet watch for household computers that uses Wazuh as the underlying open-source watcher. These repos help with better detections, software inventory, validation of alerts, complementary tools, and external attack surface awareness.

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
- [apache/caldera](https://github.com/apache/caldera) — Automated adversary emulation platform based on MITRE ATT&CK. Run controlled tests and check what Wazuh detects.
- [BishopFox/sliver](https://github.com/BishopFox/sliver) — Modern open-source C2 / adversary emulation framework (mTLS, HTTP, DNS, WireGuard). Useful in a lab for generating realistic endpoint signals.

## Attack Surface Management / External Discovery
- [owasp-amass/amass](https://github.com/owasp-amass/amass) — In-depth attack surface mapping and external asset discovery (passive + active). Ideal for mapping domains, subdomains, and related cloud assets.
- [projectdiscovery/nuclei](https://github.com/projectdiscovery/nuclei) — Fast, template-based vulnerability scanner with a large community library. Chain with other PD tools for lightweight external checks.
- [projectdiscovery/subfinder](https://github.com/projectdiscovery/subfinder) — Fast passive subdomain enumeration. Entry point for the ProjectDiscovery recon chain.
- [yogeshojha/rengine](https://github.com/yogeshojha/rengine) — Self-hosted GUI-based ASM platform that orchestrates Subfinder, httpx, naabu, Nuclei, and more. Continuous monitoring and correlation.
- [1N3/Sn1per](https://github.com/1N3/Sn1per) — All-in-one automated reconnaissance and attack surface management platform (Community Edition free).

## Vulnerability Scanning Complements
- [aquasecurity/trivy](https://github.com/aquasecurity/trivy) — Comprehensive scanner for containers, filesystems, IaC, secrets, licenses, and Kubernetes. Complements Wazuh inventory and vuln detection.
- [anchore/grype](https://github.com/anchore/grype) — Focused vulnerability scanner for container images and filesystems with EPSS/KEV risk scoring. Pairs well with Syft for SBOMs.

## Other Lightweight Helpers
- [zaproxy/zaproxy](https://github.com/zaproxy/zaproxy) — OWASP ZAP for web application testing if you have personal sites or APIs.
- [CISOfy/lynis](https://github.com/CISOfy/lynis) — Simple Linux hardening audit tool for household servers or EC2 instances.

## Optimization ideas for HouseCalm Wazuh
1. Deploy or enhance custom rules from socfortress and BeardedTinker focused on household signals (outdated software, odd logins, Defender events, FIM for key paths).
2. Use software inventory + vulnerability detection output to generate plain-English “what to do this week” letters.
3. Integrate osquery for richer inventory and ad-hoc checks.
4. Validate detections with Atomic Red Team and Caldera in a lab environment.
5. Use Amass / ProjectDiscovery / reNgine / Sn1per for periodic external attack surface checks on any domains or cloud assets.
6. Complement with Trivy/Grype for container/image/filesystem vulnerability scanning.
7. Consider custom dashboards or alert enrichment (e.g., local LLM summaries) for non-technical output.
8. Review active response carefully — HouseCalm monitors/alerts; it does not stop attacks.

Starred or referenced for easy access. Fork and adapt rules as needed for your stack.
