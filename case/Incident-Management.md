# Incident Management Lab

## Overview
This lab demonstrates hands-on experience with ServiceNow ITSM workflows and structured network troubleshooting. The scenario simulates a real-world mobile support issue where a user cannot access corporate email on an iPhone.

The incident was investigated using a hypothetical layered troubleshooting approach and resolved by resetting the device’s network settings.

---

## Objectives
- Simulate end-user incident submission via Service Portal
- Document resolution using ServiceNow best practices
- Create a Knowledge Basearticle for repeat incidents

---

## Environment
- Platform: ServiceNow Personal Developer Instance (PDI)
- Modules Used:
  - Service Portal
  - Incident Management
  - Service Operations Workspace
  - Knowledge Base
- Test Users:
  - Abel Tuter (End User)
  - Beth Anglin (IT Support Agent)
- Device: iPhone (user-reported issue)

---

## Lab Steps

### 1. Preparation (End-User Simulation)
- Impersonated user: `Abel Tuter`
- Accessed Service Portal (`/sp`)
- Simulated user experience when submitting a ticket

---

### 2. Incident Creation
- **Short Description:** Cannot access corporate email on iPhone  
- **Description:** User unable to sync or access corporate email via mobile device  
- **Urgency:** High (business-impacting issue)

---

### 3. Incident Resolution (Help Desk Perspective)

- Impersonated: `Beth Anglin`
- Accessed **Service Operations Workspace**
- Located and investigated the incident

---

## Troubleshooting Methodology

A structured, layered approach was used to isolate the issue:

### Step 1: Confirm Wi-Fi Connection
- Verified correct SSID and signal strength
- Toggled Wi-Fi OFF/ON
- Forgot and reconnected to network

**Purpose:** Eliminate stale or unstable connections

---

### Step 2: Validate Internet Connectivity
- Tested web access using Safari 

**Outcome Logic:**
- No internet = network issue
- Internet works = likely app/configuration issue

---

### Step 3: Compare Networks (Isolation Step)
- Tested using:
  - Cellular data
  - Mobile hotspot

**Outcome:**
- Works on hotspot = Wi-Fi network issue identified
- Fails everywhere = not network-related

---

### Step 4: Check for Captive Portal Issues
- Opened browser to trigger login portal
- Tested random website access

**Purpose:** Detect “connected but no internet” scenarios common in restricted networks

---

### Step 5: Toggle VPN
- Tested with VPN ON and OFF

**Purpose:** Validate dependency on corporate VPN for email access

---

### Step 6: Reset Network Settings (Final Resolution)
- Navigated to:
  Settings > General > Transfer or Reset iPhone > Reset > Reset Network Settings

**Result:**
- Cleared corrupted network configurations (DNS, routing, saved connections)
- Restored normal connectivity
- Corporate email access successfully resumed

---

### Step 7: Evaluate Network Restrictions
- Considered:
  - Firewall rules
  - DNS filtering
  - Router misconfiguration

**Context:** Common in corporate or public Wi-Fi environments

---

## Resolution Summary

- **Root Cause:** Corrupted network configuration on the iPhone  
- **Fix Applied:** Reset network settings  
- **Outcome:** Email functionality restored and verified  

---

## Documentation in ServiceNow

### Work Notes (Internal)
- Documented full troubleshooting flow
- Included network isolation steps and test results

### Resolution Notes (User-Facing)
- Provided clear explanation of fix:
  > Reset network settings to resolve connectivity issue causing email sync failure

- Incident marked as **Resolved**

---



---


---

