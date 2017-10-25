# Der Date-Time-Picker als Standalone

Originally designed for Bootstrap Material, the V2.0 is now completely standalone and responsive.
Originally forked by T00rk.

## UM AUF DEUTSCH ZU STELLEN:
**It's a multilingual version, you can change the language in the .js file (line 6)!**


### Prerequisites

* jquery [http://jquery.com/download/](http://jquery.com/download/)

* momentjs (with locales!) [http://momentjs.com/](http://momentjs.com/)

* Google Fonts (place in <head> before the datetimepicker.css):

`<link href='http://fonts.googleapis.com/css?family=Roboto:400,500' rel='stylesheet' type='text/css'>`

`<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">`


### Example

![](http://pichoster.net/images/2016/05/31/687474703a2f2f692e696d6775722e636f6d2f4d66375234314c2e706e67IjRO.png?raw=true)
![](http://pichoster.net/images/2016/05/31/device-2015-04-19-163042-480x708.png?raw=true)

### Usage

Use standard settings:
        `$('#your-date-input-field').bootstrapMaterialDatePicker();`
	
Define some extra settings:
        `$('#your-date-input-field').bootstrapMaterialDatePicker({
		format : 'dddd, DD. MMMM YYYY - HH:mm',
		nowButton : true,
		clearButton : false,
		nowText : 'Jetzt'
	});`


	
### Parameters

| Name				| Type							| Description									|
| ----------------- | ----------------------------- | --------------------------------------------- |
| **format**		| String						| MomentJS Format								|
| **shortTime**		| Boolean						| true => Display 12 hours AM|PM 				|
| **minDate**		| (String\|Date\|Moment)		| Minimum selectable date						|
| **maxDate**		| (String\|Date\|Moment)		| Maximum selectable date						|
| **currentDate**	| (String\|Date\|Moment)		| Initial Date									|
| **year**			| Boolean						| true => Has Yearpicker						|
| **date**			| Boolean						| true => Has Datepicker						|
| **disabledDays**	| Array							| Array containing day indices (1-7) to disable	|
| **time**			| Boolean						| true => Has Timepicker						|
| **clearButton**	| Boolean						| true => Show Clear Button						|
| **nowButton**		| Boolean						| true => Show Now Button						|
| **switchOnClick**	| Boolean						| true => Switch view on click (default: false) |
| **cancelText**	| String						| Text for the cancel button (default: Cancel)	|
| **okText**		| String						| Text for the OK button (default: OK)			|
| **clearText**		| String						| Text for the Clear button (default: Clear)	|
| **nowText**		| String						| Text for the Now button (default: Now)		|
| **triggerEvent**		| String						| Event to fire the calendar (default: focus)		|
| **monthPicker**	| Boolean						| true => Act as monthpicker (hide calendar) (default: false) |



### Events

| Name				| Parameters				| Description										|
| ----------------- | ------------------------- | ------------------------------------------------- |
| **beforeChange**	| event, date				| OK button is clicked								|
| **change**		| event, date				| OK button is clicked and input value is changed	|
| **yearSelected**	        | event, date			        | New year is selected								|
| **dateSelected**	| event, date				| New date is selected								|
| **open**	        | event				        | datepicker is opened								|
| **close**	        | event				        | datepicker is closed								|


### Methods

        $('input').bootstrapMaterialDatePicker('setDate', moment());

| Name				| Parameter					| Description					|
| ----------------- | ------------------------- | ----------------------------- |
| **setDate**		| (String\|Date\|Moment)	| Set initial date				|
| **setMinDate**	| (String\|Date\|Moment)	| Set minimum selectable date	|
| **setMaxDate**	| (String\|Date\|Moment)	| Set maximum selectable date	|
| **destroy**		| NULL						| Destroy the datepicker		|