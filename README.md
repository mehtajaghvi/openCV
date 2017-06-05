# openCV
Installed using:
  http://docs.opencv.org/2.4/doc/tutorials/introduction/linux_install/linux_install.html
  -----cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local ..
  When I used a local directory instead of /usr/local, all the paths for the header files were in local directory and not in /usr/local.
  This was an issue as I was unable to compile programs without proper paths
  
Running the first program:
 -----g++ -o test_2 f2.cpp `pkg-config opencv --cflags --libs` 
source:  https://stackoverflow.com/questions/7816607/opencv-2-3-compiling-issue-undefined-refence-ubuntu-11-10
Had to use the above line of code with pkg-config, got bunch of errrs otherwise, running this also created an issue, had to use the code below to rectify that
 
------ sudo ldconfig -v 
(source: https://stackoverflow.com/questions/480764/linux-error-while-loading-shared-libraries-cannot-open-shared-object-file-no-s)
 
