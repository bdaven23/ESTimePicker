ESTimePicker
============

A custom time picker just like the [Google Calendar Android App](https://www.google.nl/search?q=google+calendar+time+picker&espv=210&es_sm=91&source=lnms&tbm=isch&sa=X&ei=hXPeUsHwLuLCyQOP_YHICg&ved=0CAkQ_AUoAQ&biw=1756&bih=1047)

## Example
<br>
![Example](https://raw.github.com/e-sites/ESTimePicker/master/Assets/example.gif)


## Features

- Choose your own colors (background, highlight, selection, text)
- Choose your own font
- Both 24 hour notation and AM/PM
- Snap the minute view
- Completelly usable in your own viewcontroller or view

## Installation
Use cocoapods:

	pod 'ESTimePicker', :git => 'https://github.com/e-sites/ESTimePicker'

## Implementation

	- (void)viewDidLoad
	{
    	ESTimePicker *timePicker = [[ESTimePicker alloc] initWithDelegate:self]; // Delegate is optional
    	[timePicker setFrame:CGRectMake(10, 100, 300, 300)];
    	[self.view addSubview:timePicker];
	}
	
	- (void)timePickerHoursChanged:(ESTimePicker *)timePicker toHours:(int)hours
	{
    	[hoursLabel setText:[NSString stringWithFormat:@"%i", hours]];
	}

	- (void)timePickerMinutesChanged:(ESTimePicker *)timePicker toMinutes:(int)minutes
	{
    	[minutesLabel setText:[NSString stringWithFormat:@"%i", minutes]];
	}
    
## Dependencies
This class uses the `ESMathUtils` class (which is included)