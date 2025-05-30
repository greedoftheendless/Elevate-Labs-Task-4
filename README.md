🛡️ Task 4: Setup and Use a Firewall on Linux
🎯 Objective

Configure and test basic firewall rules to allow or block network traffic using UFW (Uncomplicated Firewall) on Linux.
🧰 Tools Used

    UFW – Frontend for iptables, used to simplify firewall configuration.

    Telnet – Used to test blocked ports.

    Systemctl – To manage the firewall service.

🛠️ Steps Performed
1. Install and Enable UFW

sudo pacman -S ufw
sudo systemctl enable --now ufw

2. Check Current Firewall Rules

sudo ufw status numbered

3. Add Rule to Block Port 23 (Telnet)

sudo ufw deny 23/tcp

4. Test Block Rule

Try connecting to port 23 (should fail):

telnet localhost 23

5. Allow SSH on Port 22

sudo ufw allow 22/tcp

6. Remove the Block Rule to Restore State

sudo ufw delete deny 23/tcp

Or using rule number:

sudo ufw status numbered
sudo ufw delete [rule_number]

💠Lesson Learned
  How to monitor rules of firewall
  How to use firewall rules to block a connection and allow connection
  Uses of firewalls in linunx
