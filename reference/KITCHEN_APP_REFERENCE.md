# BlazeBite Kitchen App Reference Guide

**Complete Internal Reference for All Menu Screens**

This document provides detailed information about all nine screens accessible via the hamburger menu (☰) in the BlazeBite Kitchen app. This is an internal reference guide for support staff and venue managers.

---

## 📱 App Navigation Overview

The Kitchen app uses a **hamburger menu** (☰) located in the **top-left corner** of the screen to access all main features. Tap the three horizontal lines to reveal the menu with these options:

1. Orders
2. Expeditor
3. Order History
4. Menu Management
5. Order Stats
6. Location Presets
7. Checkout *(if enabled)*
8. Settings
9. Log Out

---

## 1️⃣ Orders Screen

**Purpose:** Primary order management interface for viewing and fulfilling incoming orders.

### Overview
The Orders screen is your main workspace during service hours. Orders appear in real-time as they're placed by customers through the BlazeBite ordering system (web, mobile app, kiosk, etc.).

### Screen Layout

**Top Section:**
- **Header:** "Orders" title
- **Filter/Sort Options:** Filter by status (New, In Progress, Ready)
- **Refresh Button:** Manual refresh (app auto-refreshes every few seconds)

**Order Cards:**
Each order displays as a card with:
- **Order Number:** Unique identifier (e.g., #12345)
- **Time Received:** Timestamp of when order was placed
- **Customer Name:** First name or "Guest"
- **Order Type:** Pickup, Delivery, Dine-in (if applicable)
- **Status Badge:** New (red), In Progress (yellow), Ready (green)
- **Item Count:** Number of items in the order
- **Special Requests:** Icon if modifications or notes present

### Order Workflow

#### Step 1: New Order Arrives
- Order appears with **red "NEW"** badge
- Visual notification (screen flash or banner)
- Audio notification (if enabled in Settings)
- Auto-print if configured in Portal

#### Step 2: Acknowledge Order
- **Tap** on the order card to open details
- Review all items and special requests
- Order status automatically changes to **"In Progress"** (yellow)

#### Step 3: View Order Details
When you tap an order, you see:
- **Full item list** with quantities
- **Modifications** (e.g., "No onions", "Extra sauce")
- **Special instructions** from customer
- **Order time and estimated pickup time**
- **Customer contact info** (if provided)
- **Payment status** (Paid, Pending, etc.)

#### Step 4: Print Order (if needed)
- **Print Button** at bottom of order detail screen
- Sends order ticket to connected Bluetooth printer
- Can print multiple times if needed (e.g., for kitchen stations)
- Print status indicator (Printed, Not Printed, Failed)

#### Step 5: Mark Order Ready
- Once food is prepared and packaged
- **Tap "Mark Ready"** button at bottom
- Order status changes to **"Ready for Pickup"** (green)
- Customer receives notification (if enabled)
- Order moves to "Ready" filter section

#### Step 6: Complete Order
- When customer picks up the order
- **Tap "Complete"** or swipe to complete
- Order moves to Order History
- No longer visible on main Orders screen

### Order Card Actions

**Swipe Gestures:**
- **Swipe right:** Mark as ready (quick action)
- **Swipe left:** Cancel or delay order (brings up options)

**Long Press:**
- Long press on order card for additional options:
  - Print
  - Edit (if permitted)
  - Cancel
  - Delay
  - Add notes

### Print Status Indicators

Orders show print status with icons:
- **🖨️ Printed:** Order ticket successfully printed
- **⚠️ Print Failed:** Printer error, needs retry
- **○ Not Printed:** Auto-print disabled or manual print needed

### Filters and Sorting

**Filter Tabs:**
- **All:** Shows all active orders
- **New:** Only new unacknowledged orders
- **In Progress:** Orders being prepared
- **Ready:** Orders ready for pickup

**Sort Options:**
- By Time (oldest first - default)
- By Pickup Time (earliest pickup first)
- By Order Number
- By Location (if using multiple pickup points)

### Special Request Alerts

Orders with modifications or special requests show:
- **Orange alert icon** on order card
- **"Special Request" badge**
- Requests highlighted in order detail view

💡 **Tip:** Always read special requests carefully - they may include allergies or critical modifications.

### Order Statistics (on Orders Screen)

Top of screen may show:
- **Active Orders:** Count of orders in New + In Progress
- **Ready Orders:** Count waiting for pickup
- **Today's Total:** Orders completed today

---

## 2️⃣ Expeditor Screen

**Purpose:** Kitchen-optimized view for high-volume periods and expo stations.

### Overview
The Expeditor screen provides a bird's-eye view of multiple orders simultaneously, allowing kitchen staff or expeditors to quickly manage order flow without opening individual orders.

### Screen Layout

**Grid/Card View:**
- Orders displayed in a **grid layout** (2-4 columns depending on tablet size)
- Each order shown as a compact card
- More orders visible at once compared to Orders screen

**Card Information:**
- **Order number** (large, prominent)
- **Elapsed time** since order received
- **Item count** and quick item summary
- **Status** (color-coded: red/yellow/green)
- **Timer** showing time in current status

### Expeditor Workflow

#### During Rush Periods
1. **Monitor all orders** at a glance
2. **Check elapsed times** (highlighted if over threshold)
3. **Prioritize** based on time or pickup window
4. **Quick status updates** with single tap
5. **Call out orders** to kitchen stations

#### Color Coding
- **Red Cards:** New orders, need immediate attention
- **Yellow Cards:** In progress, monitor for timing
- **Green Cards:** Ready for pickup
- **Orange Border:** Has special requests or modifications

### Time Alerts

Orders are highlighted when:
- **5 minutes:** Order still in "New" status
- **15 minutes:** Order still "In Progress"
- **20 minutes:** Order ready but not picked up
- Thresholds configurable in Settings

### Quick Actions

**Tap Actions:**
- **Single tap:** Open order details (same as Orders screen)
- **Double tap:** Mark next status (New → In Progress → Ready)
- **Long press:** Show action menu

**Swipe Actions:**
- **Swipe up:** Priority boost (moves to top)
- **Swipe down:** Delay order
- **Swipe right:** Mark ready

### Expeditor-Specific Features

**Running Timers:**
- Each order shows **elapsed time** in current status
- Helps identify bottlenecks
- Visual warning when times exceed targets

**Item Summary:**
- Quick preview of order contents
- Example: "2 Burgers, 1 Salad, 3 Drinks"
- Allows calling out orders to stations

**Kitchen Station Tags** (if configured):
- Orders can show station assignments
- Example: "Grill", "Fryer", "Cold Prep"
- Helps coordinate multi-station orders

### When to Use Expeditor View

✅ **Use Expeditor when:**
- Managing high order volume (10+ active orders)
- Multiple kitchen staff working different stations
- You need to monitor overall kitchen flow
- Running an expo station coordinating order assembly

❌ **Use Orders screen when:**
- Low to moderate volume (1-10 orders)
- Need detailed view of order contents
- Focused on individual order fulfillment
- Single person managing all orders

💡 **Tip:** Many venues switch to Expeditor view during lunch/dinner rush and back to Orders during slower periods.

---

## 3️⃣ Order History & Refunds

**Purpose:** View past orders and process refunds when authorized.

### Order History Overview

Access all completed, cancelled, and refunded orders from previous days and current day.

### Screen Layout

**Search and Filter Bar:**
- **Search field:** Search by order number, customer name, or phone
- **Date picker:** Select specific date or date range
- **Status filter:** All, Completed, Cancelled, Refunded
- **Export button:** Export orders to CSV (if enabled)

**Order List:**
- Orders displayed in reverse chronological order (newest first)
- Each row shows:
  - Order number
  - Date and time
  - Customer name
  - Total amount
  - Status badge
  - Quick actions (View, Refund)

### Viewing Past Orders

1. **Select date range** or search for specific order
2. **Tap** on order to view full details
3. View complete order information:
   - All items ordered
   - Payment method
   - Original order time
   - Completion time
   - Any modifications or special requests
   - Customer information

### Search Functionality

**Search by:**
- **Order Number:** Enter full or partial order number (e.g., "12345")
- **Customer Name:** First or last name
- **Phone Number:** Customer contact number
- **Date Range:** Specific day, week, or custom range

**Search Tips:**
- Use partial matches for names (e.g., "John" finds "Johnny", "Johnson")
- Order numbers can be entered with or without # symbol
- Date searches include all orders within selected range

### Processing Refunds

⚠️ **Authorization Required:** Only authorized users can process refunds. Check with your manager about refund permissions.

#### Refund Workflow

**Step 1: Locate Order**
- Search for the order using Order History search
- Verify it's the correct order

**Step 2: Open Order Details**
- Tap on the order in the list
- Review order contents and total

**Step 3: Initiate Refund**
- Tap **"Refund"** button at bottom of screen
- Select refund type:
  - **Full Refund:** Entire order amount
  - **Partial Refund:** Select specific items or enter custom amount
  - **Cancel Order:** Cancel pending order (before fulfillment)

**Step 4: Select Reason**
- Choose from dropdown menu:
  - Wrong order prepared
  - Quality issue
  - Customer complaint
  - Order never picked up
  - Venue error
  - Other (requires note)

**Step 5: Add Notes** (required)
- Enter explanation for refund
- Be specific (e.g., "Burger was cold, customer complaint")
- Notes are logged for accounting and review

**Step 6: Confirm Refund**
- Review refund amount and reason
- Tap **"Confirm Refund"**
- Wait for processing (usually 2-5 seconds)

**Step 7: Refund Confirmation**
- Success message displays
- Customer receives refund notification
- Order marked as "Refunded" in history
- Refund processes to original payment method

✅ **Success Indicator:** Green checkmark and "Refund Processed" message

#### Refund Policies

**Full Refund:**
- Order not picked up due to venue error
- Significant quality issues
- Completely wrong order prepared

**Partial Refund:**
- Single item issue in larger order
- Minor quality complaint
- Missing item(s)

**No Refund Situations:**
- Customer changed mind after pickup
- Order was correct and picked up
- Customer complaint without validity

💡 **Tip:** Always document refunds thoroughly in notes. This helps with accounting and identifies patterns for improvement.

### Refund Limitations

- **Time Limit:** Refunds typically allowed within 7-14 days of order
- **Authorization:** Some refunds require manager approval
- **Refund Methods:** Funds return to original payment method only
- **Processing Time:** Credit card refunds take 3-5 business days

### Export Orders (if enabled)

1. **Select date range** for export
2. **Tap "Export" button**
3. **Choose format:** CSV or PDF
4. **Select fields** to include (optional)
5. **Tap "Generate Export"**
6. **Download or email** file

**Exported Data Includes:**
- Order numbers and dates
- Customer information
- Items and totals
- Payment methods
- Order statuses
- Times (received, completed)

---

## 4️⃣ Menu Management

**Purpose:** Real-time control over menu and item availability.

### Overview
Menu Management allows you to toggle entire menus or individual items on and off. Changes sync instantly to all customer-facing ordering systems (website, apps, kiosks).

### Screen Layout

**Menu List View:**
- Shows all configured menus
- Each menu has an on/off toggle switch
- Expand menu to see individual items

**Menu Categories:**
- Breakfast
- Lunch
- Dinner
- Late Night
- Drinks
- Desserts
- Specials
- (Custom categories as configured)

### Managing Entire Menus

#### Turn Menu On
1. **Tap the toggle switch** next to menu name
2. Switch turns **green** (on position)
3. **Confirmation message:** "Menu activated"
4. All items in menu become available to customers

#### Turn Menu Off
1. **Tap the toggle switch** next to menu name
2. Switch turns **gray** (off position)
3. **Confirmation message:** "Menu deactivated"
4. Entire menu hidden from customers immediately

**Common Use Cases:**
- **Start of day:** Turn on Breakfast menu
- **Mid-day:** Turn off Breakfast, turn on Lunch
- **Evening:** Turn on Dinner menu
- **Kitchen closes:** Turn off all menus

### Managing Individual Menu Items

#### View Items in a Menu
1. **Tap** on menu name (not the toggle)
2. Menu **expands** to show all items
3. Each item has its own toggle switch

#### Turn Item Off (86 an Item)
1. **Find the item** in the menu list
2. **Tap the toggle** next to item name
3. Switch turns **gray** (off)
4. Item immediately unavailable to customers
5. Optional: Add reason note (e.g., "Out of ingredients")

#### Turn Item Back On
1. **Tap the toggle** to turn it back to **green**
2. Item immediately available again
3. Customers can order immediately

**When to 86 Items:**
- Ran out of ingredient(s)
- Equipment issue (e.g., fryer down, can't make fries)
- Item prep delayed
- Special item sold out
- Quality issue with ingredient

💡 **Tip:** Use Menu Management liberally during service to prevent orders for items you can't make. It's better to mark items unavailable than to cancel customer orders.

### Item Status Indicators

Items show various status indicators:
- **Green toggle:** Item available
- **Gray toggle:** Item unavailable (86'd)
- **Orange warning icon:** Item low stock (if inventory tracking enabled)
- **Clock icon:** Item scheduled (available only at certain times)

### Batch Operations (if available)

Some versions allow bulk updates:
- **Turn off entire category** (e.g., all sandwiches)
- **Quick 86 list:** Common items to disable
- **Scheduled changes:** Pre-set menu toggles for specific times

### Scheduled Menus

If your venue uses scheduled menus:
- Menus automatically activate/deactivate at set times
- You can override schedule with manual toggles
- **Auto icon** shows when menu is schedule-controlled
- Manual changes persist until next scheduled change

**Example Schedule:**
- Breakfast: Auto-on at 7am, auto-off at 11am
- Lunch: Auto-on at 11am, auto-off at 3pm
- Dinner: Auto-on at 5pm, auto-off at 9pm

### Best Practices

✅ **Do:**
- Turn off items as soon as you run out
- Update menus at shift start to verify availability
- Add reason notes when 86'ing items
- Re-enable items as soon as they're available again
- Check Menu Management before opening

❌ **Don't:**
- Forget to turn menus back on after private events
- Leave items off overnight unnecessarily
- Toggle menus during active order (wait for order to complete)
- Make changes without communicating to team

### Troubleshooting

**Changes not appearing for customers?**
- Check WiFi connection
- Verify menu is published in Portal
- Try toggling off and on again
- Contact support if issue persists

**Can't toggle menu or item?**
- Item may be locked in Portal (requires admin)
- Check user permissions
- Verify you have manager role

---

## 5️⃣ Order Stats

**Purpose:** View daily sales reports and performance metrics.

### Overview
Order Stats provides real-time and historical sales data for your venue. Use this for daily reporting, tracking popular items, and analyzing sales trends.

### Screen Layout

**Dashboard View:**
- **Date selector** at top (defaults to today)
- **Summary cards** showing key metrics
- **Charts/graphs** for visual analysis
- **Detailed tables** for item-level data

### Key Metrics

#### Summary Cards

**Today's Orders:**
- Total number of orders
- Compared to previous day
- Average order value

**Total Revenue:**
- Gross sales for selected period
- Breakdown by payment type
- Tax and fees (if applicable)

**Average Order Time:**
- Average time from order placed to ready
- Helps identify efficiency opportunities

**Peak Hours:**
- Busiest hour(s) of the day
- Order volume by hour

### Sales Charts

**Order Volume Over Time:**
- Line graph showing orders per hour
- Helps identify rush periods
- Plan staffing accordingly

**Revenue by Hour:**
- Bar chart of sales by hour
- See which hours generate most revenue

**Top Items:**
- Pie chart or bar graph
- Shows most popular items
- Quantities sold for each item

**Payment Methods:**
- Breakdown of card vs. cash vs. other
- Percentage of each payment type

### Item-Level Statistics

**Popular Items Table:**
Shows for each item:
- Item name
- Quantity sold
- Total revenue from item
- Percentage of total sales
- Average price (if item has variations)

**Sort Options:**
- By quantity (most popular)
- By revenue (highest earning)
- By item name (alphabetical)

### Sales Reports

#### Daily Report
- Summary of all sales for single day
- Order count, revenue, averages
- Top 10 items sold
- Peak hour(s)

#### Weekly Report
- Aggregated data for 7-day period
- Day-over-day comparison
- Trends and patterns
- Best/worst selling days

#### Monthly Report
- Full month statistics
- Week-over-week trends
- Monthly totals and averages

### Exporting Reports

1. **Select date range** for report
2. **Tap "Export" or "Generate Report"**
3. **Choose format:**
   - PDF (formatted for printing)
   - CSV/Excel (for further analysis)
   - Email (send directly)

4. **Select report type:**
   - Summary only
   - Detailed item breakdown
   - Full transaction log

### Use Cases

**Daily Close-Out:**
- Review end-of-day totals
- Verify revenue matches cash/card receipts
- Note best-selling items for inventory planning

**Performance Tracking:**
- Compare current day to previous weeks
- Identify growth or decline trends
- Set sales goals

**Inventory Planning:**
- See which items sell most
- Identify slow-moving items
- Plan prep quantities

**Staffing Decisions:**
- Analyze peak hours for scheduling
- Determine if additional staff needed
- Optimize labor costs

### Filters and Date Ranges

**Quick Select:**
- Today
- Yesterday
- This Week
- Last Week
- This Month
- Last Month
- Custom Range

**Compare Periods:**
- View current period vs. same period last week
- Month-over-month comparisons
- Year-over-year (if data available)

### Troubleshooting

**No data showing?**
- Check date range selection
- Verify orders were actually placed
- Ensure you're viewing correct location (if multi-location)

**Numbers don't match expectations?**
- Verify time zone settings
- Check if refunds are included/excluded
- Confirm filters are set correctly

💡 **Tip:** Check Order Stats daily during your closing routine to catch any discrepancies while they're fresh.

---

## 6️⃣ Location Presets

**Purpose:** Select default pickup location for incoming orders.

### Overview
If your venue has multiple pickup points (e.g., main counter, bar, patio window, drive-thru), Location Presets allows you to set which location new orders should default to.

### Screen Layout

**Location List:**
- Shows all configured pickup locations
- Radio buttons or selection cards
- Currently selected location highlighted
- Description for each location (optional)

### Configured Locations (Examples)

Typical location setups:
- **Main Counter** - Front register/pickup counter
- **Bar Pickup** - Bar area for drink orders
- **Patio Window** - Outdoor pickup window
- **Drive-Thru** - Car pickup (if applicable)
- **Delivery Staging** - Orders for delivery drivers
- **VIP/Suite** - Premium seating area

### How Location Presets Work

#### Setting Default Location

1. **Open Location Presets** from hamburger menu
2. **View available locations**
3. **Tap** on desired location to select it
4. **Green checkmark** or highlight shows active location
5. **Confirmation message:** "Default location set to [Location Name]"

#### Impact on New Orders

Once set:
- All new incoming orders automatically tagged with selected location
- Order tickets print with location label
- Expeditor screen groups orders by location
- Staff knows where to stage completed orders

### When to Change Locations

**Shift Changes:**
- Morning shift focuses on counter orders
- Evening shift splits between counter and bar
- Late night only using bar pickup

**Event-Driven:**
- Special event at patio, enable patio window
- Private event in certain area
- Temporary closure of normal pickup point

**Staff Positioning:**
- When specific staff member stationed at certain location
- Multiple tablets in different areas, each with own location

### Multi-Tablet Setups

If your venue has multiple tablets:
- **Each tablet** can have different default location
- **Tablet 1** (kitchen): Main Counter
- **Tablet 2** (bar): Bar Pickup
- **Tablet 3** (patio): Patio Window

Orders route to appropriate tablet based on:
- Location selected by customer (if option available)
- Order type (food vs. drinks)
- Venue configuration in Portal

### Location Information Display

Each location may show:
- **Location name**
- **Description** (e.g., "Front counter near entrance")
- **Active orders** currently at this location
- **Staff assigned** (if configured)
- **Estimated wait time** for this location

### Overriding Location per Order

Even with a default location set:
1. **Open specific order** details
2. **Tap location field**
3. **Select different location** from dropdown
4. Order reassigned to new location
5. Useful for special circumstances or customer requests

### Single Location Venues

If your venue only has one pickup location:
- Location Presets menu may not appear
- No action needed - all orders go to single location
- This screen is only relevant for multi-location setups

💡 **Tip:** If you have multiple pickup points, train staff to check order location label before staging food to ensure it goes to the right place.

### Troubleshooting

**Location not appearing in list?**
- Locations configured in Portal
- Contact support or check Portal settings
- May need admin to add new location

**Orders going to wrong location?**
- Verify correct location selected in Location Presets
- Check if customer manually selected different location
- Review Portal routing rules

---

## 7️⃣ Checkout (if enabled)

**Purpose:** Accept walk-up payments and create orders directly on the tablet.

⚠️ **Note:** Checkout feature is only visible if enabled for your venue. Not all venues have this feature activated.

### Overview
The Checkout screen allows you to create orders at the venue for walk-up customers and accept payment via cash or card directly on the tablet. This is useful for customers who want to order in person rather than through digital ordering systems.

### Screen Layout

**Order Entry Area:**
- Item selection interface (similar to customer app)
- Running order total
- Customer name field (optional)
- Special instructions field

**Payment Section:**
- Order summary
- Total amount
- Payment method selection
- Transaction completion buttons

### Creating a Walk-Up Order

#### Step 1: Add Items

1. **Tap "New Order"** or "Create Order"
2. **Browse menu** by category
3. **Tap items** to add to order
4. **Adjust quantities** with +/- buttons
5. **Add modifications** if needed (tap item to customize)
6. **Add special instructions** in notes field

#### Step 2: Review Order

- Verify all items correct
- Check quantities
- Review modifications and special requests
- Confirm total amount

#### Step 3: Optional Customer Info

- **Enter customer name** for order tracking
- **Phone or email** (optional) for notifications
- Helps with order identification at pickup

### Payment Processing

#### Step 4: Select Payment Method

**Cash Payment:**
1. Tap **"Cash"** button
2. Enter **amount tendered** by customer
3. App calculates **change due**
4. Display change amount to customer
5. Tap **"Complete Transaction"**
6. Give customer change

**Card Payment:**
1. Tap **"Card"** button
2. If card reader attached:
   - Prompt customer to insert/tap card
   - Wait for approval
   - Transaction processes automatically
3. If manual entry:
   - Enter card details
   - Process payment
4. Tap **"Complete Transaction"**

#### Step 5: Transaction Complete

- Order submitted to kitchen
- Prints to receipt printer (if configured)
- Give customer receipt and order number
- Order appears in Orders screen like online orders
- Customer can track via order number

### Order Types in Checkout

**For Here / Dine-In:**
- Customer eating on premises
- May include table number

**To Go / Takeout:**
- Customer taking order with them
- Default for most walk-up orders

**Delivery:**
- Some systems allow delivery orders from checkout
- Requires address entry

### Checkout Features

**Quick Add Favorites:**
- Pin frequently ordered items
- One-tap add to order
- Speeds up order entry

**Discounts and Promos:**
- Apply discount codes
- Manual discount entry (with permission)
- Percentage or fixed amount

**Split Payment:**
- Accept multiple payment methods
- Example: Partial cash, partial card
- Track each payment method

**Tax Calculation:**
- Auto-calculates based on venue settings
- Shows tax separately on receipt

### Receipt Options

After payment:
- **Print receipt** - Paper receipt from printer
- **Email receipt** - Send to customer email
- **SMS receipt** - Text receipt to phone
- **No receipt** - Customer declines

### Checkout Security

**Staff Permissions:**
- Checkout may require specific user role
- Some venues restrict to managers only
- Prevents unauthorized transactions

**Cash Handling:**
- Follow venue cash handling procedures
- Count change carefully
- Log cash payments for end-of-day reconciliation

**Voids and Refunds:**
- Void transaction before completion if error
- Refunds handled through Order History (see Section 3)

### Best Practices

✅ **Do:**
- Verify order accuracy before payment
- Count change back to customer clearly
- Provide receipt (even if customer doesn't request)
- Enter customer name for easier tracking
- Be patient with customers unfamiliar with ordering

❌ **Don't:**
- Rush through order entry (leads to errors)
- Process payment before order is complete
- Forget to apply available discounts
- Skip giving receipt

### End-of-Day Reconciliation

For cash transactions:
1. **Review Order Stats** for cash total
2. **Count cash drawer**
3. **Verify amounts match**
4. **Document discrepancies**
5. **Follow venue cash handling policy**

### Troubleshooting

**Card reader not working?**
- Check Bluetooth connection
- Restart card reader
- Fall back to cash payment
- Contact support

**Transaction failed?**
- Ask customer to try card again
- Check WiFi connection
- Verify card reader has power
- Use alternative payment method

**Wrong item added?**
- Tap item in order list
- Select "Remove" or use - button to decrease quantity
- Correct before processing payment

💡 **Tip:** Keep checkout process moving during busy times by having menu visible so customers can decide before reaching the front of line.

---

## 8️⃣ Settings

**Purpose:** Configure hardware, notifications, and app preferences.

### Overview
Settings screen allows you to customize the Kitchen app behavior, connect hardware devices, and adjust notification preferences.

### Settings Categories

#### Printer Settings

**Connected Printers:**
- View currently connected printers
- Connection status (Connected, Disconnected, Error)
- Printer name and model

**Add/Connect Printer:**
1. Tap **"Add Printer"** or **"Connect Printer"**
2. Select printer from available devices list
3. Wait for connection confirmation
4. Test print to verify

**Printer Preferences:**
- **Auto-print on order:** On/Off toggle
- **Number of copies:** 1, 2, or 3
- **Print format:** Standard, Compact, Detailed
- **Cut paper:** Auto-cut on/off
- **Font size:** Small, Medium, Large

**Test Print:**
- Tap **"Test Print"** button
- Verifies printer connection and paper
- Shows sample order format

**Disconnect Printer:**
- Tap **"Disconnect"** next to printer name
- Confirm disconnection
- Printer can be reconnected later

💡 **Tip:** Run a test print after connecting or reconnecting printer to verify everything works before service starts.

#### Notification Settings

**Sound Alerts:**
- **New order sound:** On/Off
- **Choose sound:** Select from available tones
- **Volume:** Slider or Low/Medium/High
- **Repeat alert:** For unacknowledged orders

**Visual Alerts:**
- **Screen flash:** On/Off
- **Banner notifications:** On/Off
- **Badge count:** Show number of new orders

**Alert Frequency:**
- Repeat alerts every X minutes for unacknowledged orders
- Choose: Never, 1 min, 2 min, 5 min

**Do Not Disturb:**
- Quiet hours when venue closed
- Temporarily disable all alerts
- Quick toggle for off-hours

#### Display Settings

**Screen Brightness:**
- Auto (based on ambient light)
- Manual slider
- Bright, Medium, Dim

**Screen Timeout:**
- Never (screen always on - recommended)
- 5 minutes
- 10 minutes
- 30 minutes

**Text Size:**
- Adjust for readability
- Small, Medium, Large, Extra Large
- Affects order cards and details

**Theme:**
- Light mode (default)
- Dark mode (easier on eyes in low light)
- Auto (switches based on time)

#### Order Settings

**Default View:**
- Orders screen (default)
- Expeditor screen
- Your preferred starting screen

**Order Sorting:**
- By time received (oldest first - default)
- By pickup time
- By location

**Auto-Refresh:**
- Frequency of auto-checking for new orders
- Every 10 sec, 30 sec, 1 min (default: 30 sec)

**Confirmation Prompts:**
- Ask before marking order ready: On/Off
- Confirm before cancelling order: On/Off
- Double-confirm refunds: On/Off

#### Account & App Info

**User Profile:**
- Name and role
- Email address
- Venue location
- Staff ID (if applicable)

**App Information:**
- App version number
- Last update date
- Device ID
- Build number

**Legal & About:**
- Terms of service
- Privacy policy
- Licenses
- Contact support

#### Advanced Settings

⚠️ **Caution:** Advanced settings should only be changed by managers or support staff.

**Network Settings:**
- View WiFi connection
- IP address
- Connection diagnostics

**Clear Cache:**
- Clears temporary app data
- Use if app behaving strangely
- Does NOT delete orders or settings

**Reset to Defaults:**
- Restores all settings to original values
- Does NOT log you out
- Does NOT affect printer pairing

**Debug Mode:**
- Enable logging for troubleshooting
- Only enable when working with support
- May impact performance

### Accessing Settings

From any screen:
1. **Tap hamburger menu** (☰)
2. **Tap "Settings"**
3. Navigate to desired settings category
4. Make changes
5. Changes save automatically

### Settings Best Practices

**Daily Setup:**
- Verify printer connection status
- Check notification volume appropriate for noise level
- Confirm screen brightness suitable for lighting

**Troubleshooting:**
- Clear cache if app is slow or glitchy
- Verify WiFi connection in settings
- Check printer status before blaming app

**Team Handoff:**
- Brief next shift on any settings changes
- Document any non-standard configurations
- Reset settings if needed for different shift preferences

### Settings Permissions

Some settings require specific permissions:
- **Printer settings:** All staff
- **Notification preferences:** All staff
- **Order settings:** Manager or above
- **Advanced settings:** Manager only
- **Reset functions:** Manager approval

### Troubleshooting Settings

**Can't access certain settings?**
- Check user role permissions
- Contact manager for access
- Some settings locked at venue level

**Changes not saving?**
- Ensure WiFi connected
- Log out and back in
- Contact support if persists

**Settings reset unexpectedly?**
- May occur after app update
- Reconfigure as needed
- Document your preferred settings

💡 **Tip:** Take screenshots of your preferred settings so you can quickly reconfigure if needed after updates or device changes.

---

## 9️⃣ Log Out

**Purpose:** Sign out of the current user account.

### Overview
Log Out signs you out of the Kitchen app and returns to the login screen. This is important for security and shift changes.

### Logging Out

**Method 1: Via Menu**
1. Open **hamburger menu** (☰)
2. Scroll to bottom
3. Tap **"Log Out"**
4. Confirm log out (if prompted)
5. Returns to login screen

**Method 2: Settings**
1. Open **Settings**
2. Scroll to account section
3. Tap **"Log Out"**
4. Confirm

### What Happens When You Log Out

**Data Preserved:**
- ✅ Order history remains in system
- ✅ Statistics and reports unchanged
- ✅ Printer remains paired (Bluetooth)
- ✅ Settings configurations saved
- ✅ WiFi connection maintained

**Data Cleared:**
- ❌ Active session ended
- ❌ Cached order details cleared
- ❌ User-specific preferences reset (if not saved)

### When to Log Out

**Shift Change:**
- End of shift, next person needs to log in
- Different staff member taking over tablet
- Security best practice for multi-staff venues

**Security:**
- Leaving tablet unattended for extended period
- End of business day
- Prevent unauthorized access

**Troubleshooting:**
- Account sync issues
- Need to switch to different account
- Resolve permissions problems

**NOT Necessary:**
- During short breaks
- Between different staff checking orders
- End of day if same user starts next day

### Logging Back In

After log out:
1. Enter email address
2. Enter password
3. Tap "Log In"
4. Verify printer still connected (Settings)
5. Resume normal operations

### Multiple Users / Shift Changes

**Best Practice for Shift Changes:**

**Closing Shift:**
1. Complete all active orders
2. Mark everything as ready or cancelled
3. Check Order Stats for day
4. Log out from hamburger menu
5. Leave tablet plugged in

**Opening Shift:**
1. Power on tablet (if needed)
2. Open Kitchen app
3. Log in with your credentials
4. Verify printer connection
5. Check Menu Management settings
6. Begin accepting orders

### Account Security

**Password Protection:**
- Don't share your login credentials
- Use strong, unique password
- Change password periodically

**Session Timeout:**
- App may auto-log out after extended inactivity
- Usually 8-24 hours depending on configuration
- Security feature to prevent unauthorized access

### Troubleshooting

**Can't log out?**
- Force close app: Settings > Apps > BlazeBite Kitchen > Force Stop
- Restart tablet
- Contact support if persists

**Logged out unexpectedly?**
- Session timeout (re-login)
- WiFi disconnection (check connection, re-login)
- App update (re-login)
- Account security action (contact support)

**Wrong account logged in?**
- Log out immediately
- Log in with correct credentials
- Report to manager if concerns about data access

💡 **Tip:** If your venue operates 24/7 or has very long shifts, logging out isn't necessary unless changing users. The app is designed to stay logged in for continuous operation.

---

## 📊 Quick Reference Chart

| Screen | Primary Use | When to Use | Key Actions |
|--------|-------------|-------------|-------------|
| **Orders** | View and fulfill incoming orders | During all service hours | View, Print, Mark Ready, Complete |
| **Expeditor** | Multi-order management | High-volume rush periods | Monitor flow, Quick status updates |
| **Order History** | Past orders and refunds | Customer inquiries, End-of-day | Search orders, Process refunds |
| **Menu Management** | Control item availability | When items run out, Shift changes | Toggle menus/items on/off |
| **Order Stats** | Sales reporting | Daily close-out, Performance review | View metrics, Export reports |
| **Location Presets** | Set pickup locations | Multi-location venues | Select default location |
| **Checkout** | Walk-up orders and payments | In-person customer service | Create orders, Process payments |
| **Settings** | Configure app and hardware | Setup, Troubleshooting | Connect printer, Adjust notifications |
| **Log Out** | End session | Shift changes, Security | Sign out |

---

## 🎯 Common Workflows

### Opening Day Workflow
1. Log in to Kitchen app
2. Check **Settings** → Verify printer connected
3. **Menu Management** → Turn on appropriate menus
4. **Location Presets** → Select default location (if multi-location)
5. Return to **Orders** screen
6. Ready to receive orders

### During Service Workflow
1. Monitor **Orders** screen (or **Expeditor** if busy)
2. Tap new orders to review details
3. Print if needed
4. Mark ready when complete
5. Use **Menu Management** to 86 items as needed

### Closing Day Workflow
1. Complete all remaining orders
2. **Menu Management** → Turn off all menus
3. **Order Stats** → Review day's performance
4. Export report if needed
5. **Log Out** (if policy requires)
6. Leave tablet charging

### Handling Customer Issue
1. Go to **Order History**
2. Search for customer order
3. Review order details
4. Process refund if appropriate
5. Document reason in notes

---

## 💡 Pro Tips for Staff

### Efficiency Tips
- **Use Expeditor during rush** - See more orders at once
- **Toggle items preemptively** - 86 items before they run out
- **Print ahead** - Print tickets as soon as orders arrive
- **Set location** - Use Location Presets for proper order routing

### Troubleshooting Tips
- **Printer issues?** Check Settings first, then Bluetooth pairing
- **Orders not appearing?** Check WiFi, refresh app, verify menu active
- **App slow?** Clear cache in Settings
- **Forgot something?** Check Order History to look up details

### Communication Tips
- **Document refunds clearly** - Future you (or coworker) will appreciate
- **Add notes to delayed orders** - Let team know about issues
- **Brief next shift** - Share any menu toggles or issues
- **Report app bugs** - Help improve system for everyone

---

## 📞 Support Resources

### Getting Help

**In-App:**
- Settings → Help/Support
- Settings → Report Issue

**External:**
- Email: support@blazebite.com
- Phone: Mark: 440-231-5818 | Joe: 724-996-6636
- Portal: portal.blazebite.com/support

### Training Materials

- **Onboarding Guide:** ../onboarding/ONBOARDING_TABLET.md
- **Video Tutorials:** portal.blazebite.com/training
- **FAQ:** portal.blazebite.com/faq

### Report Issues

When contacting support:
- Note which screen you're on
- Describe what you expected vs. what happened
- Include order numbers if relevant
- Mention any error messages
- Note your app version (Settings → App Info)

---

## 📝 Appendix: Screen Navigation Map

```
Kitchen App Home (Orders Screen)
│
├── ☰ Hamburger Menu
│   │
│   ├── 1. Orders (Main Order Management)
│   │   └── Order Details → Print, Mark Ready, Complete
│   │
│   ├── 2. Expeditor (Multi-Order View)
│   │   └── Order Cards → Quick Status Updates
│   │
│   ├── 3. Order History
│   │   ├── Search Orders
│   │   ├── View Details
│   │   └── Process Refunds
│   │
│   ├── 4. Menu Management
│   │   ├── Toggle Menus On/Off
│   │   └── Toggle Items On/Off
│   │
│   ├── 5. Order Stats
│   │   ├── Daily Reports
│   │   ├── Charts & Graphs
│   │   └── Export Data
│   │
│   ├── 6. Location Presets
│   │   └── Select Default Pickup Location
│   │
│   ├── 7. Checkout (if enabled)
│   │   ├── Create Order
│   │   └── Process Payment
│   │
│   ├── 8. Settings
│   │   ├── Printer Settings
│   │   ├── Notifications
│   │   ├── Display
│   │   ├── Order Settings
│   │   └── Account Info
│   │
│   └── 9. Log Out
│       └── Return to Login Screen
```

---

## ✅ Staff Training Checklist

Use this checklist to verify staff competency:

**Basic Operations:**
- [ ] Can log in to Kitchen app
- [ ] Understands Orders screen layout
- [ ] Can open and review order details
- [ ] Knows how to mark orders ready
- [ ] Can complete orders when picked up

**Menu Management:**
- [ ] Can turn menus on/off
- [ ] Knows how to 86 individual items
- [ ] Understands when to toggle items

**Printer Operations:**
- [ ] Can verify printer connection in Settings
- [ ] Knows how to reconnect printer
- [ ] Can load printer paper
- [ ] Can perform test print

**Advanced Features:**
- [ ] Comfortable using Expeditor view
- [ ] Can search Order History
- [ ] Understands when/how to process refunds
- [ ] Can view Order Stats for reports

**Troubleshooting:**
- [ ] Knows how to reconnect WiFi
- [ ] Can troubleshoot printer issues
- [ ] Understands when to contact support
- [ ] Can log out and back in

---

**Document Version:** 1.0  
**Last Updated:** November 2025  
**Intended Audience:** Internal staff, support team, venue managers  
**Classification:** Internal reference documentation

---

**End of Kitchen App Reference Guide**

For tablet setup and initial configuration, see **../onboarding/ONBOARDING_TABLET.md**.  
For operational questions and FAQ, see Issue #1 tracking document.