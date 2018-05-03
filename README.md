# Purpose  

I always focus on the networks software devlopment whatever userspace or kernel and client or server :)  
In this repository, I try to describe the details of kernel networks module as many as possible. 

Now there are two flow charts already now.  
1. kernel_skb_path: Describe the skb's flow path.  
2. netfilter_path: Describe the netfilter path which skb would go through.  
3. skb_member: Describe the skb's members.  
4. skb_gro: Describe the skb GRO flow.  


# kernel_skb_path
It is the skb path of Linux kernel. I would like enlarge the flow always.  
The flow is constructed based on latest netdev kernel whose git link is git://git.kernel.org/pub/scm/linux/kernel/git/davem/net.git


Because I want to focus on the skb path from the lay 2 to socket layer, so the driver is not that I care about. I just selected the intel's e1000 driver to explain the NAPI. 



There are two reasons as following
1. Intel's driver is more clear than other vendor's.   
2. The e1000 driver is most simplest and is enough to show the NAPI  

link: https://github.com/gfreewind/kernel_net_chart/blob/master/kernel_skb_path.jpg


# netfilter_path  
It is the netfilter path which skb would go through.  
The netfilter is often used as the firewall in network devices and servers. The path chart could help you learn about the netfilter.  
link: https://github.com/gfreewind/kernel_net_chart/blob/master/netfilter_path.jpg  

# ipvlan  
It is the complete flow of ipvlan including control plane and data plane  
link: https://github.com/gfreewind/kernel_net_chart/blob/master/ipvlan.jpg

# macvlan  
It is the complete flow of macvlan including control plane and data plane  
link: https://github.com/gfreewind/kernel_net_chart/blob/master/macvlan.jpg


# skb_member

It is used to describe the sk_buff's members, and show which functions would access them. 
It could help you learn about the struct sk_buff.  
link: https://github.com/gfreewind/kernel_net_chart/blob/master/skb_members.jpg


# skb_gro  
Describe the GRO flow of skb. It would refer too many details of specific proto.  
So there is no investigation deep for the protos.  
link: https://github.com/gfreewind/kernel_net_chart/blob/master/skb_gro.jpg


# udp_protocol  
Describe the flow of UDP recept and deliver flow based on the struct udp_protocol and udp_prot.  
link: https://github.com/gfreewind/kernel_net_chart/blob/master/udp_protocol.jpg  
