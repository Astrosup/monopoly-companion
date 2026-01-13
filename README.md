# 🎩 Monopoly Companion OS

**Monopoly Companion OS** is a single-file, mobile-responsive web application designed to act as a "Digital Banker" and "Game Master" for your physical Monopoly board game. 

It replaces paper money and deed cards with a streamlined digital interface, speeding up gameplay and introducing a **Dynamic Economy System** that changes rent prices based on market events.

---

## 🚀 Quick Start

1. **Download:** Save the source code as `index.html`.
2. **Run:** Open the file in any modern web browser (Chrome, Safari, Firefox).
   - *Recommended:* Use a tablet or smartphone placed in the center of the table.
3. **Play:** Use physical dice and tokens, but use this app for all transactions.

## ✨ Key Features

### 🏦 Digital Banking
* **Automated Math:** No more calculation errors. The app handles all cash additions and subtractions.
* **Instant Rent:** Calculates rent automatically based on:
  * Dice rolls (Utilities).
  * Ownership count (Railroads).
  * House/Hotel level (Properties).
* **Mortgages:** One-click mortgage/unmortgage management.

### 📈 Dynamic Economy System
This OS introduces a "House Rule" mechanic called the **Economy**.
* **Trigger:** When all 4 players have passed GO.
* **Effect:** A random event occurs (e.g., *Market Boom*, *Recession*, *Housing Bubble*).
* **Impact:** Specific color groups (e.g., Red Properties) receive a rent multiplier (e.g., +50% or -30%) for the duration of the round.

### 🔨 Advanced Tools
* **Auction House:** A built-in turn-based interface to handle bidding wars when a player declines to buy a property.
* **Trading Post:** A dedicated screen to swap cash and properties between players.
* **Card Manager:** Handles Chance and Community Chest financial effects (beta).

---

## 🕹️ User Guide

### The Dashboard (Home)
* **Status:** See current cash, "Passed Go" status, and the current Economy Round multiplier.
* **Action:** Tap a player's name to open their specific menu.

### Player Menu
* **Board Spaces:** View the map, buy properties, or pay rent to owners.
* **My Properties:** Manage your portfolio. Build houses/hotels or mortgage properties here.
* **Trade:** Initiate a trade with another player.

### Buying & Rent
1. Navigate to **Board Spaces**.
2. Click the property you landed on.
   * **If unowned:** You can "Buy" or "Start Auction".
   * **If owned:** You will see a big "Pay Rent" button.

---

## 🛠️ Configuration & Customization

Since this is a single-file application, you can modify game data directly in the `<script>` section of the HTML file.

### Changing Player Names
Find the `state` object around line 240:
```javascript
players: [
    { id: 'p1', name: 'Dad', ... },
    { id: 'p2', name: 'Mom', ... },
    ...
]
