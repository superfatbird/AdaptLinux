During installation of MATLAB on ubuntu. I used a reference as this [link](https://linuxconfig.org/how-to-install-matlab-on-ubuntu-18-04-bionic-beaver-linux).

Everything goes well until starting the matlab app after installation. 
I have encountered with a error -9. <pre><code>License checkout failed. License Manager Error -9.</code></pre>

During the installation or the startup process of the matlab. It will ask you to enter a END USER NAME, under that name, the software could be activated and used. 
You should enter the name of the account you login into linux. Otherwise, you will encounter the error -9. (I had entered a different user name which bring the issue).

Here is not the end of the story. When you install the matlab. You need to use the 'sudo ./install' command. That will cause all the files and folders for the matlab belonging to the user "root". 
In such condition, when you activate the matlab or start it. the account you login do not have the permission to change the files which belongs to the root. So you just change the ownership of these files and folders to the account you login as. 
Then the matlab will start normally. **Do not try to assign the matlab license to the user ”root“**
