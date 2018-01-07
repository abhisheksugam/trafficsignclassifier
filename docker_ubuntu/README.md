Testing

1. Launch AWS m4.2xlarge Instance (ami-01f05461) with appropriate Security Group (I used https://gist.github.com/iamatypeofwalrus/5183133 for reference). 
 
2. Once Instance is launched, SSH into it. I use Putty. Refer to http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/putty.html for details.

3. After SSHing
	* $ `sudo apt-get install git`
	* $ `git clone https://github.com/yourHandle/whereYouSavedYourProjectFiles.git`
	* Download the folder `https://github.com/sahiljuneja/Udacity-Self-Driving-Car-ND/tree/master/Term-1/P2-Traffic-Sign-Classifier/docker_ubuntu`

4. Build Docker Container
	* $ `cd docker_ubuntu` (wherever cloned/downloaded)
	* $ `chmod +x *.sh`
	* $ `sudo ./install.sh`
	* $ `sudo ./build.sh`

5. Download project data
	* Edit get_data.sh to save data files (train.p and test.p) to your project folder. Edit `/home/ubuntu/Udacity-Self-Driving-Car-ND/Term-1/P2-Traffic-Sign-Classifier/`
	* $ `sudo ./get_data.sh`

6. Edit run.sh and Run the Container
	* In run.sh modify the line `-v /home/ubuntu/Udacity-Self-Driving-Car-ND:/home/Udacity-Self-Driving-Car-ND \ ` to correspond to your own cloned project repo directory
	* $ `sudo ./run.sh` (You might have to press "Enter" again after running the command)

7. Run notebook
	* `jupyter notebook --ip='*' --port=8888 --no-browser`

8. Access notebook in your local machine browser
	* `public_ip:8888` where public_ip is the ip of your aws instance

Don't forget to terminate your instance once you are done.

