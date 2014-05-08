---
layout: page
title: Resources 
tagline: useful information 
---

#### [GNU Scientific Library](http://www.gnu.org/software/gsl/)
- A free numerical library for C and C++ programmers


---

#### [Python](http://www.python.org) 

- A beginner [tutorial](https://wakari.io/gallery) 
- Notebook viewer [link](http://nbviewer.ipython.org)
- Python [data type](http://www.tutorialspoint.com/python/python_variable_types.htm)  
- Pandas [data type](http://pandas.pydata.org/pandas-docs/stable/dsintro.html)
- [Statsmodels module](http://statsmodels.sourceforge.net)

  ...[more](foo) 

---

#### [R](http://www.r-project.org)

- [RStudio](https://www.rstudio.com) (A very good IDE for R)

  > To generate graphs with a better resolution, add the following parameters   

  >	```{r fig1, fig.width=9, fig.height=3, unit="in", dpi=200}
  >        plot(foo)
  >     ```

- Style [guide](assets/google_style.pdf) recommended by google

- Lattice (trellis) [graphs](http://www.statmethods.net/advgraphs/trellis.html) 

  > ![.](assets/lattice_graphs.png) 

---

#### Stata
- Stata [graphs](http://www.stata.com/support/faqs/graphics/gph/stata-graphs/)

---

#### LaTeX
- Math [notations](http://en.wikibooks.org/wiki/LaTeX/Mathematics) and [symbols](http://web.ift.uib.no/Teori/KURS/WRK/TeX/symALL.html)
- [Hightlighting and underlining](http://www.ctan.org/pkg/soul)

  >	\usepackage{soul, color}	% use \ul{}, \hl{}

- [Todonotes](http://www.tex.ac.uk/ctan/macros/latex/contrib/todonotes/todonotes.pdf)

  >	\usepackage[textwidth=1.5in, textsize=tiny]{todonotes}		
  >					% use \todo{text}, \missingfigure, \listoftodos
  >	\usepackage[left=.3in, right=1.7in,top=1in, bottom=1in]{geometry}
  >			       		% make right margin wider

- Reduce space around title/sections

  >	 \usepackage[compact]{titlesec}
  >	 %\titlespacing{\section}{0pt}{4pt}{0pt}
  >	 %\titlespacing{\subsection}{0pt}{3pt}{0pt}
  > 	 %\titlespacing{\subsubsection}{0pt}{3pt}{0pt}

- Citation 'name-author-year' 

  >	\usepackage[super,sort&compress,comma]{natbib}
  >	\bibpunct{(}{)}{;}{a}{}{,}

- Fancy heading

  >	\usepackage{fancyheadings}
  > 	\lhead{Draft}
  > 	\rhead{\textsf{Liu, Tao}}
  > 	\cfoot{\textsf{Page} \sf\thepage}
  > 	\pagestyle{fancy}

- Change section numbering

  >	 \renewcommand{\thesection}{\Alph{section}.}
  >	 \renewcommand{\thesubsection}{\thesection\arabic{subsection}.}
  >	 \renewcommand{\thesubsubsection}{\thesubsection\alph{subsubsection}}
  >	 \renewcommand{\textfraction}{.2}

- Write in other languages 

  > 	\usepackage[utf8]{inputenc}	% prerequisite
  >	\usepackage[T1]{fontenc}	% prerequisite
  >	\usepackage[chinese]{babel}

- Math 

  >	\usepackage{amsmath,amssymb,amsthm,mathrsfs,amsfonts}

- Line space 

  >	\usepackage{setspace}
  >	%\doublespacing
  >	%\onehalfspacing

- Misc. 

  >	\usepackage[latin9]{inputenc} 
  				      % allows for inputting accented chars directly from KB
  >	\usepackage{mathpazo}	      % Palatino font
  > 	\usepackage{breakurl}	      % url line break 
  > 	\usepackage{booktabs}	      % table makeups
  >	\usepackage{graphicx}	      % figures 
  >	\renewcommand{\bibsection}{\centering \textbf{REFERENCES}}

- Wrapping [text around figures](http://en.wikibooks.org/wiki/LaTeX/Floats,_Figures_and_Captions) and [tables](http://tex.stackexchange.com/questions/49300/wrap-text-around-a-tabular)

  >	   \begin{wrapfigure}{r}{0.5\textwidth}
  >	     \vspace{-20pt}
  >	     \begin{center}
  >	       \includegraphics[width=0.48\textwidth]{gull}
  >	     \end{center}
  >	     \vspace{-20pt}
  >	     \caption{A gull}
  >	     \vspace{-10pt}
  >	   \end{wrapfigure}


  >	   \begin{wraptable}{r}{5.5cm}
  >	   \caption{A wrapped table going nicely inside the text.}\label{wrap-tab:1}	
  >	   \begin{tabular}{ccc}\\\toprule  
  >	   Header-1 & Header-1 & Header-1 \\\midrule
  >	   2 &3 & 5\\  \midrule
  >	   2 &3 & 5\\  \midrule
  >	   2 &3 & 5\\  \bottomrule
  >	   \end{tabular}
  >	   \end{wraptable} 


---

#### Vim 
- LaTex [shortcuts](http://vim-latex.sourceforge.net/documentation/latex-suite/latex-macros.html)
- Most productive [shortcuts](http://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim/1218429)
- Close a buffer:  `:BW` 
- Initiate the (insert) VISUAL model:  `ctrl+o, v`.
- Open at the last edited file position. 
  
  >	'0; no need to open the file. 

  Or, create ~/.vim/view, and place this in your .vimrc :

  >	au BufWinLeave * mkview
  >	au BufWinEnter * silent loadview	

- [Sync with Skim](http://sourceforge.net/apps/mediawiki/skim-app/index.php?title=TeX_and_PDF_Synchronization)
  
  Add a mapping in .vimrc or .vim/ftplugin/tex.vim     
  
  >     map ,r :w<CR>:silent !/Applications/Skim.app/Contents/SharedSupport/displayline <C-r>=line('.')<CR> %<.pdf %<CR>

  Supply the command line option `-synctex=1`, or include \synctex=1 
  
  In Skim, choose Preference -> sync. (Need to move mvim in the installation package to /usr/local/bin.) 

  In Skim: use shift+command+click. In vim, use ,r.

---

#### Linux

- CL setup wifi 

  >      ifconfig -a	(optional, show all devices)
  >      sudo ifconfig wlan0 up 	   	
  >      sudo iwlist wlan0 scanning | less	(optional, show available wifi)
  >      sudo iwconfig wlan0 essid dd-wrt	(connect to dd-wrt) 
  >      sudo dhclient wlan  (obtain IP) 

- Terminal 
  
  >	alias xterm = "xterm -fa 'Dejavu San Mono' -fs 10"


--- 

#### GitHub
- Create project page [(gh-pages)](https://help.github.com/articles/creating-project-pages-manually)

---

#### [Bullet Journal System](http://www.bulletjournal.com)

--- 
*Last updated Apirl 2014*
