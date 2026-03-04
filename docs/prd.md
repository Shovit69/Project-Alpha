# Product Requirements Document (PRD)

## Product Name
Auto Card Wallet

## Author
Shovit Bastakoti

## Version
MVP v0.1

## Date
2026-03-03

---

# 1. Product Overview

## Problem
Consumers often carry multiple loyalty cards from different retailers.  
Finding the correct card during checkout is inconvenient and slow.

## Solution
A mobile wallet application that stores loyalty cards and automatically suggests the correct card based on store location, allowing quick barcode scanning at checkout.

## Target Users
- Frequent retail shoppers
- Users with multiple loyalty cards
- People who want faster checkout experiences

## Success Metrics
- Card opens within 2 seconds
- Successful barcode scan rate > 95%
- Users add at least 3 cards

---

# 2. Screens List

| Screen | Description | Key Actions |
|------|------|------|
| Welcome Screen | Introduces the app | Continue to login |
| Login Screen | User authentication | Sign in / create account | Skip if already logged in |
| Home Screen /Card View Screen| Shows One Big Card | | Displays barcode | Show barcode for scanning | Button for accessing location and retreiving correct card |
| Add Card Screen | Add loyalty card | Scan barcode / manual entry |
| Settings Screen | Manage cards and permissions | Edit or remove cards |
| Profile Screen | Basic user details |
| Settings Screen | 
---

# 3. User Flows

## Flow 1 — First Time Setup
User installs app  
→ Opens welcome screen  
→ Logs in or creates account  
→ Grants location permission /Camera permission   
→ Adds first loyalty card

---

## Flow 2 — Add Loyalty Card

User taps **Add Card**  
→ Camera opens  
→ User scans barcode  
→ If unable , User does manually 
→ Card saved in wallet

---

## Flow 3 — Use Card at Store

User enters store location(App grabs from user location )  
→ App detects store  
→ Relevant loyalty card Pops big   
→ USer displays to store
→ Barcode displayed  
→ Store scans barcode

---

# 4. User Stories

## Card Management
- As a user, I want to add my loyalty cards so that I do not carry physical cards.
- As a user, I want to scan my card barcode so that adding cards is fast.

## Smart Detection
- As a user, I want the correct loyalty card to appear automatically so I do not search manually.

## Checkout
- As a user, I want to open the barcode quickly so the cashier can scan it immediately.

## Control
- As a user, I want to edit or remove cards so that I can manage my wallet.

---

# 5. Edge Cases

## Location Permission Denied
User denies location permission.

System behavior:
- Notify user why location is needed and explain privacy policy
- Allow manual card selection.

---

## Camera Permission Denied
User denies camera permission  and explain privacy policy

System behavior:
- Allow manual barcode entry.

---

## Offline Mode
User has no internet connection.Try to recover from downloaded apps and offline GPS

System behavior:
- Cards stored locally.
- Barcode can still be displayed.

---

## Store Detection Failure
App cannot identify store location. show probable cards around if too many stores areound 

System behavior:
- Show list of neabry stores
- User chooses manually.

---

# 6. MVP Scope

## Included
- Add card by scanning barcode
- Store loyalty cards locally
- Display barcode for scanning
- Basic location detection
- Manual card selection

## Not Included
- Cloud synchronization
- Rewards tracking
- NFC payments
- Multi-device sync 

---

# 7. Acceptance Criteria

## Add Card
- User can scan barcode successfully
- Card is saved locally
- Card appears in wallet

## Display Card
- Card opens within 2 seconds
- Barcode readable by scanner

## Store Detection
- App suggests correct card when entering store

## Offline Usage
- User can display barcode without internet

---

# 8. Future Enhancements

- Apple Wallet integration
- Google Wallet integration
- AI card suggestions
- Cloud backup
- Rewards tracking