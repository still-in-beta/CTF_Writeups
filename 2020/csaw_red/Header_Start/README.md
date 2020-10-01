The problem states:
> This challenge should give you a good picture of a warm up challenge...if only we could view it

And has a file attached. Unfortunately, as the problem suggests, this file is a plain data file, meaning we cannot view it. The problem implies that the file is meant to be viewed, so looking into its hex data would not a bad idea.

![image1](https://github.com/still-in-beta/CTF_Writeups/blob/master/2020/csaw_red/Header_Start/Screen%20Shot%202020-09-30%20at%203.44.46%20PM.png)

In the ASCII on the right, we can see that part of the signature is IHDR and sRGB. A basic Google search will tell you that those are part of a PNG header, which tells us that this is supposed to be a PNG file. It's just that the rest of the header is missing.

If we do another search for the specific PNG header in hex, we get:
> 89 50 4E 47 0D 0A 1A 0A

We can see that the first four bytes of the file are the same as the last four parts of the header, so this means we have to <b> insert </b> (not replace) the first four bytes of the header.

After we have done this, we now rename the file to a png filetype, and then view it.

![image 2](https://github.com/still-in-beta/CTF_Writeups/blob/master/2020/csaw_red/Header_Start/myImageFile.png)

The flag is:
> flag{itZ_ju$7_A_w@Rm_Up}
