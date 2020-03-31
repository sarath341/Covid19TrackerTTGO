# Covid19TrackerTTGO
Covid19 Data tracker using TTGO T-Badge E-Paper Display
T-Badge Model: T5_V2.3_2.13 (20190107)

I finally found the error on new displays by adding a newly updated library content (Need to include a line in the example code of TTGO Library example. They forgot to update it in the example code.)

Library Link: https://github.com/lewisxhe/TTGO-EPaper-Series (Follow installation Instruction & Install dependent libraries)

Fixing Error for Black Screen (on New Displays): https://github.com/lewisxhe/TTGO-EPaper-Series/issues/9
Include this Header file for New TTGO T5_v2.3_2.13 Displays and comment all other models.

#include <GxGDE0213B72B/GxGDE0213B72B.h>      // 2.13" b/w

Make sure you have installed all the dependent libraries mentioned in TTGO Library Github Page.

Library Links:
TTGO Epaper - https://github.com/lewisxhe/TTGO-EPaper-Series
Arduino JSON (V6) - https://github.com/bblanchon/ArduinoJson (Old version may conflict, remove old version if it happens)

url1: https://services1.arcgis.com/0MSEUqKaxRlEPj5g/arcgis/rest/services/ncov_cases/FeatureServer/1/query?f=json&where=(Country_Region=%27India%27)&returnGeometry=false&outFields=Country_Region,Confirmed,Recovered,Deaths

The URL1 fetches data as JSON and parsed in the code. I didn't get statewise data, so got that from another website.

Note: Make sure to fetch the data 10 minutes once or hourly once or even more delay. Otherwise the server may overload and block your IP by firewalls.

url2: Steps for thingHTTP on thingspeak
1. Got to Apps>ThingHTTP
2. Create thingHTTP Set Method as GET and enter 
URL as https://www.mohfw.gov.in/ 
Parse String as //*[@id="cases"]/div/div/table/tbody/tr[23]/td[3]

The Parse String can be get by goto the mohfw.gov.in website and right click on the data you want to display, and select inspect element. On the inspect element panel, again right click on the value and copy Xpath. Paste it somewhere and you can able to see the parse string like the above.

3. Save thing and on next page you will get URL like this https://api.thingspeak.com/apps/thinghttp/send_request?api_key=QDTVRQZGP6DCAFPW

4. Replace the URL in Arduino Code on url2 field



