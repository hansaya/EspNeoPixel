# EspNeoPixel

Esp32 based neo pixel driver designed to work with WLED. 

# Thoughts behind my design
I recently discovered that [wled project](https://github.com/Aircoookie/WLED) works with [hyperion](https://hyperion-project.org/) and sparked my interest in building a unified system to tick off all the requirements. From previous experience with neo pixels, I knew I had to make sure to have a good power supply and a good logic level conversion to run the leds reliably. Power supply is the biggest thing to tackle and for it I have tried many off the shelve converters but most either bulky or cannot run at specified rating. You could buy a AC to DC converts thats rated for the led without using dc-dc converter but either they are expensive or have to compromise in quality. I decided to design my board around ~20V input because I have many old laptop power bricks collecting dust that can handle at least 100W each. They are safe and can find in many shape and sizes. If you don't have one, you can easily obtain one through ebay. 

Features:
* Buck converter, 8-24V input to 5v or 12v output to drive the led strips.
* Up to 10A output current.
* Level converter to drive the data and clock singles at 5v.
* Button connected to GPIO0. This can be used within wled to turn off the output.
* Capability to turn off the output using wled relay output.
* Push in terminal connectors for quick connections.

# Board

Use zip file within /cam folder to fabricate the board using your favorite pcb house. Bom contains the parts list. Please note, I have not listed out all parts since I had most 0603 jelly beans parts at home. Use the schematic to get the full list.

Enjoy!