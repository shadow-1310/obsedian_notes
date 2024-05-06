- ultisnippets for LaTex
	- https://www.youtube.com/watch?v=PAjzNEUXTxI, watch at 25:00
#### problems with zathura highlighting
- https://www.reddit.com/r/vim/comments/cvu78p/vim_opens_zathura_with_unwanted_green_highlight/

## put logo in top right corner
- [stackoverflow post](https://tex.stackexchange.com/questions/228055/put-logo-on-top-right-corner-in-beamer)
```tex
\usepackage{eso-pic}
\beamertemplatenavigationsymbolsempty
\setbeamertemplate{footline}[frame number]

\newcommand\AtPagemyUpperLeft[1]{\AtPageLowerLeft{%
\put(\LenToUnit{0.9\paperwidth},\LenToUnit{0.9\paperheight}){#1}}}
\AddToShipoutPictureFG{
  \AtPagemyUpperLeft{{\includegraphics[width=.5cm,keepaspectratio]{logo.png}}}
}%
```
