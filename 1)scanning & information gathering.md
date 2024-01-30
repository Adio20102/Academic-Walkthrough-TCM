# Scanning & Information Gathering

Information gathering and scanning is the first and essential step to solve a challenge and get the weakness information about target to hijack the system and get the control. First we will do a quick nmap scan to figure out all open ports and running services and it’s version information.

<img alt="" class="bg hc hd c" width="1000" height="450" loading="lazy" role="presentation" src="https://i.ibb.co/gMV3q98/Academy-i.png"></img>

<ul><li data-selectable-paragraph=""><strong >We got three ports open on the victim machine.</li>
<li data-selectable-paragraph=""><strong >On port number 21, A ftp server is running and anonymous login as allowed to the server.</li>
<li data-selectable-paragraph=""><strong >Now we login to the machine using FTP port.</li></ul>

<img alt="" class="bg hc hd c" width="1000" height="450" loading="lazy" role="presentation" src="https://i.ibb.co/RyYgC6g/Academy-ii.png"></img>

Give `username` as `anonymous` , put `password` `blank` and hit enter.</br >
We got a file called `note.txt` on the server.<br>
`note.txt` file is revealing database query and student information as student ID and password hash.<br>

# Directory Busting
<ul>
<li data-selectable-paragraph=""><strong >We move further on to port 80.</li>
<li data-selectable-paragraph=""><strong >A default page is running on the port 80 server.</li>
<li data-selectable-paragraph=""><strong >We will use a directory busting tool called ffuf.</li>
</ul>


