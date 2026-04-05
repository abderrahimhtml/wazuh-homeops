# Active Response Configuration

Wazuh is configured to automatically respond to SSH brute force attacks.

## Rule
- Rule ID: 5763 (SSH brute force detected)
- Action: firewall-drop (block attacker IP)
- Timeout: 300 seconds (5 minutes)

## How it works
When Wazuh detects 8+ failed SSH login attempts from the same IP,
it automatically blocks that IP using iptables for 5 minutes.
