- How to leverage cache using Dockerfiles
    Use already created layers or base images and install minimum required to execute the requried task
    Use Copy or Add as a last command where possible


- What are multi-stage builds
    Creating images from already derived images to cut the size of the final build
    This is acheived by spliting docker file onti multiple sections using FROM, and use of earlier build output into another for e.g. compile code using first FROM and used the artifact in final that only requried runtimes to cut the unnecessary files requrie to buit etc.

- Explain Containers vs Image
    Images are blueprint and Containers are its instance
    Containers actually executed to perform task
    Images to be built using optimized instructions
    Images are layer based which are immutable
    Container used that layes and add its RW layer on top of it
    Images can be created from container executing with changes, that will create a new image

- Explain RUN vs CMD vs Entrypoint
    RUN executes command(s) in a new layer and creates a new image. E.g., it is often used for installing software packages. It is a build time command
    CMD sets default command and/or parameters, which can be overwritten from command line when docker container runs. It is a run time command
    ENTRYPOINT configures a container that will run as an executable. It is a rumtime command