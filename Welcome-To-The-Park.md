![[-1 Welcometothepark-header.png]]


Once I downloaded the file, I extracted the contents in that directory.
![[-2 Extracted.png]]

I begin to examine the files within the extracted content. During my examination, I found a file named "interesting.command" containing the text "ls -a is your friend".
![[-3 ls2.png]]
![[-3 ls.png]]

I continued my examination whilst using the ls -a command. I then came across a directory named ".hidden"
![[-4 hidden.png]]

Within the .hidden directory, I found a file named "welcometothepark". I cat the file and find a base64 string.
![[-5 welcomefile.png]]

I copied the base64 sting and take it into Cyberchef to decode it.
![[-6 base64Decoded.png]]

Once decoded, I see that it is xml content and can also see what it is trying to accomplish. I went ahead and put the pieces together from this output. I could see that I needed to curl "curl https://gist.github.com/stuartjash/a7d187c44f4327739b752d037be45f01". 
![[-7 curl.png]]


After using the curl command with the pieced together URL, I found another subdomain to with the extension "/JohnHammond.jpg".
![[-8 suburl.png]]

When I navigate to that link, it is a picture from the iconic 90's movie "Jurassic Park" (previously hinted in challenge description).
![[-9 JurrasicJPG.png]]

I downloaded the .jpg file and saved it to my attack machine. Opening the file did not yield any results. I then cat the .jpg file and obtained the "flag" at the bottom of the output!
![[-10 Flag.png]]


