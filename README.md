# hue-hacking: Hue Control Library #
***
hue-hacking is a javascript library designed to control the Philips Hue smart LED bulb system.

For more information on the Philips Hue bulbs and wireless bridge system, visit [meethue.com](http://meethue.com).

_Initial concept and startup work inspired by [Ross McKillop's post](http://rsmck.co.uk/hue)._

## Getting Started ##
Once you've followed the instructions with your Hue starter kit and you have your lamps working through the web interface or smartphone app, it's time to configure your copy of hue.js.

1. Generate and save your MD5 hash (any [MD5 generator](http://www.miraclesalad.com/webtools/md5.php) will do).
Be sure to save your hash and the passphrase used to generate it in a safe place.

2. Find the IP address of your Hue wireless bridge. This can be gathered in a number of ways, including the
meethue.com control panel, https://www.meethue.com/en-US/user/preferencessmartbridge, by clicking on the "Show me more" link. See [screenshot](http://imgur.com/yDhCp) for an example.

3. Call the setIpAndApiKey() function, passing in the IP address and the API key value generated and registered with the hub.

5. __Optional:__ If you have more than 3 bulbs (the number included in the Hue starter kit), call the setNumberOfLamps() function, passing in the total number of lamps available, prior to using the lamp control functions.

## Included Files ##

### colors.js ###
Provides convenience functions to convert between CSS-style hex color values, their corresponding RGB color values, and the CIE 1931 X,Y color coordinates supported by the Hue lamp system.

### hue.js ###
Provides control functions to control either single lamps, groups of lamps, or all available lamps. Lamps can be toggled (on/off), flashed for a short or long time, and have their color changed. See code for API documentation.

### sample ###
Sample html page that uses RequireJS, jQuery, jQuery UI to demo basic lamp control options. Not intended to be an exhaustive feature demo. __Note:__ Setup detailed above must be completed in the hue.js file in sample/hue.

### tests ###
QUnit test suites for colors.js and hue.js. Each test is contained within an html page; simply open the page locally in a browser to run tests. __Note:__ Setup detailed above must be completed in the hue.js file to have tests run.

&copy; 2013 Bryan Johnson; Licensed MIT.
