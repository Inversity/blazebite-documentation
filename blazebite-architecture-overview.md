# BlazeBite System Architecture & Workflows

## System Overview
BlazeBite is a location-based food ordering platform connecting small/unique venues (food trucks, stadium concessions, golf clubs) with customers through a managed device ecosystem and custom apps.

---

## 1. Customer Apps (iOS & Android)
**Purpose:** Public-facing ordering interface for end customers

### Core Workflow:
1. **Discovery Phase**
   - App uses GPS to show nearby venues
   - Filters by distance, type, availability
   - Shows venue hours, status (open/closed)

2. **Ordering Phase**
   - Browse menu with categories, items, modifiers
   - Add to cart with customizations
   - Apply promo codes/deals

3. **Checkout Phase**
   - Select pickup/delivery method (counter, seat delivery)
   - Payment processing (in-app card, soon: Stripe)
   - Order confirmation with pickup time

4. **Fulfillment Phase**
   - Real-time order status updates
   - Push notifications for ready orders
   - QR code for pickup verification

### Data Dependencies:
- **FROM Portal:** Menu structure, pricing, venue details, hours, pickup locations
- **TO Kitchen:** Order details, customer info, modifications
- **TO Backend:** Payment processing, order history, analytics

### Key Technical Details:
- Location services required for venue discovery
- Push notifications for order updates
- Offline menu caching for performance
- Deep linking for promotional campaigns

---

## 2. Kitchen App (Android - Tablet/Kiosk)
**Purpose:** Venue-side order management and business operations

### Core Workflows:

**Order Management:**
1. Receives incoming orders in real-time
2. Staff accepts/rejects orders
3. Marks preparation stages
4. Triggers customer notifications
5. Handles refunds/modifications

**Expeditor View:**
- Simplified UI for kitchen staff
- Focus on order queue and timing
- Large text, high contrast display
- Timer-based prioritization

**Business Management:**
- Daily/weekly sales reports
- Popular items tracking
- Peak time analysis
- Inventory suggestions

### Hardware Configurations:
- **Tablet Mode:** Bluetooth printer, portable setup
- **Kiosk Mode:** USB printer, fixed installation
- Both run same app with different UI optimizations

### Data Dependencies:
- **FROM Customer Apps:** Orders, payment status
- **FROM Portal:** Venue config, menu updates, staff permissions
- **TO Printer:** Receipt formatting, order tickets
- **TO Backend:** Sales data, inventory updates

---

## 3. Venue Portal (Web - Tailwind)
**Purpose:** Venue configuration and management hub

### Core Management Areas:

**Menu Management:**
- Categories (Appetizers, Entrees, etc.)
- Items with descriptions, prices, images
- Modifiers (size, toppings, etc.)
- Availability scheduling
- Combo/deal creation

**Venue Configuration:**
- Business hours
- Location settings
- Pickup/delivery zones
- Seating charts (for stadiums)
- Tax rates
- Tip suggestions

**Appearance/Branding:**
- Logo upload
- Color schemes
- Banner images
- Marketing messages

**Operations:**
- Staff account management
- Device management (tablets/kiosks)
- Notification preferences
- Payment settings
- Report generation

### Critical Portal → App Sync:
- Menu changes must propagate to Customer Apps within 5 minutes
- Venue hours affect real-time availability
- Pickup location changes affect Kitchen display
- ALL downstream apps depend on Portal accuracy

---

## 4. Super Admin Portal (Limited Release)
**Purpose:** BlazeBite administrative control

### Management Capabilities:
- Venue account creation/suspension
- Subscription tier management
- Global fee structures
- Currency settings
- System-wide announcements
- Multi-venue ownership groups
- Advanced analytics

---

## 5. Critical Data Flows

### Order Flow:
```
Customer App → Backend → Kitchen App → Printer
     ↓            ↓           ↓
  Payment    Notifications  Analytics
```

### Configuration Flow:
```
Portal → Backend → Customer Apps
              ↓
          Kitchen App
```

### Device Provisioning Flow:
```
Esper MDM → Device → Kitchen App → Portal Login
```

---

## Integration Points & Dependencies

### Payment Systems:
- Current: In-app card processing only
- Coming: Stripe integration
- Coming: Cash drawer support

### External Services:
- Esper MDM for device management
- SMS for customer notifications
- Push notification services
- Location services/mapping
- Receipt printer protocols (ESC/POS)

### Authentication Flow:
- Same credentials work across Portal + Kitchen App
- Customer accounts separate system
- Staff can have multiple venue access

---

## Common Failure Points (QA Focus Areas)

### Portal → App Sync Issues:
- Menu changes not reflecting
- Price updates delayed
- Venue hours mismatch
- Location settings corruption

### Order Flow Breaks:
- Orders not reaching Kitchen
- Notification failures
- Payment confirmation delays
- Printer communication drops

### Device/Network Issues:
- WiFi instability breaking order flow
- Bluetooth printer disconnection
- App update failures
- Login session timeouts

### Edge Cases to Test:
- Venue switching time zones
- Multiple orders at once
- Menu changes during active orders
- Network drops mid-order
- Printer paper out scenarios
- Customer refunds after pickup

---

## Testing Priority Matrix

### HIGH Priority (Breaks Everything):
1. Portal menu configuration
2. Order transmission Customer → Kitchen
3. Payment processing
4. Device provisioning

### MEDIUM Priority (Bad Experience):
1. Push notifications
2. Printer reliability
3. Report accuracy
4. Search/filtering

### LOW Priority (Nice to Have):
1. Analytics accuracy
2. UI polish issues
3. Performance optimization
4. Advanced features

---

## Key Business Context

### Why These Venues Need BlazeBite:
- Can't afford custom app development
- Don't fit DoorDash/UberEats model
- Need location-specific features (stadium seating)
- Want to own customer relationships
- Need specialized workflows (concession stands)

### Revenue Model:
- Venues pay device rental/subscription
- Transaction fees on orders
- Premium features (marketing, analytics)
- Advertisement partnerships

### Growth Indicators:
- New venue onboarding rate
- Order volume per venue
- Customer retention/repeat orders
- Device utilization rates
