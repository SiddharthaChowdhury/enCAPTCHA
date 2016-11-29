<a name="intro"></a> 
# En-captcha 
![Image missing](https://github.com/SiddharthaChowdhury/enCAPTCHA/blob/master/img.webp)

A "Completely Automated Public Turing test to tell Computers and Humans Apart" aka CAPTCHA, build on JavaScript. Simple integration to prevent bots from submiting your form

##FEATURE

- Control on number of wrong attempt (Reloads the page on attempt expires)
- Auto reload captcha after specific interval
- Shortcut detection, i.e. reloads captcha if any shortcut is detected (like ctrl + V or RightClick + paste)

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
		var obj = new Encaptcha({
			config:{
				container: '#captcha2',
				reload_interval: 70,
				themeColorHex: '#E6E6E6',
				reloadBtn_text: '<i class="fa fa-refresh" aria-hidden="true"></i> Refresh',
				allowed_attempt: 5,
				form: '#form1'
			},
			onSuccess: function(){
				console.log("YAY! success")
			},
			onFailure: function(){
				console.log('Hi I might be a robot~ T_T ')
			}
		});
	});		

<a name="CONFIGURATION"></a>
##CONFIGURATION / Options 

* **`char_count:`** Strength of CAPTCHA (ie number of letters in CAPTCHA image). *Recommended-value: 5 or 6* . It cannot be less than 5
* **`container:`**  DOM element where you want the CAPTCHA to be displayed. Value can be `id` or `class` of the element. Please make sure this CAPTCHA container is **empty**.  *Example value:* `'#container'` or `'.container'` .  
* **`reload_interval:`** *[OPTIONAL]* The CAPTCHA must reload after certain seconds so this value should contain an integer. *Recommended-value: 30 or 60*. Default is 45
* **`allowed_attempt:`** *[OPTIONAL]* Number of times a user is allowed to enter wrong CAPTCHA. Accepts a number. Default - infinite
* **`onSuccess:`**  *[OPTIONAL]* The value has to be an anonymous function which will execute when the CAPTCHA is successfully validated.
* **`onfailure:`**  *[OPTIONAL]* The value has to be an anonymous function which will execute when the CAPTCHA validation FAILS each time.
* **`form:`**  *[OPTIONAL]* This value has be the form identifier which you want to protect from bots. Example: '#form_id' or '.form_class'


<a name="browser"></a>
##Browser support 

Tested in all modern browser ( Chrome, Opera, FF, Safari ) Doesnt work in old IE

<a name="dependency"></a>
##Dependency

NO Dependency. Though it is not dependent on any 3rd party library or framework, but if you are using enCAPTCHA on any form which is NOT asynchronously submitted, it is recommended to have jQuery, will add an extra layer of security to enCAPTCHA.

##Resources##

- Online [Image Cropping](http://croppiconline.com/en)
- Online [Sprite generator](https://www.leshylabs.com/apps/sstool)
- Online [OCR](http://www.ocrconvert.com/)
- Online [Image compress](https://tinypng.com/)
- Online [Image metadata viewer](http://regex.info/exif.cgi)
- Online [Base64](http://jsfiddle.net/handtrix/xztfbx1m/)
 
##CONTENT

- [Intro](#intro)
- [Setup-guide](#setup)
- [Example](#example) 
- [Configuration / Options](#CONFIGURATION)
- [Dependency] (#dependency)
- [Browser support](#browser) 
