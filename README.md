# BASH Timelapse

BASH scripts that take timelapse photography as JPGs and assembles them into an fullsized and thumbnail MP4.

`timelapse_photo` takes photos using `fswebcam` and deletes old photos maintaining a maximum number of files and a minimum amount of hard drive space.

### Timelapse photo capture

- To install the prerequisite, `fswebcam`, execute the following or equivalent:
	
		sudo apt-get fswebcam`

- Edit `timelapse_photo` specifying the desired photo directory, photo resolution, maximum number of photos, minimum hard drive capacity, and camera rotation (orientation in degrees).

- Edit `timelapse_photo.crontab` specifying the path to the `timelapse_photo` executable, as well as desired schedule (see `man 5 crontab` for documentation of schedule format).

- To enable the scheduled execution of the timelapse photo script, execute:

		crontab timelapse_photo.crontab
		
### Timelapse video creation

- Edit `timelapse_video` specifying the photo directory and desired output directory.

- Execute: `timelapse_video`