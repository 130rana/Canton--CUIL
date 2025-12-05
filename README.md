# Canton Unified Interaction Layer (CUIL)

## Overview  
CUIL is a modular interaction layer that unifies user actions, asset states, and protocol messaging across Canton applications. It is designed to eliminate the fragmented user experience across Canton apps and create a seamless, coherent flow where actions and states naturally “follow” the user.

---

## Problem  
Despite Canton’s strong infrastructure, the user experience is fragmented:

- Users constantly switch between apps with different UIs and onboarding flows.  
- Balances, positions, and risk states do not carry over between apps.  
- Developers build in isolated silos, making unified flows difficult.  
- Composable finance is possible in theory but operationally disconnected.  

The ecosystem feels *powerful for builders* but *scattered for users*. CUIL addresses the invisible UX layer that ties all Canton actions together.

---

## Solution: CUIL  
CUIL is a lightweight “interaction fabric” that sits between users and Canton apps—without replacing them or forcing new standards—making the entire ecosystem feel like one continuous environment.

### **1. Universal Interaction Schema (UIS)**  
A simple schema apps can expose to standardize:

- Actions (lend, borrow, stake, swap…)  
- Requirements (collateral, approvals, risk thresholds)  
- Expected outcomes (balances, positions, state changes)

No internal changes required for apps—just expose logic via UIS.

### **2. Context-Aware State Memory (CASM)**  
Tracks the user’s dynamic context across apps:

- Balances  
- Active positions  
- Risk exposure  
- Pending actions  
- User preferences  
- Recent steps  

Users no longer lose their state when switching apps.

### **3. Flow-Oriented Smart Guides**  
Dynamic, contextual guides such as:

- “You can borrow more—your RWA collateral increased.”  
- “This swap lowers your margin health.”  
- “You have unused assets improving capital efficiency.”

Guides use UIS + CASM, without needing on-chain AI.

### **4. Inter-App Coordination Layer**  
Borrow on App A → Swap on App B → Re-stake on App C  
All executed in one coherent flow, even if the apps never integrated directly.

### **5. Developer Plugins**  
Optional modules for teams:

- UI consistency components  
- Safety/risk check modules  
- UIS data adapters  
- Pre-built templates for common actions  

### **6. Zero-Lock-In Architecture**  
No consensus layer, no wallet replacement, no forced UX.  
CUIL is optional, modular, and designed to “disappear” behind the apps.

---

## Tools & Technologies  

- **Daml APIs & JSON Ledger API**  
- **React** (front-end UI)  
- **WebGL** (interactive visualizations)  
- **Lightweight off-chain session storage** for CASM  
- **Canton interoperability primitives**  
- **Mock UX prototypes & diagrams**

---

## How to Run (Prototype)  
If a prototype exists:

```bash
git clone https://github.com/USERNAME/Canton--CUIL
cd Canton--CUIL
npm install
npm start
