# html-to-google-sheet


This is the appscript code to use in google sheets
const sheets = SpreadsheetApp.openByUrl("https://docs.google.com/spreadsheets/d/1ZgiaodI7iPaBeJItjvQ9JLFCDjrculOQqRBvx9V3JsU/edit#gid=0");
const sheet = sheets.getSheetByName("Sheet1");
function doPost(e){
  let data = e.parameter;
  sheet.appendRow([data.name,data.email,data.phone]);
  return ContentService.createTextOutput('success')
}
