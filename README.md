# ai-python-project-1--counting-loans-with-dockerized-shell-script-solved
**TO GET THIS SOLUTION VISIT:** [AI-python Project 1- Counting Loans with Dockerized Shell Script Solved](https://www.ankitcodinghub.com/product/python-p1-6-of-grade-counting-loans-with-dockerized-shell-script-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;119418&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;AI-python Project 1- Counting Loans with Dockerized Shell Script Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Overview

Learning objectives: * deploy a virtual machine in the cloud * follow a complicated series of steps to install Docker * write a shell script to automate several bash commands * bundle a shell script up as a Docker image/container

Before starting, please review the general project directions.

Corrections/Clarifications

Sep 7: Link to walkthrough + GCP clarification

Sep 8: Fix directions to get correct Docker compose version Sep 8: Clarify output format for line count

Part 1: Virtual Machine Setup

We’ll use Google’s Cloud (GCP) for our virtual machines. They’ve generously given each 544 student $100 in credits, which should last the whole semester if you stick to the budget plan.

You can obtain the credits here: https://canvas.wisc.edu/courses/374194/pages/google-credits.

Setup a virtual machine that you’ll use for the first few projects (we’ll eventually delete it and create a more powerful one for some of the later projects).

You should have some experience in creating VMs in a prior course (320 or 400), so these directions will be brief, and you can decide things like what geographic region to create it in (I picked Iowa since it’s nearby), but here are some highlights:

you can launch and see VMs from here: https://console.cloud.google.com/compute/instances Be sure to choose e2-small for machine type.

you’ll need to setup an SSH key so you can connect from your laptop: https://console.cloud.google.com/compute/metadata?tab=sshkeys (the browser-based SSH client won’t work for what we need to do in this class)

When you’re done, check that you have the correct Operating System and CPU with cat /etc/os-release and lscpu. Save the outputs to hand in too:

cat /etc/os-release &gt; os.txt lscpu &gt; cpu.txt Part 2: Docker Install

Carefully follow the directions here to install Docker 24.0.5 and Compose 2.20.2 on your virtual machine: https://docs.docker.com/engine/install/ubuntu/

Notes: * there are several different approaches described under “Installation methods”. Use the directions under “Install using the apt repository”.

Make sure you don’t keep going after you reach “Install from a package” * the first step under “Install Docker Engine” has two options: “Latest” or

“Specific version”. Choose “Specific version” * here is the command to get the required versions: sudo apt-get install dockerce=5:24.0.5-1~ubuntu.22.04~jammy docker-ce-cli=5:24.0.5-1~ubuntu.22.04~jammy containerd.io docker-buildxplugin docker-compose-plugin=2.20.2-1~ubuntu.22.04~jammy

To avoid needing to run every Docker command with root, there are a few more steps you can do here:

https://docs.docker.com/engine/install/linux-postinstall/#manage-docker-as-a-non-root-user (don’t go beyond the “Manage Docker as a non-root user” section).

Create some more files so we can check your Docker install:

docker version &gt; docker.txt docker compose version &gt; compose.txt

Part 3: Shell Script

Try running some shell commands to download the zip, extract the contents, and print how many lines contain the text “Multifamily” (case sensitive) — it’s OK if you print other additional output too.

Now, combine these commands in a count.sh file; the script should have a shebang line so that the following runs with bash:

sh ./count.sh

Make sure your .sh file is executable!

Part 4: Docker Image

Create a Dockerfile that starts from a base image of your choosing and includes your count.sh file. The Dockerfile should do any installs needed for your script to run.

You should be able to create an image and container like this:

docker build . -t p1 docker run p1

It’s OK if there’s extra output besides the actual count.

Submission

At a minimum, your submission repo (watch for an announcement on how to set this up) should contain the following: os.txt, cpu.txt, docker.txt, compose.txt, count.sh, Dockerfile.

If you worked with a partner, there should only be one submission repo, with at least one commit by each partner.

Tester

Copy autograde.py and ../tester.py to your working directory then run python3 autograde.py to test your work and environment setup. The test result will be written to a test.json file in your directory. This will probably be your grade, but autograders are imperfect, so we reserve the right to deduct further points. Some cases are when students achieve the correct output by hardcoding, or not using an approach we specifically requested.
