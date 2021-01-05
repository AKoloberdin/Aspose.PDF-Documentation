---
title: Create Tagged PDF 
linktitle: Create Tagged PDF  
type: docs
weight: 10
lastmod: "2020-12-23"
url: /net/create-tagged-pdf/
description: This article explains how to create structure's elements for Tagged PDF document programmatically using Aspose.PDF for .NET. 
sitemap:
    changefreq: "weekly"
    priority: 0.7
---

Creating a Tagged PDF means adding (or creating) certain elements to the document that will enable the document to be validated in accordance with PDF/UA requirements. These elements are called often Structure Elements.

## Creating Structure Elements

In order to create structure elements in a Tagged PDF Document, Aspose.PDF offers methods to create structure element using [ITaggedContent](https://apireference.aspose.com/pdf/net/aspose.pdf.tagged/itaggedcontent) interface. Following code snippet shows how to create structure elements of Tagged PDF:

```csharp
// For complete examples and data files, please go to https://github.com/aspose-pdf/Aspose.PDF-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_AsposePdf_WorkingDocuments();

// Create Pdf Document
Document document = new Document();

// Get Content for work with TaggedPdf
ITaggedContent taggedContent = document.TaggedContent;

// Set Title and Language for Document
taggedContent.SetTitle("Tagged Pdf Document");
taggedContent.SetLanguage("en-US");

// Create Grouping Elements
PartElement partElement = taggedContent.CreatePartElement();
ArtElement artElement = taggedContent.CreateArtElement();
SectElement sectElement = taggedContent.CreateSectElement();
DivElement divElement = taggedContent.CreateDivElement();
BlockQuoteElement blockQuoteElement = taggedContent.CreateBlockQuoteElement();
CaptionElement captionElement = taggedContent.CreateCaptionElement();
TOCElement tocElement = taggedContent.CreateTOCElement();
TOCIElement tociElement = taggedContent.CreateTOCIElement();
IndexElement indexElement = taggedContent.CreateIndexElement();
NonStructElement nonStructElement = taggedContent.CreateNonStructElement();
PrivateElement privateElement = taggedContent.CreatePrivateElement();

// Create Text Block-Level Structure Elements
ParagraphElement paragraphElement = taggedContent.CreateParagraphElement();
HeaderElement headerElement = taggedContent.CreateHeaderElement();
HeaderElement h1Element = taggedContent.CreateHeaderElement(1);

// Create Text Inline-Level Structure Elements
SpanElement spanElement = taggedContent.CreateSpanElement();
QuoteElement quoteElement = taggedContent.CreateQuoteElement();
NoteElement noteElement = taggedContent.CreateNoteElement();

// Create Illustration Structure Elements
FigureElement figureElement = taggedContent.CreateFigureElement();
FormulaElement formulaElement = taggedContent.CreateFormulaElement();

// Methods are under development
ListElement listElement = taggedContent.CreateListElement();
TableElement tableElement = taggedContent.CreateTableElement();
ReferenceElement referenceElement = taggedContent.CreateReferenceElement();
BibEntryElement bibEntryElement = taggedContent.CreateBibEntryElement();
CodeElement codeElement = taggedContent.CreateCodeElement();
LinkElement linkElement = taggedContent.CreateLinkElement();
AnnotElement annotElement = taggedContent.CreateAnnotElement();
RubyElement rubyElement = taggedContent.CreateRubyElement();
WarichuElement warichuElement = taggedContent.CreateWarichuElement();
FormElement formElement = taggedContent.CreateFormElement();

// Save Tagged Pdf Document
document.Save(dataDir + "StructureElements.pdf");
```

## Creating Structure Elements Tree

In order to create structure elements tree in a Tagged PDF Document, Aspose.PDF offers methods to create a structure element tree using [ITaggedContent](https://apireference.aspose.com/pdf/net/aspose.pdf.tagged/itaggedcontent) Interface. Following code snippet shows how to create structure elements tree of Tagged PDF Document:

```csharp
// For complete examples and data files, please go to https://github.com/aspose-pdf/Aspose.PDF-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_AsposePdf_WorkingDocuments();

// Create Pdf Document
Document document = new Document();

// Get Content for work with TaggedPdf
ITaggedContent taggedContent = document.TaggedContent;

// Set Title and Language for Document
taggedContent.SetTitle("Tagged Pdf Document");
taggedContent.SetLanguage("en-US");

// Get root structure element (Document)
StructureElement rootElement = taggedContent.RootElement;

// Create Logical Structure
SectElement sect1 = taggedContent.CreateSectElement();
rootElement.AppendChild(sect1);

SectElement sect2 = taggedContent.CreateSectElement();
rootElement.AppendChild(sect2);

DivElement div11 = taggedContent.CreateDivElement();
sect1.AppendChild(div11);

DivElement div12 = taggedContent.CreateDivElement();
sect1.AppendChild(div12);

ArtElement art21 = taggedContent.CreateArtElement();
sect2.AppendChild(art21);

ArtElement art22 = taggedContent.CreateArtElement();
sect2.AppendChild(art22);

DivElement div211 = taggedContent.CreateDivElement();
art21.AppendChild(div211);

DivElement div212 = taggedContent.CreateDivElement();
art21.AppendChild(div212);

DivElement div221 = taggedContent.CreateDivElement();
art22.AppendChild(div221);

DivElement div222 = taggedContent.CreateDivElement();
art22.AppendChild(div222);

SectElement sect3 = taggedContent.CreateSectElement();
rootElement.AppendChild(sect3);

DivElement div31 = taggedContent.CreateDivElement();
sect3.AppendChild(div31);

// Save Tagged Pdf Document
document.Save(dataDir + "StructureElementsTree.pdf");
```

## Styling Text Structure

In order to style text structure in a Tagged PDF Document, Aspose.PDF offers [Font](https://apireference.aspose.com/pdf/net/aspose.pdf.logicalstructure/structuretextstate/properties/font), [FontSize](https://apireference.aspose.com/pdf/net/aspose.pdf.logicalstructure/structuretextstate/properties/fontsize), [FontStyle](https://apireference.aspose.com/pdf/net/aspose.pdf.logicalstructure/structuretextstate/properties/fontstyle) and [ForegroundColor](https://apireference.aspose.com/pdf/net/aspose.pdf.logicalstructure/structuretextstate/properties/foregroundcolor) properties of [StructureTextState](https://apireference.aspose.com/pdf/net/aspose.pdf.logicalstructure/structuretextstate) Class. Following code snippet shows how to style text structure in a Tagged PDF Document:

```csharp
// For complete examples and data files, please go to https://github.com/aspose-pdf/Aspose.PDF-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_AsposePdf_WorkingDocuments();

// Create Pdf Document
Document document = new Document();

// Get Content for work with TaggedPdf
ITaggedContent taggedContent = document.TaggedContent;

// Set Title and Language for Document
taggedContent.SetTitle("Tagged Pdf Document");
taggedContent.SetLanguage("en-US");

ParagraphElement p = taggedContent.CreateParagraphElement();
taggedContent.RootElement.AppendChild(p);

// Under Development
p.StructureTextState.FontSize = 18F;
p.StructureTextState.ForegroundColor = Color.Red;
p.StructureTextState.FontStyle = FontStyles.Italic;

p.SetText("Red italic text.");

// Save Tagged Pdf Document
document.Save(dataDir + "StyleTextStructure.pdf");
```

## Illustrating Structure Elements

In order to illustrate structure elements in a Tagged PDF Document, Aspose.PDF offers [IllustrationElement](https://apireference.aspose.com/pdf/net/aspose.pdf.logicalstructure/illustrationelement) class. Following code snippet shows how to illustrate structure elements in a Tagged PDF Document:

```csharp
// For complete examples and data files, please go to https://github.com/aspose-pdf/Aspose.PDF-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_AsposePdf_WorkingDocuments();

// Create Pdf Document
Document document = new Document();

// Get Content for work with TaggedPdf
ITaggedContent taggedContent = document.TaggedContent;

// Set Title and Language for Document
taggedContent.SetTitle("Tagged Pdf Document");
taggedContent.SetLanguage("en-US");

// Under Development
IllustrationElement figure1 = taggedContent.CreateFigureElement();
taggedContent.RootElement.AppendChild(figure1);
figure1.AlternativeText = "Figure One";
figure1.Title = "Image 1";
figure1.SetTag("Fig1");
figure1.SetImage("image.png");

// Save Tagged Pdf Document
document.Save(dataDir + "IllustrationStructureElements.pdf");

```

## Validate Tagged PDF

Aspose.PDF for .NET provides the ability to validate PDF/UA Tagged PDF Document. Validation of PDF/UA standard supports:

- Checks for XObjects
- Checks for Actions
- Checks for Optional Content
- Checks for Embedded Files
- Checks for Acroform Fields(Validate Natural Language and Alternate Name and Digital Signatures)
- Checks for XFA Form Fields
- Checks for Security settings
- Checks for Navigation
- Checks for Annotations

The code snippet below shows how to validate the Tagged PDF Document. Corresponding problems will be displayed in the XML log report.

```csharp
// For complete examples and data files, please go to https://github.com/aspose-pdf/Aspose.PDF-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_AsposePdf_WorkingDocuments();
string inputFileName = dataDir + "StructureElements.pdf";
string outputLogName = dataDir + "ua-20.xml";

using (var document = new Aspose.Pdf.Document(inputFileName))
{
    bool isValid = document.Validate(outputLogName, Aspose.Pdf.PdfFormat.PDF_UA_1);

}
```