## Setup

Pull a container from Docker and run it. Website should be available at http://localhost:80.

## Common issues

### Unknown database
Connection failed: Unknown database 'bWAPP'

If you see this go to http://localhost/install.php and press install. 
Now you can continue to http://localhost/login.php.

### DNS lookup does not work

For OS command injection the server performs a dns lookup with a popular program that may not be installed. Go to the container (exec tab) and run apt-get update and then apt install dnsutils.
