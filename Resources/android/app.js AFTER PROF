var win=Ti.uI.createWindow({
backgroundColor: '#ffffff',
layout:'vertical'
});
	
var timeVeiw=Ti.UI.createView({
top:0,
width:'100%',
Height:'30%',
backgroundColor: '#1C1C1C'	
});

var label= Ti.UI.createLabel({
	color: '#404040',
	text: 'READY?',
	height:Ti.UI.SIZE,
	textAlign: 'center',
	verticalAlign: Ti.UI.TEXT_VERTICAL_ALIGNMENT_CENTER,
font:{
fontSize: '55sp',
fontWeight: 'bold'
}
});

var buttonsVeiw=
Ti.Ui.createView({
	width: '100%',
	height: '10%',
	layout: 'horizontal'
});

var ButtonStartLap =
Ti.UI.createButton({
 title: 'GO!',
 color: '#COBFBF', 
 width: '50%',
 height: Ti.UI.FILL,
 backgroundColor: '#727F7F',
 font: {
 	fontSize: '25sp',
 	fontWeight: 'bold'
  }
 });
  
 var ButtonStopReset = Ti.UI.createButton({
 	title: 'STOP',
 	color: '#COBFBF',
 	width: '50%',
 	height: Ti.UI.FILL,
 	backgroundColor: '#404040',
 	font: {
 		fontSize: '25sp',
 		fontWeight: 'bold'
 	}
 });
 
 buttonsView.add(ButtonStopReset);
 buttonsVeiw.add(ButtonStartLap);
 win.add(buttonsVeiw);
 
ButtonStartLap.addEventListener('click', function(e) {
 	stopWatch.start();
 	}

ButtonStopReset.addEventListener('click', function(e) {
	stopWatch.stop();
	label.text='READY?';
	}
	 
var Stopwatch = require('stopwatch');

function stopwatchListener(watch) {
	label.text= watch.toString();
}

var stopWatch= new Stopwatch(stopwatchListener,10);

var isRunning=false;
buttonStartLap.addEventListener('click', function(e) {
if (isRunning) {	
Ti.API.info(stopWatch.toString());
} else {
	isRunning=true;
	buttonStartLap.title='LAP!';
	buttonStopReset.title='STOP';
	stopWatch.start();
	}
});	

var table=Ti.UI.createTableView({
	width:'100%',
	height:Ti.UI.FILL,
	backgroundColor: '#COBFBF'
	});
	
	win.add(table);
	
	buttonStartLap.addEventListener('click', function(e){
		if (isRunning){
			var row=
	Ti.UI.createTableVeiwRow({
		title:stopWatch.toString(),
		color:'#404040',
		className: 'lap',
		leftImage:	'images/lap.png',
		font: {
			fontSize: '24sp',
			fontWeight: 'bold'
			}
			});	
			
			table.appendRow(row);
		}else{
			
		buttonStopReset.addEventListener('click',function(e)	{
			if (isRunning){
				buttonStartLap.title='GO!';
				buttonStopReset.title=	'Reset';
			stopWatch.stop();
			isRunning=false;
			}else{
				table.setData({});
				stopWatch.reset();
				label.text='READY?';
				}
				});
buttonsVeiw.add(buttonStartLap);				

win.add(buttonvseiw);			
win.open();