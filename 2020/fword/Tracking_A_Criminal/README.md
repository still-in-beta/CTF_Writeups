The problem states:
> "We have found a flash memory in the crime scene, and it contains 3 images of different villages.
> So, the criminal may be hiding in one of these villages! Can you locate them? Flag Format: FwordCTF{}
> - Separate between the villages names using underscores ( _ ).
> - All the villages names are in lowercase letters.
> - There is no symbols in the villages names.
And has a zip file attached, with three images inside. 

Here it is, if you wish to download: [zipfile]

This challenge is very long and requires LOTS of brute forcing. Google's Reverse Image search and Google Lens
are your best friends. I would suggest using more than one team member to help. Be prepared for lots of trial
and error.

For the first image, I tried using Google images, but no matter how far I scrolled, I just couldn't find anything similar.
I then tried another image searching service called Tineye, but that wasn't so helpful either. At first, I was
stumped, but then I realized that by using the Google Lens feature on my phone, I could take photos from
different angles. I ended up using Google Lens for all of the villages. Though it did take some scrolling
and extra angles, I was eventually able to find this image, which is essentially the original flipped: 
![image 1](https://www.travelsupermarket.com/content/travelsupermarket/en-gb/blog/inspiration/10-of-the-coolest-country-house-hotels/jcr:content/par/image_1910514053.img.fp1518709276679fp.jpg/1518709276679.jpg)
When clicking on the article it's from and scrolling down, you find out that the place originates from
the village of Llanfairpwllgwyngyll. It would also make sense why the Fword team would give a village with
such an unusual name.

Now, let's take a look at the second image. I actually found this one much more quickly than the last (though
it still took lots of time). Again, through Google Lens, I found this photo:
![Alt text](https://images.squarespace-cdn.com/content/v1/54e1f071e4b03a8b46e5a5b4/1426074294224-M7510Y0FH9YHRTZQLI8P/ke17ZwdGBToddI8pDm48kJ4cOYEd37CVJCP8mA0AIfhZw-zPPgdn4jUwVcJE1ZvWQUxwkmyExglNqGp0IvTJZamWLI2zvYWH8K3-s_4yszcp2ryTI0HqTOaaUohrI8PIRvR7vbO2-okrIjBxRCGBroyk8D2xU1Oinph1zpBqgkMKMshLAGzx4R3EDFOm1kBS/MONSANTO_PORTUGAL_A_home_.jpg)
It's not as obvious as the last, but we can definitely see it's the second image from another angle. Same flat
roof, same plants, and same colors. If we read the article, we can tell that it's from Monsanto.

Finally, the last image. This one was the most troubling, since I had to take photos from many different angles to find the
exact windows, stones, etc. I wasn't able to find the exact image, but I did find two similar images. One was from
Marrakesh, and the other from Chefchaouen. I tried both of them, and Chefchaouen was the one that worked with the flag.
After doing some research, I found out that Chefchaouen is known as "the blue city," which would make sense why this
place has blue buildings on the sides.

The exact answer is:
> fwordCTF{llanfairpwllgwyngyll_monsanto_chefchaouen}
