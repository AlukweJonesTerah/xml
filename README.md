# Bookstore XML Project

This project is a simple example of using XML, DTD, XML Schema (XSD), and XSLT to manage and display a bookstore inventory. The project includes an XML document with sample book data, a DTD and XSD to define its structure, and an XSLT stylesheet to transform the XML data into an HTML table for easy viewing on a web page.

## Table of Contents

1. [Project Structure](#project-structure)
2. [Files Overview](#files-overview)
3. [How to Run](#how-to-run)
4. [Sample Output](#sample-output)
5. [Troubleshooting](#troubleshooting)
6. [References](#references)

## Project Structure

```
/bookstore
│
├── bookstore.xml       # XML data file containing book entries
├── bookstore.dtd       # Document Type Definition to define XML structure
├── bookstore.xsd       # XML Schema for stricter structure definition
├── bookstore.xsl       # XSLT file to transform XML data into HTML
└── README.md           # Project documentation
```

## Files Overview

### 1. `bookstore.xml`
The main XML file containing the bookstore data. It lists multiple books with details like title, author, year, price, and category.

### 2. `bookstore.dtd`
A DTD file that defines the structure of the XML data. It specifies the elements and attributes required for each book entry in the bookstore.

### 3. `bookstore.xsd`
An XML Schema file that offers a more rigorous definition of the XML structure, including data types for each element, such as `string`, `integer`, and `decimal`.

### 4. `bookstore.xsl`
An XSLT stylesheet that transforms `bookstore.xml` into an HTML table format for easy viewing. It displays each book’s details in an organized table.

## How to Run

### Prerequisites
Ensure that you have a text editor (e.g., VS Code, Notepad++) and a web browser that supports XSLT (e.g., Firefox) to view the HTML output.

### Steps

1. **Save All Files**  
   Make sure the `bookstore.xml`, `bookstore.dtd`, `bookstore.xsd`, and `bookstore.xsl` files are saved in the same directory.

2. **Open `bookstore.xml` in a Web Browser**  
   Some browsers (e.g., Firefox) can directly apply the XSLT transformation to the XML file and display the result as an HTML page. Open `bookstore.xml` to see the transformed output.

3. **Using an XSLT Processor (Optional)**  
   If you'd like, you can transform the XML file to HTML manually using an XSLT processor like `xsltproc`:
   
   ```bash
   xsltproc bookstore.xsl bookstore.xml > bookstore.html
   ```

   Then, open `bookstore.html` in any browser to view the result.

### Note on Encoding
Ensure all files are saved in UTF-8 encoding without BOM to avoid parsing issues.

## Sample Output

When successfully transformed, the output HTML page will display a table with the following structure:

**Bookstore Inventory**

| Category   | Title         | Author         | Year | Price  |
|------------|---------------|----------------|------|--------|
| children   | Harry Potter  | J. K. Rowling  | 2005 | 29.99  |
| web        | Learning XML  | Erik T. Ray    | 2003 | 39.95  |

## Troubleshooting

### Common Issues

1. **XML Declaration Error**  
   Ensure `<?xml version="1.0" encoding="UTF-8"?>` is the very first line in each XML-based file (no spaces or lines before it).

2. **Encoding Issues**  
   Save files with UTF-8 encoding without BOM. Some editors can add a BOM at the start of UTF-8 files, which can cause XML parsing issues.

3. **Incorrect File References**  
   Verify that the `href` in `<?xml-stylesheet type="text/xsl" href="bookstore.xsl"?>` matches the exact filename and path of your XSL file.

## References

- [XSLT Tutorial - W3Schools](https://www.w3schools.com/xml/xsl_intro.asp)
- [Linking XSLT to XML Document - Microsoft Docs](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/ms757904(v=vs.85))
