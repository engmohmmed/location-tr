# location-tr
function doPost(e) {
  var sheet = SpreadsheetApp.openByUrl("YOUR_GOOGLE_SHEET_URL").getActiveSheet();
  var data = JSON.parse(e.postData.contents);
  sheet.appendRow([new Date(), data.latitude, data.longitude]);
  return ContentService.createTextOutput("OK");
}
