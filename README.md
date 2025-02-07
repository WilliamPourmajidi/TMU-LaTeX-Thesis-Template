# TMU-LaTeX-Thesis-Template

This repository provides a LaTeX template for MSc and PhD theses at Toronto Metropolitan University’s Department of Computer Science. It contains all the essential files needed to set up, compile, and format a thesis according to the department’s guidelines.

## File Overview

- **CLS-Creation-Instruction**  
  Contains step-by-step instructions on how to generate or modify the thesis class file from the `.dtx` and `.ins` sources.

- **natbib.sty**  
  A commonly used LaTeX package for managing citations and bibliographies. It supports numeric and author–year citation styles.

- **ryesample.bib**  
  A sample BibTeX database demonstrating reference entries. Replace or modify it to include your own references.

- **ryethesis.cls**  
  The core document class file that enforces TMU’s thesis formatting rules (margins, spacing, headings, etc.).  
  - **Using on Overleaf**: Simply upload this file to the root folder of your Overleaf project. It is ready to be used without reconstruction for most cases.

- **ryethesis.dtx**  
  A documented LaTeX source containing the definitions for `ryethesis.cls`. It’s useful for those who want to customize the class at a deeper level.

- **ryethesis.ins**  
  The installation script that extracts and compiles `ryethesis.cls` from `ryethesis.dtx`. Run this to rebuild the class if you make changes to the `.dtx` file.

- **thesisTemplate.tex**  
  The main LaTeX file illustrating how to use the class and packages. It’s the recommended entry point for writing your thesis.

## Usage

1. **Obtain the Files**  
   - Clone or download this repository.

2. **Installation and Dependencies**  
   - Make sure you have a full LaTeX distribution (e.g., [TeX Live](https://www.tug.org/texlive/), [MikTeX](https://miktex.org/)).
   - Ensure standard packages (like `natbib`) are available; they are typically part of most LaTeX distributions.

3. **Class File Creation (Optional)**  
   - By default, `ryethesis.cls` can be used as-is.
   - If you wish to modify or rebuild the `.cls`, follow the instructions in **CLS-Creation-Instruction** and run:
     ```
     latex ryethesis.ins
     ```
     to generate or update `ryethesis.cls` from `ryethesis.dtx`.

4. **Overleaf Usage**  
   - Upload `ryethesis.cls`, `natbib.sty`, `ryesample.bib`, and `thesisTemplate.tex` to the main (root) folder of your Overleaf project.
   - Update `thesisTemplate.tex` with your personal details and compile.

5. **Modifying the Template**  
   - Edit `thesisTemplate.tex` to change information such as the thesis title, author name, department, and date.
   - Replace `ryesample.bib` with your own set of references, adjusting your citation commands accordingly.
   - Add or remove chapters and sections within the provided structure as needed.

6. **Compiling Your Thesis (Local)**  
   - From the command line:
     ```
     pdflatex thesisTemplate.tex
     bibtex thesisTemplate
     pdflatex thesisTemplate.tex
     pdflatex thesisTemplate.tex
     ```
   - Alternatively, use `latexmk`:
     ```
     latexmk -pdf thesisTemplate.tex
     ```

## Tips

- If you notice missing references or a blank table of contents, additional LaTeX passes are usually needed.
- Adjust citation styles in `thesisTemplate.tex` if you prefer numeric or author–year citations.
- Rebuild the class file after any changes to `ryethesis.dtx` by running `ryethesis.ins`.

## Contributing

Feel free to open issues or submit pull requests for improvements or bug fixes. Feedback is welcome.

## License

