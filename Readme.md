WiFi module
==============

Provides connected WiFi network information gathered by `/System/Library/PrivateFrameworks/Apple80211.framework/Versions/Current/Resources/airport -I` and various WiFi preferences

Client Preferences
---

It is possible to enable the collection of known networks on clients using the preference domain `MunkiReport` with boolean key `wifi_known_networks_enabled` set to `true`. Alternatively, you can run `sudo defaults write /Library/Preferences/MunkiReport.plist wifi_known_networks_enabled -bool true` on the client. Collection of this data is only supported on macOS 11 and newer.

Remarks
---

* 'init' state indicates that WiFi is on, but not connected to any networks


Table Schema
---

* agrctlrssi (integer) Aggregate RSSI (decibels) 
* agrextrssi (integer) Aggregate external RSSI (decibels)
* agrctlnoise (integer) Aggregate noise (decibels)
* agrextnoise (integer) Aggregate external noise (decibels)
* state (string) WiFi state (running, init, off)
* op_mode (string) Access point mode
* lasttxrate (integer) Last transmit rate (Mbps)
* lastassocstatus (string) Last association status
* maxrate (integer) Maximum supported transmit rate (Mbps)
* x802_11_auth (string) Type of authentication
* link_auth (string) Link authentication type
* bssid (string) Access point's BSSID
* ssid (string) SSID or name of the connected wireless network
* mcs (string) Modulation and Coding Scheme
* channel (string) Channel of wireless network
* snr (integer) Signal to noise ratio
* known_networks (medium text) JSON string detailing known wireless networks