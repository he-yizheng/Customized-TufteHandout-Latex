Hello! 
Wellcome to this customizable Tufte-Handout template! 

## Acknowledgement
This template is heavily influenced by McGill folks, including student, professor and alumni, due to the fact that this style is kind of popular at McGill. Especially, this template is my personal replication and customization of Anna Brandenberger's notes template. 
>https://github.com/abrandenberger/course-notes

## Quick Start
Basically all the basic function are commented in the .tex file. 
And all the common usage of the package can be found in the main text, including theorem/definition block, margin-note, inserting figures and so on.

### Recommendation for Using Latex
1. Go set your own snippets! I put parts of my snippets json file in the repo too. (I used vscode latex workshop)
2. VS code is still really good for writing latex, you can try.

## Latex Class Related Issues
Be aware that some warning like "Latex: Marginpar Missing in Page ~" is fine, as long as you can see the desired pdf file after compiling.

It's still recommended to check out the documents in the original Tufte-Latex repository, since the Latex class we're using here is exactly the same as that one. Any instruction with class related issues should be directed to those documents.

## Further Customization
There are several parts in this template can be further customized. 
#### Section title style
You can select font and colors for title itself and its numeration, and decide wether you want to display title or numeration for a certain section type in latex, as you wish.

There are a bunch of section types in latex, including Chapter, Section, Subsection, Paragraph.
You can even create your own section type, e.g. Subparagraph.
##### Idea of my section title style
I used a fcolorbox behind the section title numeration to make it look better. 
##### Understanding the code:
You can through the code in for title style configuration into Chatgpt or any LLM, asking them to explain it for you. 
But I will briefly explain what it's important here, adding comments in forms of "_(comments)"

```
\makeatletter
\makeatletter
  \renewcommand{\section}{\@startsection{section} % set the section title
    {3_(set the depth)}{-1.01em_(shift the entire thing horizontally)}
    {-3ex \@plus -1ex \@minus -.2ex} 
    % vertical space above, 
    % \@plus set the additional range that latex can decide to use when needed, 
    % vice versa
    {1.5ex \@plus .2ex} % vertial space below, similarly
    {\hspace*{-5.5em}\fcolorbox{blue}{blue}{\parbox[c][1.0ex][b]{4em}{\phantom{space}}}
    % the repeative things to display in every this type of titles
    % the trick is, we used a colorbox to create a color background for the 
    % numeration
    \normalfont\Large\itshape\color{blue}}}
    % the font and color for title itself
\makeatother
```

#### Theorem Blocks
You can also customized the theorem blocks to meet your preference. I used thmtools package here, but you can also use amsthm, shouldn'd cause any problem.

## Debugging

### Overall
Latex is a bit old and it's normal to have some strange problem/warning. Debugging by trying is useful.

**However, if you are using VS Code to write, sometime restart VS code is the only thing you need to do.** The compiler can stop working even when your codes are completely legit.
#### The titles
The position of the title might go wrong in some cases. In some cases, you can fix it by changing the horizontal shift parameter, and the \\hspace*{} to move things around. In other cases, if the first title looks strange, change the length of the abstract a bit.


## Contributing

Patches and pull requests are most welcome via the issue tracker!  

## License

Copyright 2007–2015 by Kevin Godby, Bil Kleb, and Bill Wood.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.




