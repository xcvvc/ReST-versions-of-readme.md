pics project
============

=========================================
archiving a .jpg album with legacy iPhoto
=========================================

These scripts allow me to reach out into my older iMac archive and pull a collection of small (thumb), medium and high resolution images from an iPhoto folder.  I can then burn a cd or dvd (or a drive) and send the photos off to the destination.

All of this flexibility is due to the [older] use of XML to contain the archive details at the location:

lg -> Pictures -> iPhoto Library -> AlbumData.xml

file instructions.txt is an overview for the sequence to run scripts. Practice with a small collection of 3-4 pictures in 2-3 iPhoto albums using a copy of the original scripts be accustomed to the changes to make in the scripts.

When hearing on the radio a while ago that iMacs would no longer install iPhoto, I became very happy that I had put the included perl scripting to use on my older equipment.

As was my circumstance, I have an archive of 8,000 photos, scanned from silver-halide negative and slide.


========================================
sequence  (pasted from instructions.txt)
========================================

Each picture is saved on an external usb disk in three resolutions, in subdirectories with example files named:  s_filename.jpg, m_filename.jpg, and filename.jpg. (thumb, medium, and large)

iPhoto

Drag and drop desired pictures into iPhoto albums. Album names become .txt files later, so no spaces or special characters.

xmlgrab.plx::

    correct album names in the script to those needed for .txt list.
    One .txt for each album.

1_fav_pic.plx::

    reads fav_pic.txt and writes fav_pic.command
    s/s(.+)\.jpg/$1/;
    mv $_ favorites/$_


end_push.plx::

    only s named small files should be in iPhoto
	
    XML file: /Users/lg/Pictures/iPhoto Libary/AlbumData.xml
    $bigdir:	/Volumes/LaCe Disk/Desktop Folder/pics/big
    $capacity
    $title		(two lines - title and heading)
    $team: specify diskname
    $multiple
    $myAlbum:	iPhoto Album name inside XML
	
::
	
    read a file from @piclist
    lookup size of file in big dir
    add size
    check if done with disk
    read another file

output::

    >$pic_home/$team\_$disknum/piclist.txt
	
each record::

    $picname
	$picsize
	$disksize

    $picname could be either .png or .jpg


htmlmake.plx::

    place this .plx file into subdirectory of team disk
    example of input picture name:  w28fa10.jpg

    set:
    $full_top_path
    $top_dir
    $teamdir
    $big_dir
    $small_dir
    $thumb_dir

piclist.txt is in subdirectory of team disk::

    output is 
    BATCHIN	move1st.command
    BATCHOUT	moveback.command
    OUT		start.html


