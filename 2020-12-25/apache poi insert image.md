### apache poi insert image 


[Busy Developers' Guide to HSSF and XSSF Features](http://poi.apache.org/components/spreadsheet/quick-guide.html#Images "Busy Developers' Guide to HSSF and XSSF Features")


 

```
//create a new workbook
Workbook wb = new XSSFWorkbook(); //or new HSSFWorkbook();
//add picture data to this workbook.
InputStream is = new FileInputStream("image1.jpeg");
byte[] bytes = IOUtils.toByteArray(is);
int pictureIdx = wb.addPicture(bytes, Workbook.PICTURE_TYPE_JPEG);
is.close();
CreationHelper helper = wb.getCreationHelper();
//create sheet
Sheet sheet = wb.createSheet();
// Create the drawing patriarch.  This is the top level container for all shapes.
Drawing drawing = sheet.createDrawingPatriarch();
//add a picture shape
ClientAnchor anchor = helper.createClientAnchor();
//set top-left corner of the picture,
//subsequent call of Picture#resize() will operate relative to it
anchor.setCol1(3);
anchor.setRow1(2);
Picture pict = drawing.createPicture(anchor, pictureIdx);
//auto-size picture relative to its top-left corner
pict.resize();

```
