---
lang: he-IL
layout: wiki
section: gbarunner2
title: מידע לגבי הBIOS של הGBA
description: מידע לגבי הBIOS של הGBA וכיצד לחלץ אותו
---

על מנת שGBARunner2 יוכל להפעיל משחקים, נדרש עותק של הBIOS של הGBA. גרסאות חדשות יותר של GBARunner2 (שמגיעות עם הגרסה האחרונה של TWiLight Menu++) כוללות את [Normatt's Open Source BIOS](https://github.com/Normmatt/gba_bios). אבל מאחר וזה לא העתק מדויק, שימוש בעותק רשמי של הBIOS משפר את התאימות. ניתן לחלץ עותק רשמי של הGBA BIOS באמצעות אחת מהשיטות הבאות.

### מדריכי חילוץ

- [GBA/DS/DS Lite with GBA flashcart or 3DS](https://glazedbelmont.github.io/gbabiosdump/)
   - It is **not** possible to dump the GBA BIOS on a DSi
- [Wii (not Family edition)/GameCube, GBA, and link cable dumper](https://github.com/FIX94/gba-link-cable-dumper)

לאחר חילוץ הBIOS, חייב לשנות את שמו ל`bios.bin` ולשים אותו ב`sd:/`, `sd:/gba/` או ב`sd:/_gba/` בשביל שGBARunner2 יוכל לקרוא אותו.

ניתן לוודא שהעותק הוא תקין על ידי השוואה שלו עם הchecksums הבאים:

GBA/GBA SP/Game Boy Micro/Game Boy Player:
- **CRC-32:** `81977335`
- **MD5:** `a860e8c0b6d573d191e4ec7db1b1e4f6`{:.wrap}
- **SHA-1:** `300c20df6731a33952ded8c436f7f186d25d3492`{:.wrap}
- **SHA-256:** `fd2547724b505f487e6dcb29ec2ecff3af35a841a77ab2e85fd87350abd36570`{:.wrap}

DS/DS Lite/3DS Family:
- **CRC-32:** `a6473709`
- **MD5:** `1c0d67db9e1208b95a1506b1688a0ad6`{:.wrap}
- **SHA-1:** `c11531d5261006810cdc954bd4bec0afe3187b35`{:.wrap}
- **SHA-256:** `782eb3894237ec6aa411b78ffee19078bacf10413856d33cda10b44fd9c2856b`{:.wrap}

If you don't know how to obtain a file checksum, you can use an [online checksum calculator](https://emn178.github.io/online-tools/crc32_checksum.html).
