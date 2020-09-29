The problem states:
> The druid in your party is a fan of the animal friendship spell. 
> To get the flag, track them down in this packet capture, then report
> who they befriended here: nc web.red.csaw.io 5017
and has a data file attached.

We can open this data file in wireshark. Just by looking at the first few columns, we can see that a link is attached to one of the requests.

When clicked, it will download a jpeg to your computer.

If we netcat to the link in the problem, it shows us the text:
> *** Animal Friendship ***
> To get the flag, answer this question:
> What sort of creature is Domo's friend?

You can answer squirrel or chipmunk. Either way, you'll get the flag:
> flag{m4k1n9_f0r3n51c5_53c0nd_n47ur3}
