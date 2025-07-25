# .txtnm

A minimal file format used to store animations for my console based game. <br>
Which in the future I will hopefully add upon with a custom library to use it.

.txtnm comes from from **.txt** + **nm** = **anim** , therefore it really just means "**text animation**".

## Main concept

Replacing text characters, some of which can be several bytes in size, with smaller amounts of data, using maps. <br>
For several thousand .txt files, this can make a relatively big difference.

Example :
A file contain the following text

"abbaabbaabbababa" <br>
<sub><sup> (16 bytes / 1 byte per character) </sub></sup>

2 distinct characters, which means only a single bit is required to represent each character.

If we now map:

a $\to$ 0 <br>

b $\to$ 1 <br>

The previous string of characters becomes:

"011001100110101" <br>
<sub><sup> (2 bytes / 1 bit per character) </sub></sup>

Each unique text file has its own local palette of characters / map, drawing its content from a global palette / list of characters. <br>
Or you can see both the local and global palettes as lists, with the local one being part of a map.

I won't go into much more detail, as this pretty much sums up the important part.


[![Han shot first!]([https://i.sstatic.net/Vp2cE.png)](https://youtu.be/vt5fpE0bzSY](https://youtu.be/0SVJsadM6FI))
