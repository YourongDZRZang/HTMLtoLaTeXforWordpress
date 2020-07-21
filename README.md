# LaTeX to HTML for Wordpress (.com) without plugins

This is a very simple program designed by Yourong DZR Zang to help himself upload his notes in LaTeX to his website on Wordpress.com (free). He couldn't afford plugins or domains.

## Installation

Download all files and change the file directory in ```main.java```.

## Usage

Change all parameters in ```main.java``` to fit your need. Paste your code, from ```\begin{document}``` to ```\end{document}``` with all ```\newcommand``` into a text file and use that filename as your file directory. IMPORTANT: you must edit your latex code to make sure it does not contain: 

- ```\begin{alignat}```
- ```\begin{itemize}```
- An equation in more than one line enclosed by ```\[...\]```
- ```\maketitle```, ```\newpage```
- All commands not supported by WordPress LaTeX
- ```\renewcommand``` (currently working on this one)
- Figures

If your code does contain any one of them, please follow these solutions respectively that can work out:
- change ```\begin{alignat}``` to ```\begin{align}``` or ```\begin{equation}```
- Delete ```\begin{itemize}``` and ```\end{itemize}``` and modify your text as HTML plain text (your math formulas will be automatically converted, don't worry about that).
- Delete all newlines and try to put them in one equation (this will always apply, no equation in latex needs newlines).
- Simply delete```\maketitle``` or ```\newpage```, and try to edit your website to achieve the same effect.
- Give up all commands not supported by WordPress LaTeX
- Delete ```\renewcommand``` (you CAN still keep your ```\newcommand``` parts)
- Do it in Wordpress

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

There are some existing bugs that are acknowledged by the creator. He is working on them. Current problems
- ~~Parentheses counting errors when handling ```\newcommand```~~
- No algorithm for dividing lengthy inline formulas
- Cannot handle ```\renewcommand```

## License
[MIT](https://choosealicense.com/licenses/mit/)
