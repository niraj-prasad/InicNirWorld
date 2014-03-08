# AnimatedTable: (iOS) Module

## Description
Lets you design table with animated rows when scrolled.

## Accessing the AnimatedTable Module

To access this module from JavaScript, you would do the following:

	var AnimatedTable = require("inic.animated.table");

The AnimatedTable variable is a reference to the Module object.	

## Reference

You can use most of the attributes and methods provided in Titanium API documentation for TableView.

## Crete AnimatedTableView

	var animatedTableView = animatedTable.createView({
		backgroundColor : 'transparent',
		width : Ti.UI.FILL,
		height : Ti.UI.FILL
	});

## Creating Rows
	
	var data = [];
	
	for (var i = 0; i < 100; i++) {
		//----------------- Creating Row  ---------------------------------------------
		var row = animatedTableView.createRow({
			backgroundColor : getColorCode(),
			width : Ti.UI.FILL,
			height : 100
		});
	
		//----------------- Creating an ImageView  ------------------------------------
		var leftImageView = Ti.UI.createImageView({
			image : '/images/smileicon.png',
			width : 64,
			height : 64,
			left:5
		});
		//----------------- Creating a Title Label  -----------------------------------
		var titleLabel = Ti.UI.createLabel({
			text : 'Row ' + i,
			color : '#FFFFFF',
			font : {
			fontSize : 18
			},
			height : Ti.UI.SIZE,
			width : Ti.UI.SIZE,
			left : 130,
			textAlign : 'center'
		});
		row.add(leftImageView);
		row.add(titleLabel);
		data.push(row);
	};
	
## Setting Data for AnimatedTableView
	animatedTableView.setData(data);
	
## Setting Animation for Every Visible Row using following style parameters
	1. GROW														  
	2. CARDS													  
	3. CURL														  
	4. WAVE														  
	5. FLIP														  
	6. FLY														  
	7. SIMPLIFIED-FLY											  
	8. REVERSE-FLY												  
	9. HELIX													  
	10. FAN														  
	11. PAPERCUT												  
	12. TWIRL													  
### Setting Upward Animation

	animatedTableView.setUpwardAnimation({
		style : 'GROW',
		duration : 0.5
	});
### Setting Downward Animation

	animatedTableView.setDownwardAnimation({
		style : 'wave',
		duration : 0.5
	});

## Usage

Please follow the example app.js provided with the module.

## Author
Niraj Kumar
(niraj.prasad@indianic.com)

## Feedback and Support
Please direct all questions, feedback, and concerns to [niraj.prasad@indianic.com](mailto:niraj.prasad@indianic.com?subject=iOS%20AnimatedTable%20Module).

## License
Copyright(c) 2010-2013 by Appcelerator, Inc. All Rights Reserved. Please see the LICENSE file included in the distribution for further details.
