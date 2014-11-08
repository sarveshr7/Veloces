Veloces
=======

An Efficient I/O Scheduler for Solid State Devices.
The Veloces I/O scheduler is a scheduler that performs scheduling, using concepts such as read preference, front merging and bundling of write requests.

Applying patch : 
	
	patch -p1 < pathtopatch/veloces

Compile linux kernel.

Selecting the scheduler : 
	
	cat /sys/block/sdX/queue/scheduler

		If the patch has been applied and kernel has been compiled correctly, then this command would show 'veloces' in the scheduler list. 
		*sdX - select the appropriate device for which scheduler is to be selected

	echo veloces > /sys/block/sdX/queue/scheduler

