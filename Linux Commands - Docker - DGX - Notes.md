##### 1.Linux commands for beginners

https://ubuntu.com/tutorials/command-line-for-beginners#1-overview

##### 2.Bash Commands

https://www.educative.io/blog/bash-shell-command-cheat-sheet

##### 3. How to accept connections for ipython from other computers?


https://stackoverflow.com/questions/10538846/how-to-accept-connections-for-ipython-from-other-computers

##### 4. Setting up docker image on GPU

https://github.com/pauloabelha/deeplearning/blob/master/tutorials/Tutorial_Tensorflow_Gpu_Docker.md

##### 5. Jupyter on the DGX

https://github.com/pamelaajohnston/notes/blob/master/juptyer_server_on_DGX.md

##### 6. Some steps involved in running sample project on DGX remotely

Replace 127.0.0.1 with the address of the DGX = csdm-dgx1.rgu.ac.uk

You need to have bash enabled in your container. then you attach to your container, and inside the container, you should be able to install git (if you need to) and clone the necessary repository. You should then be able to type jupyter notebook inside the container to start up the server. It'll give you a new token, but you should be able to work out the address and navigate to it using a browser on myapps.


Step inside that container and type top. It should show you that Juptyer is running.



Type who. If it says root then you're in a container.If it says your student number, you're on the DGX.


If inside DGX, type 'docker attach fpad' to enter inside container.


Inside the container, in whichever directory you like, you should just be able to do 'git clone <link_repo>'

When you run jupyter notebook inside the container, you need to specify the CUDA-VISIBLE_DEVICES.
'CUDA_VISIBLE_DEVICES=7 jupyter notebook --notebook-dir=/tf --ip 0.0.0.0 --no-browser --allow-root'

ctrl+c/cms+c to stop the jupyter notebook. Then install missing libraries

If you use & you'll get your command prompt back, and you should be able to view the notebook on the browser and install things in the terminal.


```python

```
