In order to complete the Python implementation of this project on the GCP VM, I followed the
tutorial "How To Serve Flask Applications with uWSGI and Nginx on Ubuntu 18.04" found on 
DigitalOcean.com, along with another guide from the same site called "How to Install Nginx 
on Ubuntu 18.04". These tutorials were very helpful while I was figuring out how to use Flask
and the different options and implementations availible for Flask. I ended up using the 
recommended setup of a virtual enviornment inside of the VM to serve my site. Fortunately, 
Flask and Nginx allow the actual Python code to be very simple. The Python code allowed me
to provide a directory-like structure to the site, and to execute methods like "files" in 
the directory. This allowed me to make the main method (i.e. root directory) simply return 
a random integer using the 'random.randrange()' function.

After getting the site up and running to be accessible by localhost, Nginx will attempt to
serve it to the web with the IP of the VM; however, I had to establish a static IP and setup some firewall rules in GCP in order for Nginx to actually serve it properly. Without
fixing GCP firewall rules, the server will not allow access to it's ports and will only serve one static page.

The site is availible through any browser or via cURL at: http://35.193.105.234:5000
