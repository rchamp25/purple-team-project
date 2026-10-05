10/5/2026:
Segment 1:
    Step 1:
    Started the projec and made first commits including the docker compose file and the the intial placholder readme. This project is going to be done entirely by hand with the aim of learning and understanding introductor aspects of cybersecutiry.
    Defintions:
        Docker Image: This is the lightweight version of a executable software package. It is read-only, Docker finds the app to be downloaded and used from its registry (Docker Hub). It can do this using the compose file which specifies a name to look for and maps a port on the PC to a port inside the container. A container is the running instance of an image.

        I ran into a error where I had a typo in the word "services" im my yaml file. While initially confused because I am new to the syntax of .yml (same as .yaml) I realized through the error in the command line that my file had a typo causing the error. 

        What the 127.0.0.1 Port Prefix is: This is the specification that is also known as localhost (computer communicates with itself rather than internet). The traffic . There are two main reasons for this. One is so that it doesnt open up these vulernable test applications to other users on the same network because even though they are running in docker containers, the security isn't perfect. 
        
        Need to clean up understanding of inbound and outbound connections and what limits each. 

        Inbound is who can reach the apps running at (127.0.01) and Outbound is what my "lab" can reach (host only network coming soon). We will setup VirtualBox to manage outbound traffic as Docker allows outbound traffic by default. 


    Step 2: 
    
    

