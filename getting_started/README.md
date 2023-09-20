# Getting started

## Where to start?

- If you still need to build the kit, go to [/building_instructions](/building_instructions) first.

- Did you purchage an fully assembled access point, you can skip the steps about flashing, because it already contains the right firmware.

## Flashing the ESP32-S3

So, you have an empty access point. First we flash the ESP32-S3, and from there on, it is capable to flash the ESP32-C6 by itself.

To flash the ESP32-S3, you have a few options:

1. Use PlatformIO and VSCode and compile the firmware yourself. Although it's a bit more complicated to get this running, this is the best choice if you want to tinker with the code yourself, or want to make additions to the software. Choose the `ESP32_S3_16_8_YELLOW_AP` environment, which is compatible with the Mini AP v3.

2. The easy method: use https://install.openepaperlink.de to use the web flasher. Connect the access point to your computer with an USB-C cable. On the web flasher page, choose 'Mini AP v3', blick 'connect', and choose the right COM-port. If you click 'install openepaperlink', the ESP32-S3 gets flashed. After flashing, you can select your wifi network/password, to connect the AP with your WiFi network. When that's successfull, choose 'visit device' to redirect to the OpenEpaperLink main screen and skip the next step.

## Connect to WiFi

Once the firmware is there, you can update the firmware over the air. By choosing 'AP config' -> 'update', you can see if there is a newer release, and apply the new firmware from there without a connection to your computer. From now on, you can simple connect the Access Point to any USB charger.

<img src="/getting_started/init.jpg"><br>

If all went well, you will see this screen. Now, to configure the WiFi settings, connect to the OpenEpaperLink WiFi network with your phone or notebook, and visit http://192.168.4.1/setup 

<img src="/getting_started/IMG_3950.jpeg" width="400"><br>

Enter your SSID and password and save the settings.

<img src="/getting_started/IMG_3952.jpeg"><br>

Success! You can go to the Access Point main screen by visiting the ip-adres shown on the screen in you browser.

## Flashing the ESP32-C6

We still need to flash the ESP32-C6. For that, from the Access Point main screen, go to 'AP config' -> 'update' -> 'advanced options' -> 'Update ESP32-C6'.
Finished? Congratulations, you have a running Access Points

## Connecting the tags

Take a (programmed) tag, and insert the batteries. This may sound easier than it is, in reality. See, these tags are cheap. They don't reset automatically when the voltage drops; if you replace batteries, you'll sometimes need to reset them (by shortening out the contacts), and you want to insert the batteries in a swift motion, so that they make contact and stay connected. You can use the battery cover to pop the batteries in.

If you want to make sure you'll reset the tag properly, the easiest way to drain the internal capacitors is to shorten the them using a battery. A battery inserted in reverse will shorten the contacts. On tags with multiple batteries: don't keep batteries in the bay with one battery shorting out the contacts; they're wired in parallel.

Now that you've successfully powered on your tag, it's time to see if it's showing up on the AP-webinterface. A few seconds after the 'Waiting for data...' screen is shown on a tag, it should show up on the accesspoint.
Select the tag in the webinterface, choose some content, and the tag should update the next time it checks in!

