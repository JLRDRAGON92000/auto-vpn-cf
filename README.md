EC2 OpenVPN AS (CloudFormation automatic version)
-------------------------------------------------

This CloudFormation template creates an EC2 instance, and a full stack of
resources to go along with it (VPC, internet gateway, subnet, routing, security
groups, elastic IP), and installs and configures OpenVPN Access Server on it.
This instance is ready to use as a VPN tunnel to the Internet (additional
configuration may be required to use it as a VPN endpoint into your AWS cloud,
such as configuring routing between its VPC and your other VPCs).

Once the template is created, go to Instances to view the server's IP address,
and browse to `https://[IP address]/` (certificate warnings are normal). Log in
with the username `openvpn` and the password you set in the template parameters.
You will be prompted to download OpenVPN Connect. This download will come
pre-configured to connect to your instance with its elastic IP address.

This template also serves as a starting point for creating a CloudFormation
template for a single EC2 instance, its own VPC, and all supporting resources.

