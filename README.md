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





