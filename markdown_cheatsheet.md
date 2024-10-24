Modified from: https://www.markdownguide.org/basic-syntax/

Other references: https://www.markdownguide.org/hacks/

Colour on Github:  
https://tex.stackexchange.com/questions/308087/command-for-both-bold-and-colored-text  
https://github.com/orgs/community/discussions/31570  

Using tables on Github  
https://stackoverflow.com/questions/24319505/how-can-one-display-images-side-by-side-in-a-github-readme-md

Multiple paragraphs within single bullet  
https://stackoverflow.com/questions/55780011/in-markdown-how-does-one-keep-multiple-paragraphs-within-a-single-bullet-point

________________________

$$\textcolor{blue}{\textbf{All hail colored text!}}$$

$$\LaTeX$$

# Heading level 1	
## Heading level 2	
### Heading level 3	
#### Heading level 4	
##### Heading level 5	
###### Heading level 6

Heading level 1
===============
Heading level 2
---------------

<br>

I just love **bold text**.
I just love __bold text__.
Love**is**bold

<br>

Italicized text is the *cat's meow*.
Italicized text is the _cat's meow_.
A*cat*meow

<br>

> Blockquote  
> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

<br>

> Nested blockquotes
> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

<br>

1. First item
2. Second item
3. Third item
    1. Indented item
    2. Indented item
4. Fourth item

<br>

- First item
- Second item
- Third item
- Fourth item

<br>

You can use html too!!! :) :) Yay! (break text!) (Pressing enter will nto introduce new lines in MD. You must use
````
<br>
````
<br>
<br>
<br>
<br>
<br>

Images: the many ways to import them: successes and failures :(  Compare source file and rendered webpage. It's funny that the image might work well in the MD file but fails to appear in the website, and vice versa!


<p> 1. Open the file containing the Linux mascot. </p>

<p> 2. Marvel at its beauty. </p>

<br>

HTML:  
<img src="https://odysseyprogramme.github.io/images/tux.jpg" width="100" >
<br>
<img src="/content/images/tux.jpg" width="100"  alt="tux fails to show up">
 
<br>
 
 Markdown:  
![Tux the mascot](https://odysseyprogramme.github.io/images/tux.jpg)

![tux fails to show up](/content/images/tux.jpg)

<br>
XHTML:  
<img src="{static}/images/tux.jpg" width="100" />

<p> 3. Close your eyes. </p>

<br>


Works on github, yet becomes code block in website. Even the list fails to render... There must be a way...
1. Open the file containing the Linux mascot.
2. Marvel at its beauty.

    ![Tux, the Linux mascot](https://odysseyprogramme.github.io/images/tux.jpg)

3. Close the file.
