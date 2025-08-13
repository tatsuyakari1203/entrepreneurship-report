# HCMUT Report Template

A LaTeX template for academic reports at Ho Chi Minh City University of Technology (HCMUT), Vietnam National University Ho Chi Minh City.

## Repository Information

- **Repository**: https://github.com/hoang-himself/hcmut-report
- **Issues**: https://github.com/hoang-himself/hcmut-report/issues
- **Latest Commit**: 350906b86be7adae1c953217029cbe12ad4f6ac5 - refactor: update `listings` styles

## Project Structure

```
entrepreneurship-report/
├── LICENSE.txt              # License file
├── README.md               # This documentation
├── report.tex              # Main LaTeX document
├── hcmut-report.cls        # Custom document class
├── codespace.sty           # Custom package for code formatting
├── chapters/               # Chapter files directory
│   └── example/           # Example chapters
│       ├── better-enum.tex
│       ├── better-tables.tex
│       ├── codespace.tex
│       └── figwidth.tex
├── code/                   # Source code directory
│   └── example.py
├── graphics/               # Images and graphics
│   └── hcmut.png          # HCMUT logo
└── refs/                   # Bibliography files
    └── example.bib
```

## Features

### Document Class (`hcmut-report.cls`)

The custom document class provides:
- **University branding**: Automatic HCMUT header and logo integration
- **Flexible layout**: Support for both one-sided and two-sided printing
- **Customizable metadata**: Course name, report type, title, advisor, and student information
- **Professional formatting**: Proper margins, spacing, and typography
- **Multi-language support**: English and Vietnamese babel support

### Code Formatting (`codespace.sty`)

The custom package offers:
- **Syntax highlighting**: Support for multiple programming languages
- **Code blocks**: Beautiful framed code environments
- **Listings integration**: Enhanced `listings` package with custom styling
- **Minted support**: Advanced syntax highlighting with Pygments
- **Customizable colors**: Predefined color scheme for code elements

### Example Chapters

The template includes comprehensive examples:
- **Better tables**: Professional table formatting with `booktabs`
- **Better enumerations**: Enhanced list formatting with `enumitem`
- **Code spaces**: Code formatting and syntax highlighting examples
- **Figure width**: Responsive figure sizing and positioning

## Quick Start

### Prerequisites

- LaTeX distribution (TeX Live, MiKTeX, or MacTeX)
- Required packages: `vntex`, `babel`, `booktabs`, `listings`, `minted`, etc.
- Python with Pygments (for `minted` package)

### Basic Usage

1. **Clone or download** this template
2. **Edit the main document** (`report.tex`):
   ```latex
   \coursename{Your Course Name}
   \reporttype{Your Report Type}
   \title{Your Report Title}
   \advisor{& Your Advisor Name &}
   \stuname{%
     & Student Name 1 & Student ID 1 \\
     & Student Name 2 & Student ID 2 \\
   }
   ```

3. **Add your content** in the main document or create separate chapter files
4. **Compile** using your preferred LaTeX compiler:
   ```bash
   pdflatex report.tex
   bibtex report
   pdflatex report.tex
   pdflatex report.tex
   ```

### Document Configuration

#### Metadata Commands

- `\coursename{text}`: Set the course name
- `\reporttype{text}`: Set the report type (e.g., "Assignment Report", "Final Project")
- `\title{text}`: Set the report title
- `\advisor{text}`: Set advisor information
- `\stuname{text}`: Set student information (supports multiple students)
- `\deptname{text}`: Set department name (default: Faculty of Computer Science and Engineering)
- `\reportplace{text}`: Set report location (default: Ho Chi Minh City)
- `\reporttime{text}`: Set report date (default: current month and year)

#### Document Options

- `twoside`: Enable two-sided printing with alternating headers
- `draft`: Enable draft mode for faster compilation
- `final`: Enable final mode (default)

## Advanced Usage

### Project Organization

#### Splitting Content into Multiple Files

For larger reports, organize content into separate files:

```latex
% In report.tex
\input{chapters/introduction.tex}        % Use \input for smaller files
\include{chapters/methodology.tex}       % Use \include for chapters
\include{chapters/results.tex}
\include{chapters/conclusion.tex}
```

