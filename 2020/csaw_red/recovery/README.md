The problem states:
> Alice forgot her throwaway email address, but she has a packet capture of her traffic. Can you help her recover it? To get the flag, answer a question about this traffic on the server here: nc web.red.csaw.io 5018
and has a data file attached.

We can open the data file in wireshark. Unfortunately, there are far too many requests listed, so we cannot just simply scroll through them. Thankfully, wireshark allows us to filter out content to get what we desire in a file.

Since we are looking for anything related to alice, it wouldn't be a bad idea to search for Alice's name. We can type:
> frame contains "alice"
into the search bar. When we do that, two results show up.

One of them has Alice's email address. If we netcat to the link specified, it asks us:
> *** Recovery *** To get the flag, answer this question: what is Alice's email address?
If we input the email address, we will get the flag:
> flag{W1r3sh4rk,TCPfl0w,gr3p,57r1n95--7h3y'r3_4ll_f0r3n51c5_700l5}
