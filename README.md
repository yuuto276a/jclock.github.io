jclock
======

Overview:
---------
jclock is a lightweight JavaScript utility that provides analog clock rendering, timestamp generation, and timezone-adjusted time conversion.  
By adding simple HTML elements to your page, the script automatically initializes and updates the clock display in real time.

Features:
---------
- Zero dependencies: Vanilla JavaScript only
- Auto-detection of HTML targets (`#clock` and `#analog-clock`)
- Real-time analog clock that updates every second
- Timezone conversion with string input (e.g., "+0900")
- Dynamic timestamp label generation

Setup:
------
1. Add the following elements to your HTML:
   <div id="analog-clock"></div>
   <div id="clock"></div>

2. Include the script:
   <script src="jclock.js"></script>

Functions:
----------
t(s)      - Converts a timezone string (e.g. "+0900") into a local time
c(mode)   - mode="1" returns UTC string; mode="2" triggers analog clock init
b()       - Generates timestamp using input fields, or defaults to current time
k()       - Renders and animates analog clock hands
e(e, m)   - Element existence check (returns true/false)
$()       - Shortcut for document.querySelector
j()       - Auto-init function for `#clock` and `#analog-clock`

Examples:
---------
• Get local time from timezone string  
  t("+0900") → "21:42:00"

• Generate timestamp label in YYMMDDHHMM format  
  b() → "2507272142"

• Start analog clock rendering  
  k()

• Auto initialize clock UI  
  j()

Customization:
--------------
• Clock size and color → Edit embedded CSS in `k()` function
• Time format → Adjust `toLocaleTimeString()` options
• Timestamp layout → Modify logic inside `b()`

License:
--------
MIT
