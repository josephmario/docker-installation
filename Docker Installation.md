<h1 id="docker-setup">Docker Setup</h1>
<p>For Reference: <a href="https://docs.docker.com/engine/install/ubuntu/">https://docs.docker.com/engine/install/ubuntu/</a></p>
<ul>
<li>Setup docker on your Ubuntu PC
<ul>
<li>
<p>Create file type “nano  <a href="http://docker-setup.sh">docker-setup.sh</a>”</p>
</li>
<li>
<p>copy and paste it in docker-setup.sh`#!/bin/bash</p>
<pre><code> echo "******************************"
 echo "*    Set up the repository   *"
 echo "******************************"

 echo "Update the apt package index and install packages to allow apt to use a repository over HTTPS:"
 sudo apt-get update
 sudo apt-get install ca-certificates curl gnupg
 echo "Add Docker’s official GPG key:"
 sudo install -m 0755 -d /etc/apt/keyrings
 curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
 sudo chmod a+r /etc/apt/keyrings/docker.gpg
 echo "Use the following command to set up the repository:"

 echo \
    "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/li$
    "$(. /etc/os-release &amp;&amp; echo "$VERSION_CODENAME")" stable" | \
    sudo tee /etc/apt/sources.list.d/docker.list &gt; /dev/null
 echo "Update the apt package index:"
 sudo apt-get update
 echo "Install Docker Engine, containerd, and Docker Compose."
 sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
 echo "Verify that the Docker Engine installation is successful by running the hello-world image."
 sudo docker run hello-world`
</code></pre>
</li>
<li>
<p>run chmod 777 -R  (filename)</p>
<ul>
<li>example “chmod 777 -R &lt;<a href="http://docker-setup.sh">docker-setup.sh</a>&gt;”  for readable, writable, and executable by all user</li>
</ul>
</li>
<li>
<p>Check the text if it’s green meaning can run the shell script</p>
</li>
<li>
<p>run shell scripts “./docker-setup.sh”</p>
</li>
</ul>
</li>
</ul>

