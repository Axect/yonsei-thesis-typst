# Yonsei University Thesis Template for Typst

This repository contains a Typst template for creating Yonsei University theses and dissertations, complying with the official formatting guidelines.

## Features

- Complete template for both doctoral dissertations and master's theses
- Pre-configured page layouts and margins according to Yonsei University requirements
- Automatically generated:
  - Cover page
  - Title page
  - Signature page
  - Table of contents
  - List of figures
  - List of tables
  - Bibliography support
  - Korean abstract page

## Requirements

- [Typst](https://typst.app/) (latest version recommended)
- Times New Roman font

## Usage

1. Clone this repository or download the `thesis.typ` file.
2. Place the file in your project directory.
3. Create your main Typst file (e.g., `main.typ`) and use the template like this:

```typst
#import "thesis.typ": thesis

#show: doc => thesis(
  title: "Your Thesis Title",
  title_kr: "논문 제목 (한국어)",
  author: "Your Name",
  degree: "Philosophy",
  department: "Your Department",
  university: "Yonsei University",
  date: "2025",
  month: "June",
  year: "2025",
  supervisor: "Name of Supervisor",
  committee: ("Committee Member 1", "Committee Member 2", "Committee Member 3", "Committee Member 4"),
  is_doctoral: true, // true for doctoral dissertation, false for master's thesis
  doc,
)

= Introduction

Your content here...
```

## Template Parameters

| Parameter | Description |
|-----------|-------------|
| `title` | Title of the thesis (in English) |
| `title_kr` | Title of the thesis (in Korean) |
| `author` | Author's name |
| `degree` | Degree type (e.g., "Philosophy", "Science") |
| `department` | Department name |
| `university` | University name (default: "Yonsei University") |
| `date` | Full date |
| `month` | Month of submission |
| `year` | Year of submission |
| `supervisor` | Name of the thesis supervisor |
| `committee` | Array of committee member names |
| `is_doctoral` | Boolean value (true for doctoral dissertation, false for master's thesis) |

## Formatting Notes

- The template uses Times New Roman at 11pt with 1.15 line spacing
- First-line indentation of 2em for paragraphs
- Justified text alignment
- Proper heading styles according to Yonsei University guidelines
- Automatic page numbering (Roman numerals for preliminaries, Arabic numerals for main content)
- Footnotes with 9pt font size

## Customization

You can customize the template by modifying the `thesis.typ` file. The file is well-commented to help you understand the different sections and formatting options.

## Korean Text Support

The template includes special handling for Korean text with appropriate line spacing:

```typst
#show "한글": set par(leading: 0.75em) // 1.5 line spacing for Korean text
```

## License

[MIT License](LICENSE)

## Acknowledgments

- Created by Axect
- Based on the official Yonsei University thesis guidelines
