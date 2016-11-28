<a name="intro"></a> 
# En-captcha 
![Image missing](https://github.com/SiddharthaChowdhury/enCAPTCHA/blob/master/img.webp)

A "Completely Automated Public Turing test to tell Computers and Humans Apart" aka CAPTCHA, build on JavaScript, this plugin requires no dependencies. A simple integration to prevent bots from submiting your form

##FEATURE

- Control on number of wrong attempt (Reloads the page on attempt expires)
- Auto reload captcha after specific interval
- Shortcut detection, i.e. reloads captcha if any shortcut is detected (like <ctrl> + V or RightClick + paste);
- Option to add icon and to change CAPTCHA theme, manually.
- Added (class) identifier to the major elements of CAPTCHA, for fine grain UI customisation.

##CONTENT

- [Intro](#intro)
- [Setup-guide](#setup)
- [Example](#example) 
- [Configuration / Options](#CONFIGURATION)
- [Dependency](#dependency)
- [Browser support](#browser) 


<a name="setup"></a>
##SETUP-GUIDE 

**`PLEASE NOTE`** *`encaptcha.min.js`* and *`encaptcha.js`* in directory **`/dist`** is always a stable version of en-captcha

- Clone/Download the repo in your local system
- Extract the `encaptcha.min.js` or `encaptcha.js` from the dir **`/dist`** and put it your project
- Once you already have the plugin (the `.js` file) in your project
- Write a script to configure and display the captcha. To do so (Refer the  [Example](#example) given below )   
- Create an `Encaptcha` object say `en-obj` and pass in the `configuration` explained below in [CONFIGURATION section](#CONFIGURATION)
- Execute `en-obj.run()` to start the captcha.

<a name="example"></a>
####EXAMPLE 
	
	$(document).ready(function(){
		var obj1 = new Encaptcha({
			config:{
				container: '#captcha1',
				reload_interval: 10, // optional
				reloadBtn_text: '<i class="fa fa-refresh" aria-hidden="true"></i> Refresh', // optional
				allowed_attempt: 5 //optional,
				themeColorHex: '#E6E6E6', //optional
			}
		});
		obj1.start();
	});		

<a name="CONFIGURATION"></a>
##CONFIGURATION / Options 

* **`container:`**  DOM element where you want the CAPTCHA to be displayed. Value can be `id` or `class` of the element. Please make sure this CAPTCHA container is **empty**.  *Example value:* `'#container'` or `'.container'` .  
* **`reload_interval:`** The CAPTCHA must reload after certain seconds so this value should be an integer. *Recommended-value: 30 or 60* 
* **`onSuccess:`**  *[OPTIONAL]* The value has to be an anonymous function which will execute when the CAPTCHA is successfully validated.
* **`onfailure:`**  *[OPTIONAL]* The value has to be an anonymous function which will execute when the CAPTCHA validation FAILS.

---------------------------------------------------

**`object.start()`** Is REQUIRED to run the captcha.

<a name="browser"></a>
##Browser support 

Tested in all modern browser ( IE-9+, Chrome, Opera, FF, Safari )

<a name="dependency"></a>
##Dependency

NO Dependency. It is **NOT** dependent on any library/framework like JQuery or as such.

##Resources##

 Online [Image Cropping](http://croppiconline.com/en)

 Online [Sprite generator](https://www.leshylabs.com/apps/sstool)

 Online [OCR](http://www.ocrconvert.com/)

 Online [Image compress](http://optimizilla.com)

 Online [Image metadata viewer](http://regex.info/exif.cgi)

 Online [Base64](http://jsfiddle.net/handtrix/xztfbx1m/)
 
##CONTENT

- [Intro](#intro)
- [Setup-guide](#setup)
- [Example](#example) 
- [Configuration / Options](#CONFIGURATION)
- [Dependency] (#dependency)
- [Browser support](#browser) 