**Difference between `\input` and `\include`**:
- `\input{file}`: Simply inserts the file content
- `\include{file}`: Equivalent to `\clearpage \input{file} \clearpage`

#### File Organization Best Practices

- **Chapters**: Store in `chapters/` directory
- **Images**: Store in `graphics/` directory
- **Code**: Store in `code/` directory
- **References**: Store in `refs/` directory

### Label Conventions

Use consistent label prefixes for better organization:

- `chap:` for chapters
- `sec:` for sections
- `subsec:` for subsections
- `eq:` for equations
- `fig:` for figures
- `tab:` for tables
- `enum:` for enumerators and items
- `fn:` for footnotes
- `lst:` for listings
- `alg:` for algorithms
- `app:` for appendices

**Important**: Always place `\label{}` **after** `\caption{}`, not before or inside it.

### Code Integration

#### Using the `listings` Package

```latex
\begin{lstlisting}[language=Python, caption=Example Python code, label=lst:example]
def hello_world():
    print("Hello, World!")
\end{lstlisting}
```

#### Using the `minted` Package

```latex
\begin{minted}{python}
def hello_world():
    print("Hello, World!")
\end{minted}
```

#### Inline Code

```latex
\mintinline{python}{print("Hello")}  % For minted
\lstinline{print("Hello")}           % For listings
```

### Tables and Figures

#### Professional Tables

Use `booktabs` for professional-looking tables:

```latex
\begin{table}[H]
  \centering
  \caption{Your table caption}
  \label{tab:example}
  \begin{tabular}{lcc}
    \toprule
    Item & Value 1 & Value 2 \\
    \midrule
    A    & 1       & 2       \\
    B    & 3       & 4       \\
    \bottomrule
  \end{tabular}
\end{table}
```

#### Responsive Figures

```latex
\begin{figure}[H]
  \centering
  \includegraphics[width=0.8\linewidth]{graphics/your-image.png}
  \caption{Your figure caption}
  \label{fig:example}
\end{figure}
```

### Bibliography Management

1. **Add references** to `refs/example.bib`:
   ```bibtex
   @article{example2023,
     title={Example Article},
     author={Author Name},
     journal={Journal Name},
     year={2023}
   }
   ```

2. **Cite in text** using `\cite{example2023}` or `\citep{example2023}`

3. **Include bibliography**:
   ```latex
   \bibliographystyle{plain}
   \bibliography{refs/example.bib}
   ```

## Customization

### Modifying the Document Class

Edit `hcmut-report.cls` to customize:
- Page layout and margins
- Header and footer design
- Font settings
- Color schemes
- University branding elements

### Extending Code Formatting

Edit `codespace.sty` to:
- Add new programming languages
- Customize syntax highlighting colors
- Create new code environments
- Modify frame styles

### Language Support

To switch to Vietnamese:

```latex
% In hcmut-report.cls, change:
\RequirePackage[english]{babel}
% to:
\RequirePackage[english,vietnamese]{babel}
```

## Compilation

### Standard Compilation

```bash
pdflatex report.tex
bibtex report
pdflatex report.tex
pdflatex report.tex
```

### With Minted (requires Python and Pygments)

```bash
pdflatex -shell-escape report.tex
bibtex report
pdflatex -shell-escape report.tex
pdflatex -shell-escape report.tex
```

### Using Latexmk (recommended)

```bash
latexmk -pdf -shell-escape report.tex
```

## Troubleshooting

### Common Issues

1. **Missing packages**: Install required LaTeX packages through your distribution's package manager
2. **Minted errors**: Ensure Python and Pygments are installed, and use `-shell-escape` flag
3. **Font issues**: Make sure `vntex` package is properly installed for Vietnamese support
4. **Bibliography not showing**: Run `bibtex` after the first `pdflatex` compilation

### Performance Tips

- Use `draft` mode during development for faster compilation
- Comment out `\listoffigures`, `\listoftables`, and `\lstlistoflistings` if not needed
- Use `\includeonly{chapter-name}` to compile only specific chapters during development

## Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

For bug reports and feature requests, please use the [Issues](https://github.com/hoang-himself/hcmut-report/issues) page.

## License

See `LICENSE.txt` for license information.

## Acknowledgments

- Ho Chi Minh City University of Technology (HCMUT)
- Vietnam National University Ho Chi Minh City
- LaTeX community for excellent packages and documentation