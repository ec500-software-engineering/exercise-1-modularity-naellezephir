# ReadMe

## Architecture Diagram of Heart Monitor
	-[Link to Diagram, credit: Miguel Mark](https://github.com/mmark9/ec500_spring19_misc/blob/prototype/heart_monitor/ec500_heart_monitor_class_diagram.png)

## Explanation of Architecture
	- Our first full implementation as a team already implemented asychronous design using threads and queues. Each of the modules does its work in its own thread, threads for the different sensors to read "data" and a thread for the ai data processor to process the information before displaying information on the display.

## Pros and Cons
	- Pro: using queues means we can give priority to different sensors based on the data. If a patient is admitted for high blood pressure, you can place priority on the blood pressure sensor and its readings, and have more frequent notifications.
	- Con: deciding what size queue to use since if the queue gets too large it could take up a lot of space. If it's a fixed size you could have more processes that you want to complete than space in the queue and it could overflow.

## What Would I Improve
	- I would try using a callback functions and upon the event of the process being finished, display the information
	- there was also a small fix that the data processor needed to include processing criteria for the blood oxygen data