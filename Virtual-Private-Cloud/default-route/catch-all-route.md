## Definition
the default route or catch-all-route represents all possible IP addresses. Think of this route as giving access from anywhere or to the internet without restriction 

IPv4 default route: 0.0.0.0/0

IPv6 default route: ::/0 

When we specify the default route address in the route table, for IGW, we are allowing internet access
When we specify the default route address in the Security Group's Inbound Rules, we are allowing traffic from the Interent to access our public resources 