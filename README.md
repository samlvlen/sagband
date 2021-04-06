# Zbar-barcode-reader-python-javascript
A bar code reader which detects and read barcode and Qr codes from the live streaming webcam, laptop cam and mobile phones (back and front both) camera.

Features
-------

- Reads and decodes any type of bar code and qr code from the live camera stream.
- Compatible with all the modern devices.
- Can be accessible from the mobile camera (back and front both)
- Uses javascript `getUserMedia ` API call to get live camera feed.
- Uses Python open source library (Zbar) Pyzbar for barcode decoding.
- Runs on Django server.
Note: Code can be use on different python frameworks.
Important Files: `/bar/static/js/main.js` `/bar/views.py` `/bar/barcode.py`

Usage
-------

**To run locally:**

First fork this repository and then follow these steps:
```
git clone https://github.com/your-name/Zbar-barcode-reader-python-javascript.git
cd Zbar-barcode-reader-python-javascript
pip install -r requirements.txt
python manage.py runserver
```
Now open [127.0.0.1:8000](127.0.0.1:8000 "127.0.0.1:8000") locally on your browser.


*Note: Starting with Chrome 47, `getUserMedia()` requests are only allowed from secure origins: HTTPS or localhost.*

**Solution: For development use `django-sslserver` for testing on different mobile devices and IP other than localhosts. Find this out [here](https://github.com/teddziuba/django-sslserver "here")*


Sequence Diagram
------------- 

![Sample generated UML diagram](https://bramp.github.io/js-sequence-diagrams/<?xml version="1.0" encoding="utf-8" standalone="no"?><!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"><svg xmlns="http://www.w3.org/2000/svg" width="652" height="366" xmlns:xlink="http://www.w3.org/1999/xlink"><source><![CDATA[Javascript->Python(Django server): Make Ajax request
Note right of Python(Django server):Decodes the image \nusing pyzbar
Javascript-->Python(Django server): Send snapshot of the \nlive camera stream
Python(Django server)->>Javascript: Returns decoded barcode]]></source><desc></desc><defs><marker viewBox="0 0 5 5" markerWidth="5" markerHeight="5" orient="auto" refX="5" refY="2.5" id="markerArrowBlock"><path d="M 0 0 L 5 2.5 L 0 5 z"></path></marker><marker viewBox="0 0 9.6 16" markerWidth="4" markerHeight="16" orient="auto" refX="9.6" refY="8" id="markerArrowOpen"><path d="M 9.6,8 1.92,16 0,13.7 5.76,8 0,2.286 1.92,0 9.6,8 z"></path></marker></defs><g class="title"></g><g class="actor"><path d="M10,20C42.3,15.5 103.5,24.5 121.3,20.0C119.5,56.1 123.0,41.1 121.3,63.0C75.3,67.5 27.8,58.5 10.0,63.0C8.3,51.8 11.7,45.9 10.0,20.0" stroke="#000000" fill="#ffffff" style="stroke-width: 2;"></path><text x="20" y="44" style="font-size: 16px; font-family: danielbd;"><tspan x="20">Javascript</tspan></text></g><g class="actor"><path d="M10,303.375C57.4,307.8 63.7,298.9 121.3,303.4C123.0,336.1 119.5,327.7 121.3,346.4C102.9,341.9 27.8,350.8 10.0,346.4C8.3,313.8 11.7,310.3 10.0,303.4" stroke="#000000" fill="#ffffff" style="stroke-width: 2;"></path><text x="20" y="327.375" style="font-size: 16px; font-family: danielbd;"><tspan x="20">Javascript</tspan></text></g><path d="M65.6,63.0C75.2,188.8 56.0,194.0 65.6,303.4" stroke="#000000" fill="none" style="stroke-width: 2;"></path><g class="actor"><path d="M201.40625,20C350.8,28.4 313.9,11.6 411.4,20.0C409.6,30.3 413.1,26.9 411.4,63.0C371.7,71.4 361.0,54.6 201.4,63.0C199.7,52.7 203.1,40.3 201.4,20.0" stroke="#000000" fill="#ffffff" style="stroke-width: 2;"></path><text x="211.40625" y="44" style="font-size: 16px; font-family: danielbd;"><tspan x="211.40625">Python(Django server)</tspan></text></g><g class="actor"><path d="M201.40625,303.375C361.9,311.8 237.9,295.0 411.4,303.4C413.1,336.1 409.6,339.5 411.4,346.4C311.5,338.0 251.8,354.8 201.4,346.4C203.1,314.5 199.7,323.3 201.4,303.4" stroke="#000000" fill="#ffffff" style="stroke-width: 2;"></path><text x="211.40625" y="327.375" style="font-size: 16px; font-family: danielbd;"><tspan x="211.40625">Python(Django server)</tspan></text></g><path d="M306.4,63.0C316.0,239.6 296.8,151.0 306.4,303.4" stroke="#000000" fill="none" style="stroke-width: 2;"></path><g class="signal"><text x="104.953125" y="90.5" style="font-size: 16px; font-family: danielbd;"><tspan x="104.953125">Make Ajax request</tspan></text><path d="M65.6,106.0C164.7,96.4 267.9,115.6 306.4,106.0" stroke="#000000" fill="none" style="stroke-width: 2; marker-end: url(&quot;#markerArrowBlock&quot;);"></path></g><g class="note"><path d="M326.3828125,126C384.4,119.2 356.2,132.8 497.1,126.0C499.2,134.3 495.1,153.9 497.1,178.2C369.8,185.0 391.4,171.4 326.4,178.2C328.5,154.6 324.3,154.6 326.4,126.0" stroke="#000000" fill="#ffffff" style="stroke-width: 2;"></path><text x="331.3828125" y="145" style="font-size: 16px; font-family: danielbd;"><tspan x="331.3828125">Decodes the image</tspan><tspan dy="1.2em" x="331.3828125">using pyzbar</tspan></text></g><g class="signal"><text x="93.15625" y="196.09375" style="font-size: 16px; font-family: danielbd;"><tspan x="93.125">Send snapshot of the</tspan><tspan dy="1.2em" x="93.125">live camera stream</tspan></text><path d="M65.6,240.4C123.4,230.7 175.8,250.0 306.4,240.4" stroke="#000000" fill="none" style="stroke-width: 2; stroke-dasharray: 6, 2; marker-end: url(&quot;#markerArrowBlock&quot;);"></path></g><g class="signal"><text x="75.6328125" y="267.875" style="font-size: 16px; font-family: danielbd;"><tspan x="75.6328125">Returns decoded barcode</tspan></text><path d="M306.4,283.4C123.4,273.7 167.0,293.0 65.6,283.4" stroke="#000000" fill="none" style="stroke-width: 2; marker-end: url(&quot;#markerArrowOpen&quot;);"></path></g></svg>images/sample.svg)


End
----
