# location-tr
function doPost(e) {
  var sheet = SpreadsheetApp.openByUrl("https://script.google.com/macros/s/AKfycbytkngyKqulxJ70oZDgtuv7PgDHhs6e10mv5MvDjkvOetG-DWQahhMzqPHS7jfbaRQZ1Q/exec").getActiveSheet();
  var data = JSON.parse(e.postData.contents);
  sheet.appendRow([new Date(), data.latitude, data.longitude]);
  return ContentService.createTextOutput("OK");
}
