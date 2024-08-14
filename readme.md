# Home Assistant Configuration
## About
I use this repository to store my personal Home Assistant configuration - mostly as a last resort means of backup, but if it inspires anyone to try something new, I'd be very happy to be of service. The idea is also to keep some sort of history about my opinions of different devices and services, as I'll intend to write a sentance or two about the tools that I am using. 

## Smart Home Philosophy
The idea is to create a smart, local and private home. The goal of reaching 100% privacy and being fully local will probably never be fully reached, as some services that I use still relies on cloud services, and I value them too much to get rid of them completely. Nevertheless, if it can run locally, it will. 

Another big guideline that I live by is that the home should still *work* if everything automated fails. The lights should still turn on, the curtains should go up, and so on. Home automation exists to easen our lives, not to make ourselves dependant on it. 

## Tools
### Hosting
I use a Dell OptiPlex 9020 SFF, where Home Assistant runs in a VM within Proxmox. It's a great machine that often can be found used for the same price as a Raspberry Pi, but with way more power.

### Connectivity
- [SMLIGHT SLZB-06 Zigbee Adapter](https://smlight.tech/product/slzb-06/) - The Zigbee adapter of choise for me. It is powered over PoE which enables me to put it in the middle of the house, which a USB dongle does not. I have about 60 Zigbee devices and it has been rock solid so far.

### Cameras
- [Reolink RLC-410](https://reolink.com/product/rlc-410/) - Some people are reporting issues using Reolink cameras with Frigate and thus they are not recommended hardware for Frigate. However, I personally never had any problems and it's been very stable for me. Powered over PoE.
- [TP-Link C200](https://www.tp-link.com/se/home-networking/cloud-camera/tapo-c200/) - Although an indoor camera I had one mounted outside under a roof for over a year, and it seems to be doing fine. However, I don't recommend using wifi cameras as it can occasionally drop out.

## Sensors
### Lights
- [Philips Hue](https://www.philips-hue.com/sv-se/products/smart-light-bulbs) - Zigbee. Pretty much an industry best. Has been very reliable for me. Dims very low.
- [IKEA Trådfri](https://www.ikea.com/se/sv/cat/smarta-led-lampor-36813/) - Zigbee. Works well and you get a lot for what you pay. Doesn't dim as low as Hue lights.
### Switches
- [IKEA Trådfri](https://www.ikea.com/se/sv/p/tradfri-tradloest-uttag-smart-90356166/) - Zigbee. Cheap and works very well. No power monitoring.
- [Shelly Plus Plug S](https://www.shelly.com/en/products/shop/shelly-plus-plug-s) - Wifi. For where I need power monitoring.
### Motion Sensors
- [IKEA Trådfri](https://www.ikea.com/se/sv/p/tradfri-tradloes-roerelsesensor-vit-70429913) - Zigbee. The original IKEA motion sensor which will probably be discontinued soon. Has a refresh rate of about 4 minutes, which greatly limits its usecases. However, I've found it to have quite a good range. 
- [IKEA Vallhorn](https://www.ikea.com/se/sv/p/vallhorn-tradloes-roerelsesensor-smart-vit-90504341/) - Zigbee. IKEAs new motion sensor. It has way better refresh rate, about 20 seconds. However, the range seems to be very short, about 2 meters for it to be reliable. For that reason, I wouldn't recommed this one.
- [Philips Hue Motion Sensor](https://www.philips-hue.com/sv-se/p/hue-hue-motion-sensor/8719514342125) - Zigbee. Pretty much the best consumer grade motion sensor with Zigbee. Refreshes almost instantly, works on long range, measures lux. Worth its quite high price.
- [Philips Hue](https://www.philips-hue.com/sv-se/p/hue-utomhussensor/8719514342262) - Zigbee. See above.
### Energy Monitoring
- [Frient Smart Energy Meter](https://www.kjell.com/se/produkter/smarta-hem/smarta-sensorer/smarta-energimatare/frient-smart-energimatare-for-elcentral-p52023) - Zigbee. I had to find a Zigbee meter since my electricity cupboard doesn't have a stable lan/wifi connection. This one also runs on AA batteries, which is neat. It counts the light impulses on the meter. So far I've found it to be very accurate - it has only differed around $1 from the actual invoice.
### Buttons & Controls
- [Philips Hue Dimmer Swith](https://www.philips-hue.com/sv-se/p/hue-dimmer-switch/8719514274617#overview) - Zigbee.
- [IKEA Styrbar](https://www.ikea.com/se/sv/p/styrbar-fjaerrkontroll-smart-rostfritt-stal-10435224/) - Zigbee.
### Door and Window Sensors
- [IKEA Parasoll](https://www.ikea.com/se/sv/p/parasoll-doerr-foenstersensor-smart-vit-80504308/) - Zigbee.
- [Aqara Door and Window Sensor](https://www.aqara.com/en/product/door-and-window-sensor/) - Zigbee.
### Leakage Sensors
- [IKEA Badring](https://www.ikea.com/se/en/p/badring-water-leakage-sensor-smart-60504352/) - Zigbee.
- [Aqara Water Sensor](https://www.aqara.com/en/product/water-sensor/) - Zigbee.


## Services
### Addons
- Advanced SSH & Web Terminal - Used for SSH access.
- ESPHome - Mostly used for experimentation. I used to do water usage monitoring with ESPHome and a magnet sensor, but it is not possilbe anymore since my meter was changed. 
- Frigate - NVR for cameras, using AI detection.
- Fusion - Dashboard addon. I mainly used this before sections was released in Core.
- Glances - For hardware monitoring.
- Home Assistant Google Drive Backup - Cloud backups.
- Mosquitto Broker - For MQTT connectivity.
- MQTT Explorer - Great tool for inspecting MQTT events.
- Samba share
- Studio Code Server
### Integrations
- AccuWeather
- Alarmo
- Blitzortung
- Browser mod
- Custom Panel
- Electricity Maps
- EspHome
- File
- FontAwesome
- Frigate
- Fully Kiosk Browser
- Garmin Connect
- Glances
- Google Calendar
- Google Cast
- Google Sheets
- Google Tasks
- Google Translate TTS
- Goove lights local
- HACS
- HASS.Agent
- Home Connect
- InfluxDB
- Local To-do
- Lynk & Co
- Met.no
- MQTT
- Ping (ICMP)
- Pollenprognos
- Proximity
- Proxmox VE
- Radio Browser
- resrobot
- RESTful
- Roborock
- Samsung Smart TV
- Shelly
- Speedtest.net
- Spook
- Spotify
- Strava
- Sun
- System Monitor
- Tasmota
- Telegram bot
- Todoist
- Uptime
- Watchman
- Waze Travel Time
- WiZ
- Workday
- Zwift
### Custom Integrations

