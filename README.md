LaTeX style files for INT-ACT deliverables.
============================================
S.Luz@ed.ac.uk.

Basic usage:
------------

The basic structure of a deliverable formatted according with these
styles should be (minimally):

```latex
    \documentclass[10pt]{report}
    \usepackage{int-act}  
    
    \begin{document}
    
    %% a Changelog. Each call to \istChange adds an entry to the
    %% changelog. After LaTeX is run, it will generate a table on page 2
    %% containing all changes. N.B.: I could not find a way to generate
    %% this table directly, so the whiledo{} loop in istprog.sty writes
    %% the changelog table to a temp file (more or less the way tables of
    %% content are generated), so you have to run LaTeX twice to update
    %% this table (as you would to update the TOC).
    \istChange{dd/mm/yyyy}{v1.o}{Name (Partner short name)}{Draft report template}
    \istChange{...}{}{...}{}
    \istChange{}{}{}{}

    %% Deliverable information (if omitted, defaults to sensible values)
    \ProjectAcronym{INT-ACT}
    \ProjectFullTitle{Cultural heritge etc}
    \ProjectRefNo{nnnn}
    \delivNumber{Dn.n}
    \delivName{[Title as appears in the DOW]}
    \delivShortTile{Short Title}
    %% Lead partner
    \delivResponsible{[Responsible partner]} 
    \delivVersion{vn.n}
    \ActualDate{dd/mm/yyyy}
    \delivDissLevel{CO}
    \delivType{[Report, Prototype, Other]}
    \delivWP{WPx.x} % Workpackage x; not used at the moment
    \delivAuthor{Names of co-authors  (partners short names)}
    \delivFPAuthor{Names of co-authors  (partners short names)}
    \delivStatus{Draft}
    \delivKeywords{[List of free keywords relevant to the deliverable]}
    \delivTask{Tn.n}
    
    \delivStatus{[Draft, v1.0, v2.0, Final version]}
    \delivExecSummary{This is a summary of the deliverable; a paragraph or
    so to go on the cover page} 
    
    \makecover
    % page 3: table of contents
    \newpage
    \fancypagestyle{plain}{}
    
    \settableofcontents
    \tableofcontents
    
    \vfill
    \section*{List of abbreviations}
    
    \begin{tabular}[h]{ll}
     EC	        &	European Commission \\
     DoA	&	Description of Action\\
    \end{tabular}
    
    
    \newpage
    \section{Your first section}
    
    \subsection{A subsection of your first section}
    
    etc
    
    \bibliography{your-bib-file}
    \bibliographystyle{apacite} %% recommended 
    \{document}
```

Further details
---------------

See `template.tex/template.pdf` in this directory.

If you have any thoughts on how to improve this style, feel free to
implement them and share your results. The same goes for bug fixes.

Just clone the project at

https://git@git.overleaf.com/67339e0d2b6b763477ec7b00

or open it on the Overleaf editor:

https://www.overleaf.com/project/67339e0d2b6b763477ec7b00

and 'Have fun!'

