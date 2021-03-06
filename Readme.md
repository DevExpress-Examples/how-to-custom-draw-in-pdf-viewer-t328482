<!-- default file list -->
*Files to look at*:

* [Form1.cs](./CS/CustomDraw/Form1.cs) (VB: [Form1.vb](./VB/CustomDraw/Form1.vb))
<!-- default file list end -->
# How to custom draw in  PDF Viewer


The PDF Viewer can draw graphics in the PDF document in the <strong>Control.Paint</strong> event handler. <br><br>In this example, the filled rectangle is drawn at any document space when you hold down the left mouse button and move it. 


<h3>Description</h3>

The PDF Viewer gets the mouse position relative to the PDF Viewer by calling the <a href="https://documentation.devexpress.com/#WindowsForms/DevExpressXtraPdfViewerPdfViewer_GetDocumentPositiontopic">PdfViewer.GetDocumentPosition</a> method in the <strong>MouseDown</strong> (when the left mouse is pressed), and&nbsp; <strong>MouseMove</strong> event handlers (when the mouse is moving). <br><br>To draw a filled rectangle in the PDF document, the<strong> RectangleF.FromLTRB</strong> method is called in the Paint event handler. The start and end client points are obtained using the document position in the <a href="https://documentation.devexpress.com/#WindowsForms/DevExpressXtraPdfViewerPdfViewer_GetClientPointtopic">PdfViewer.GetClientPoint</a> method.

<br/>


