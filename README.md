# A collection of all my templates

1. [Curriculum Vitae](./cv_template/vs_template.tex)
2. [Beamer template for talks](./beamer/beamer.tex)
3. [Homework template]()

##  Curriculum Vitae

```latex
%%| EDUCATION |%%
\newcommand{\education}[6]{
	\item\textbf{#1} \hfill \textbf{#2} \\ \emph{#3} \hfill #4 --- #5

	\begin{addmargin}[2em]{1em}
	#6
	\end{addmargin}
	\vspace{3mm}
}

%-----------------------------------------------------------------%

%%| WORK EXPERIENCE |%%
\newcommand{\work}[7]{
    \IfEqCase{#1}{
    	{title}{\item\textbf{#2} \hfill \textbf{#3} 

    	\emph{#4} \hfill #5 --- #6
		\begin{addmargin}[0.5em]{1em}
			\internalList{#7}
		\end{addmargin}
		}
    	{notitle}{\item[]\emph{#4} \hfill #5 --- #6
		\begin{addmargin}[0.5em]{1em}
			\internalList{#7}
		\end{addmargin}
		}
    }
}
```

##  Beamer template for talks

```latex
%%| TALKS |%%
\newcommand{\talk}[5][0.5]{
	\item \begin{minipage}{#1\textwidth}
		\emph{#2}
	\end{minipage}\begin{minipage}{\textwidth - #1\textwidth - \columnsep}
		\raggedleft{\textbf{\hrefTalk{#4}{#3}}}\\ \raggedleft{#5}
	\end{minipage}
}
```

##  Homework template

```latex
% Labeling question from the book
\NewDocumentCommand\book{O{}mg}{
    \vspace{-4.1em}
    \begin{adjustwidth}{}{1em}
        \begin{flushright}
            \footnotesize(\textit{From }\IfNoValueTF{#3}{
                    \textit{the book}
                }{#1#3#1}\textit{, \textbf{question #2}})    
        \end{flushright}
    \end{adjustwidth}   
    \par\vspace{2.5em}\noindent
}
% 'and' for inbetween two equations in align environment or $$
\newcommand\andeqs[1][and]{\qquad\text{#1}\qquad}

% space for tensor indices
\newcommand\none{\phantom{\mu}}

\newcommand\questiontext[1]{
    \begin{adjustwidth}{0.8in}{0.8in}
        \begin{tcolorbox}[empty, borderline south={1pt}{0pt}{black!30!white}]
            \small#1
        \end{tcolorbox}
    \end{adjustwidth}
}
```

