# \# Colonoscopy Polyp Segmentation Report

# 

# \## Introduction

# This is a LaTeX template for the report "Colonoscopy Polyp Segmentation Using Deep Learning" by Group 42, University of Science and Technology of Hanoi.

# 

# \## File Structure

# ```

# colonoscopy\_fixed.tex          # Main LaTeX file

# README.md                       # This guide

# ```

# 

# \## Required Images

# To compile successfully, prepare the following image files and place them in the same directory as the .tex file:

# 

# \- \*\*usth.png\*\* - USTH Logo

# \- \*\*637266958\_2151000069002670\_8489864047731370573\_n.png\*\* - U-net architecture diagram

# \- \*\*output.png\*\* - Training curves chart

# \- \*\*1.png\*\* - Qualitative segmentation results

# \- \*\*preb2.png\*\* - Visualization example case 1

# \- \*\*preb3.png\*\* - Visualization example case 2

# 

# \## Usage Guide

# 

# \### Option 1: Overleaf (Recommended)

# 1\. Visit \[overleaf.com](https://www.overleaf.com)

# 2\. Create new project → "Upload Project"

# 3\. Copy all content from `colonoscopy\_fixed.tex`

# 4\. Upload all image files

# 5\. Compile and download PDF

# 

# \### Option 2: Local (Your Computer)

# 1\. Install LaTeX (TexLive, MiKTeX, or MacTeX)

# 2\. Copy `colonoscopy\_fixed.tex` and all images to a folder

# 3\. Compile:

# &nbsp;  ```bash

# &nbsp;  pdflatex colonoscopy\_fixed.tex

# &nbsp;  ```

# 4\. PDF will be generated automatically

# 

# \## Report Structure

# 

# \### Page 1 (Title Page)

# \- USTH Logo

# \- Title: Colonoscopy Polyp Segmentation Using Deep Learning

# \- Group Information:

# &nbsp; - Bui Duc Thang -- 23BI14400

# &nbsp; - Le Quoc Anh -- 23BI14022

# &nbsp; - Nguyen Hoang Lan -- 23BI14392

# \- Department \& University

# \- Date

# 

# \### Pages 2+

# \- Table of Contents

# \- Abstract

# \- Main Sections:

# &nbsp; - Introduction

# &nbsp; - Related Work

# &nbsp; - Dataset

# &nbsp; - Data Preprocessing

# &nbsp; - Data Augmentation

# &nbsp; - Neural Network Architecture

# &nbsp; - Loss Functions

# &nbsp; - Training Strategy

# &nbsp; - Evaluation Metrics

# &nbsp; - Experimental Results

# &nbsp; - Discussion

# &nbsp; - Limitations

# &nbsp; - Future Work

# &nbsp; - Conclusion

# &nbsp; - References

# 

# \## Features Fixed

# 

# ✅ \*\*Logo \& Title on Page 1\*\* - All author information on single page  

# ✅ \*\*No Image Misalignment\*\* - Uses `\[H]` placement and 0.7-0.9 linewidth  

# ✅ \*\*Professional Layout\*\* - Header/Footer, page numbers, proper spacing  

# ✅ \*\*Multi-class Segmentation\*\* - Supports 3 classes: Background, Neoplastic, Non-neoplastic  

# ✅ \*\*Hybrid Loss Function\*\* - Dice Loss + Focal Loss  

# ✅ \*\*Complete Metrics\*\* - IoU, mIoU, Dice, Recall  

# 

# \## Customization

# 

# \### Change Group/Authors

# Find and replace:

# ```latex

# {\\large \\textbf{Group 42}}

# 

# Bui Duc Thang -- 23BI14400 \\\\

# Le Quoc Anh -- 23BI14022 \\\\

# Nguyen Hoang Lan -- 23BI14392

# ```

# 

# \### Change Date

# ```latex

# \\today  % Auto-generates today's date

# % or

# 26 February 2026  % Manual entry

# ```

# 

# \### Adjust Image Size

# ```latex

# \\includegraphics\[width=0.9\\linewidth]{image.png}  % Reduce 0.9 to 0.7, 0.8, etc.

# ```

# 

# \### Add New Section

# ```latex

# \\section{Section Name}

# Section content here

# ```

# 

# \## Troubleshooting

# 

# \### Error: Image not found

# \- Ensure all image files are in the same directory as the .tex file

# \- Check file names match exactly (case-sensitive)

# \- Verify file extensions (.png)

# 

# \### Images appear cut off

# \- Reduce width value: change `0.9\\linewidth` to `0.8\\linewidth` or lower

# \- Use `\[H]` placement specifier for better positioning

# 

# \### Compilation errors

# \- Ensure all required packages are installed

# \- Check for missing closing braces `}`

# \- Verify all `\\begin{}` have matching `\\end{}`

# 

# \### Header/Footer not showing

# \- Confirm `\\pagestyle{fancy}` is set before `\\begin{document}`

# \- Make sure page style isn't overridden by `\\thispagestyle{empty}`

# 

# \## Packages Used

# 

# \- `graphicx` - Image insertion

# \- `amsmath, amssymb` - Math equations

# \- `hyperref` - Hyperlinks

# \- `booktabs` - Professional tables

# \- `geometry` - Page margins

# \- `setspace` - Line spacing

# \- `caption, subcaption` - Figure captions

# \- `fancyhdr` - Headers and footers

# \- `float` - Float placement control `\[H]`

# 

# \## Document Properties

# 

# \- \*\*Font Size\*\*: 11pt

# \- \*\*Paper Size\*\*: A4

# \- \*\*Line Spacing\*\*: 1.3x

# \- \*\*Margins\*\*: 2.5cm on all sides

# \- \*\*Language\*\*: English

# 

# \## Tips \& Best Practices

# 

# 1\. \*\*Always backup\*\* your .tex file before major edits

# 2\. \*\*Use consistent\*\* section naming and formatting

# 3\. \*\*Check spelling\*\* before final compilation

# 4\. \*\*Compress images\*\* to reduce PDF file size

# 5\. \*\*Test compilation\*\* after each major change

# 6\. \*\*Use meaningful\*\* figure labels for cross-references

# 

# \## Contact \& Support

# 

# For issues with the LaTeX template, ensure:

# \- All image files are present

# \- File names match exactly

# \- You're using a compatible LaTeX compiler

# \- All required packages are installed

# 

# \## License

# 

# This template is provided as-is for educational purposes.

