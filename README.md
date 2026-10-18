# 🛡️ Wazuh SIEM Zero-Downtime Migration

> Amazon Linux 2 → Ubuntu 24.04
> 84+ Agents | Zero Alert Loss | Zero Downtime | 72 Hours

## 🎯 Challenge

Migrate production Wazuh SIEM from EOL Amazon Linux 2
to Ubuntu 24.04 without disrupting security monitoring
across 84+ agents in production infrastructure.

## 📋 Migration Strategy
Phase 1: Parallel Setup
OLD: Amazon Linux 2 Manager (active)
NEW: Ubuntu 24.04 Manager (standby)
Phase 2: Config Migration
Export custom rules + decoders
Migrate agent groups
Validate rule parity
Phase 3: Rolling Agent Migration
Groups of 10 agents at a time
Verify connection + events
Monitor 1 hour before next group
Phase 4: Parallel Run (7 days)
Both managers active
Alert parity monitoring
Zero discrepancy threshold
Phase 5: Decommission
Old manager offline
Migration complete
## ⚙️ Tech Stack

| Component | Technology |
|---|---|
| SIEM | Wazuh 4.14.5 |
| Old OS | Amazon Linux 2 |
| New OS | Ubuntu 24.04 LTS |
| Agents | 84+ (Linux servers) |
| Monitoring | Custom detection rules |

## ⚠️ Risks Mitigated

| Risk | Mitigation |
|---|---|
| Agent connection failure | One-command rollback script |
| Custom rule loss | Full export + version control |
| Alert gap during cutover | 7-day parallel run |
| Log format issues | All 84 agent configs pre-validated |

## 📊 Results

- ✅ 84+ agents migrated
- ✅ Zero alert loss
- ✅ Zero downtime
- ✅ Zero agent reinstallation
- ✅ Complete in 72 hours

## 🔑 Key Learning

Parallel manager strategy is the safest approach —
never cut over without running both systems
simultaneously and validating parity first.
