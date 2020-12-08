---
title: "Gs1api issue"
date: 2020-11-27T15:12:22+08:00
draft: false
---

#  Gs1api issue

1. http 404
   - Error: **Request failed with status code 404**
   - Time: 10:38:32.266
   - Get url: http://api.chinatrace.org/AAQI/v1/ProductData/gtin/?targetMarket=156&dataVersion=1.1&clientGln=6901234501681&mac=4A8A61C32414868DF0203AE4701120375CB025DBA6CF44477DC4914986A68F5D
   - Reason: No gtin

2. http 400

   - Error: **Request failed with status code 400**
   - Time: 10:50:23.266
   - Get url: http://api.chinatrace.org/AAQI/v1/ProductData/gtin/01.01.02.007%1?targetMarket=156&dataVersion=1.1&clientGln=6901234501681&mac=A1E9754A9E98599E926542C79DFA171A21C778AED25D127D0202549B37363CC0
   - Reason: Error gtin format

3. http 500

   - Error: **Request failed with status code 500**

   - Time: 10:50:02.501

   - Get url: http://api.chinatrace.org/AAQI/v1/ProductData/gtin/D0034055275011?targetMarket=156&dataVersion=1.1&clientGln=6901234501681&mac=7890492600E48714E0D4A28C1F1157B4D33B4205D818BDDF54F849FB37D67D71

   - Reason: **Request processing failed; nested exception is java.lang.NumberFormatException: For input**

     ​        **string** (Error gtin format)

4. TypeError

   - Error: **TypeError [ERR_UNESCAPED_CHARACTERS]: Request path contains unescaped characters**
   - Time: 10:34:20.381
   - Get url: http://api.chinatrace.org/AAQI/v1/ProductData/gtin/16544009058?targetMarket=156&dataVersion=1.1&clientGln=6901234501681&mac=D81723F7DAA6161BF8C5E17CFB92C6D4BE44D4A31B36017C0A3AE1F7916991A6
   - Reason: Error MAC

