---
title: Extract Images from PDF in Node.js
linktitle: Extract Images from PDF
type: docs
weight: 20
url: /nodejs-cpp/extract-images-from-the-pdf-file/
description: How to extract a part of the image from PDF using Aspose.PDF for Node.js toolkit.
lastmod: "2023-11-05"
sitemap:
    changefreq: "weekly"
    priority: 0.7
---

## Extract images from PDF files in the Node.js environment

In case you want to extract images from PDF document, you can use [AsposePdfExtractImage](https://reference.aspose.com/pdf/nodejs-cpp/convert/asposepdfextractimage/) function. 
Please check following code snippet in order to extract images from PDF file using Node.js via C++.

**CommonJS:**

1. Require the AsposePDFforNode.сjs module.
1. Specify the name for the PDF file from which the image will be extracted.
1. Initialize the Aspose Pdf() module. Receive the object if successful.
1. Call the function [AsposePdfExtractImage](https://reference.aspose.com/pdf/nodejs-cpp/convert/asposepdfextractimage/).
1. Extract images from the PDF file. Thus, if 'json.errorCode' is 0, the result of the operation is saved in "ResultPdfExtractImage{0:D2}.jpg". Where {0:D2} represents the page number with a two-digit format. The images are saved with a resolution of 150 DPI. If the json.errorCode parameter is not 0 and, accordingly, an error appears in your file, the error information will be contained in 'json.errorText'.

```cjs

  const AsposePdf = require('.//AsposePDFforNode.cjs');
  const pdf_file = 'Aspose.pdf';
  AsposePdf().then(AsposePdfModule => {
      /*Extract image from a PDF-file with template "ResultPdfExtractImage{0:D2}.jpg" ({0}, {0:D2}, {0:D3}, ... format page number), resolution 150 DPI and save*/
      const json = AsposePdfModule.AsposePdfExtractImage(pdf_file, "ResultPdfExtractImage{0:D2}.jpg", 150);
      console.log("AsposePdfExtractImage => %O", json.errorCode == 0 ? json.filesNameResult : json.errorText);
  });
```

**ECMAScript/ES6:**

1. Import the AsposePDFforNode.mjs module.
1. Specify the name for the PDF file from which the image will be extracted.
1. Initialize the Aspose Pdf() module. Receive the object if successful.
1. Call the function [AsposePdfExtractImage](https://reference.aspose.com/pdf/nodejs-cpp/convert/asposepdfextractimage/).
1. Extract images from the PDF file. Thus, if 'json.errorCode' is 0, the result of the operation is saved in "ResultPdfExtractImage{0:D2}.jpg". Where {0:D2} represents the page number with a two-digit format. The images are saved with a resolution of 150 DPI. If the json.errorCode parameter is not 0 and, accordingly, an error appears in your file, the error information will be contained in 'json.errorText'.

```mjs

    import AsposePdf from './/AsposePDFforNode.mjs';
    const AsposePdfModule = await AsposePdf();
    const pdf_file = 'ReadMe.pdf';
    /*Extract image from a PDF-file with template "ResultPdfExtractImage{0:D2}.jpg" ({0}, {0:D2}, {0:D3}, ... format page number), resolution 150 DPI and save*/
    const json = AsposePdfModule.AsposePdfExtractImage(pdf_file, "ResultPdfExtractImage{0:D2}.jpg", 150);
    console.log("AsposePdfExtractImage => %O", json.errorCode == 0 ? json.filesNameResult : json.errorText);
```
