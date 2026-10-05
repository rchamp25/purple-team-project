10/5/2026:

Part 1:
    Steps 1-6:

        Started the projec and made first commits including the docker compose file and the the intial placholder readme. This project is going to be done entirely by hand with the aim of learning and understanding introductor aspects of cybersecurity.

        Defintions:
            Docker Image: This is the lightweight version of a executable software package. It is read-only, Docker finds the app to be downloaded and used from its registry (Docker Hub). It can do this using the compose file which specifies a name to look for and maps a port on the PC to a port inside the container. A container is the running instance of an image.

            I ran into a error where I had a typo in the word "services" im my yaml file. While initially confused because I am new to the syntax of .yml (same as .yaml) I realized through the error in the command line that my file had a typo causing the error. 

            What the 127.0.0.1 Port Prefix is: This is the specification that is also known as localhost (computer communicates with itself rather than internet). The traffic . There are two main reasons for this. One is so that it doesnt open up these vulernable test applications to other users on the same network because even though they are running in docker containers, the security isn't perfect. 
        
            Need to clean up understanding of inbound and outbound connections and what limits each. 

            Inbound is who can reach the apps running at (127.0.01) and Outbound is what my "lab" can reach (host only network coming soon). We will setup VirtualBox to manage outbound traffic as Docker allows outbound traffic by default. 


    Step 7: 

        Downloaded VirtualBox which will be the VM of choice for this project.

        Note: the difference between a container and a virtual machine is that a container still shares the same kernel to run applications as the host computer as where virtual machines are meant to emulate their own "physical computer" which is isolated from the host computer's OS.
        
        VM's tend to take up much more memory and take longer to boot and offer hardware-level security. 

        Containers run on a container engine (like Docker here) and use much less storage and boot faster, though they are process-level security.

        Note: Hardware-level security uses physical hardware and hypervisors to completely isolate entire operating systems. Process-level security relies on software boundaries within a single operating system to isolate individual applications. 

        The reason we are using hardware-level security for this lab is the same as why most purple-team professionals use it as well, that is, because running live malware in a container can breakout and allow the malware to infect the host machine, and then move to the network as well. For safety, we use VMs.
        
    Step 8:



    

