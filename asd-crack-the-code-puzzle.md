# Solving ASD's "Can You Crack the Code?" Puzzle

> **Brief:** The Australian Signals Directorate posted what's apparently called a Mastermind puzzle on the 12th of October 2026. What follows is a writeup of how I arrived at the solution. A full description and illustration of the problem can be found in the link below.

**Original post:** [Australian Signals Directorate on LinkedIn](https://www.linkedin.com/posts/a-little-game-night-nostalgia-for-your-feed-share-7515253668980391936-IDaw/)

In the write-up, the rows of the board are called Line 1 (top row), Line 2, and so on down.

> ⚠️ **Spoiler warning:** the answer and full reasoning are in the collapsed section below. Try the puzzle first.

<details>
<summary><strong>Solution (spoiler)</strong></summary>

## Answer

**Yellow, Black, Green, Blue**

## Write-up

Now that I am at my desk, I have the mental and workable space to write the complete solution.

### Hard rules

There are some hard rules I can state:

1. This is a 4 colour solution.
2. There are 6 possible colours.
3. From 1 and 2, we can now say that there are 2 invalid colours.

### Lines 3 and 4

I will denote the top line as Line 1, and each following line to be a line of the next number. Taking a look at lines 3 and 4, according to the pins there are 2 valid colours in each line. There are many combinations of valid colours that satisfy the pins:

- Red White
- Red Blue
- White Blue
- Red Green Yellow
- White Green Yellow
- Blue Green Yellow

Taking a look at the first 3 pairs, what happens when checking against lines 3 and 4, 3 colours become invalid. E.g. If we assume Red and White to be valid colours, against line 3 Blue and Green can't be valid colours, and looking at line 4, Yellow is also not a valid colour. In total that is 3 invalid colours, which contradicts the 3rd hard rule. This contradiction occurs in all 3 pair possibilities.

So I am left with the possible triplets of Red Green Yellow, White Green Yellow, and Blue Green Yellow. Also note that in each of these triplets, there are 2 invalid colours. E.g. For Red Green Yellow, Blue and White are invalid. So rather than triplets, we can confirm 3 of the 4 colours - Black, Green and Yellow - with the 4th being red, white or blue.

### Testing the 4th colour

If we test red as the 4th colour, this contradicts the 2nd line that says there are only 3 valid colours. If we test white as the 4th colour, this contradicts the first line, as there are 2 pins, but three "valid but not valid" colours. And just to check for blue, the 1st line is missing 2 of my assumed valid colours (i.e. yellow and blue), and line 2 is missing an assumed valid colour, which is blue.

### Placing black (slot 2)

Looking at line 1, there is a white pin and a black pin. White and red are invalid, which leaves me with two possibilities.

1. The black pin is in the right place and the green is not.
2. The green is in the right place and the black is not.

However line 3 already shows that green cannot be on the 4th slot, therefore black has to be in the 2nd hole.

### Placing blue (slot 4)

In the 4th position, green and yellow are confirmed to not belong on the 4th slot based on line 3 and 4, black is already set on slot 2, which leaves me with blue.

### Placing yellow (slot 1) and green (slot 3)

Now if I take a look at line 2, there is one correct coloured pin in the correct position. I know black belongs in the 2nd slot (and is not there at line 2), I know blue belongs in the 4th slot (and isn't present in line 2), and I know red is an invalid colour, thus yellow has to be what satisfies the black pin, and is therefore the first.

Finally, by hard rule 1, I am left with green in the remaining slot.

</details>
