# Timeselector

A simple jQuery plugin for time selection in form.

**Current version:** [1.0.0](https://github.com/nicolaszhao/timeselector/archive/v1.0.0.tar.gz)

## Usage
Include jQuery and the plugin on your page. Then select a input element and call the timeselector method on DOM ready.

	<script src="jquery.js"></script>
	<script src="jquery.timeselector.js"></script>
	<script>
		$(function() {
			$('[name="time"]').timeselector();
		});
	</script>
	<input type="text" name="time" />

If you want an initial "starting time" (what would make sense with the **step** option for minutes, see below) you should set this as the ```input```'s value, e.g.:

	<input type="text" name="time" value="08:15" />
	

## Restrictions

Due to implementation details you currently cannot have more than one timeselector on the same page (maybe you can if your browser applies some non-standard intelligence) since the checking logic for ```_checkExternalClick``` in ```src/jquery.timeselector.js``` depends on an element id that can [per definition](http://www.w3.org/TR/html401/struct/global.html#h-7.5.2) not exist more than one time in the same document. 


## Options
**hours12** (default: true)   
Type: Boolean   
Decide between AM/PM / 12 hour (setting: true) or 24 hour (setting: false) clock.

***

**step** (default: 1)   
Type: Number   
The step size to adjust minutes when click the timeselector buttons or press the UP/DOWN KEY on the keyboard. You should set a starting value for your HTML input field (see Usage) if you want to achieve steps like "08:15 - 08:30 - 08:45" and so on.

## Methods
**option( options )**  
Returns: jQuery   
Set one or more options for the timeselector.
	
* **options**   
	Type: Object   
	A map of option-value pairs to set.
	
**Code example:**
	
	$('[name="time"]').timeselector('option', {"hours12": false});

*Note the double quotes around "hours12" which are not necessary for timeselector but are obligatory for correct [JSON](http://en.wikipedia.org/wiki/JSON) syntax which lies behind here*

***

**refresh()**   
Returns: jQuery   
When the input value is set manually, need to call this method to manually update the timeselector and input value if the value is valid.

**Code example:**
	
	$('[name="time"]').val('13:00').timeselector('refresh'); // input value will update to '01:00 PM'

## Keyboard interaction
* **UP**: Increment the minute by one step.
* **DOWN**: Decrement the minute by one step.
* **PAGE UP**: Increment one hour.
* **PAGE DOWN**: Decrement one hour.
* **ESCAPE**: Close the timeselector without selection.
	
## Theming
If timeselector specific styling is needed, the following CSS class names can be used:
* `timeselector`: The outer container of the timeselector.
	* `timeselector-item`: The outer container of the hour or the minute section. The hour section will additionally have a `timeselector-hour` class and the minute section will additionally have a `timeselector-minute` class. 
		* `timeselector-button`: The button controls used to increment and decrement the time's value. The up button will additionally have a `timeselector-up` class and the down button will additionally have a `timeselector-down` class.
		* `timeselector-value`: The element to display the time's value.
	* `timeselector-separator`: The separator of time.

## Dependencies
### Required
[jQuery, tested with 1.10.2](http://jquery.com)

## License
Copyright (c) 2014 Nicolas Zhao; Licensed MIT
