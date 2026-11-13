# BIM Muhandis MCP — oxirgi versiya

## 1.8.0 (13.11.2026)

BIM Muhandis MCP — AI ilovalar (Claude Desktop/Code, ChatGPT, Gemini, Cursor, Windsurf, LM Studio, Cline) uchun Revit, AutoCAD / Civil 3D, Navisworks, Tekla Structures, SketchUp va LIRA-SAPR 2022–2027 ulagichi.

O'rnatish: ZIP'ni chiqarib oling → «BIM Muhandis MCP - O'rnatish.exe» → Claude va Revit'ni qayta oching. AI ilovalar o'zi ulanadi. To'liq o'chirish: «BIM Muhandis MCP - O'chirish.exe».

- AutoCAD 2026 xatolari tuzatildi — acad_drawing_info (katta chizmalarda NullReference), acad_list_layouts (DictionaryEntry), acad_run_csharp (C# kompilyatori AutoCAD bundle'iga nusxalanmagan edi)
- AutoCAD / Civil 3D lentasida Revit'dagi kabi «BIM Muhandis MCP» paneli (logotip, MCP: ON/OFF, Jurnal, Bildirishnoma), sozlamalar oynasi har bir dastur oynasi o'rtasida ochiladi
- chap yuqoridagi holat oynasi (Bajarildi
- Xato
- Qaytarildi) endi AutoCAD, Civil 3D, Navisworks, Tekla, SketchUp va LIRA'da ham
- AutoCAD +25 tool: istalgan buyruq va AutoLISP (GeoUzPro, ModPlus, СПДС kabi plaginlar buyruqlari ham), lenta tugmalarini bosish, tizim o'zgaruvchilari, skrinshot, tanlash, har qanday element xossalari, statistika, blok atributlari (CSV), dinamik bloklar, XREF, listlar va viewport, PDF chop etish, DXF/WBLOCK, DWG qo'yish, multileader, qatlamlarni birlashtirish
- Civil 3D: profillar va PVI, quvur tarmoqlari, COGO nuqtalar, koridorlar
- Revit: boshqa plaginlarni boshqarish — D5 Render, Enscape, ModPlus, BIM Muhandis plagini, pyRevit… tugmalari ekranni egallamasdan bosiladi (rvt_list_addin_buttons, rvt_run_addin_button), Revit buyruqlari (rvt_post_revit_command), skrinshot
- istalgan Windows dasturi oynasi bilan ishlash (bm_ui_*): plagin dialoglari, D5, Enscape, LIRA oynalarini o'qish, tugma bosish, matn yozish, rasm
- SketchUp 2022–2027 ulagichi (skp_): jism, devor, ekstruziya, komponentlar, materiallar, teglar, sahnalar, kesim, atributlar, statistika (hajm, maydon), eksport/import, skrinshot, erkin Ruby
- LIRA-SAPR: karkas hisob sxemasini parametrlardan yaratish (ustun, rigel, plita to'ri), sxemani tahrirlash, natija jadvallari tahlili (eng katta kuch/ko'chish), LIRA holati va faylni LIRA'da ochish
- Navisworks va Tekla skrinshot
- AI rasmni o'zi ko'radi (MCP image)
- AI ilovalar: Windsurf, LM Studio (mahalliy AI), Cline qo'shildi, VS Code + Copilot olib tashlandi; Claude o'rnatilmagan kompyuterda bim-muhandis.mcpb bosilsa — hamma AI ilovalarga ulanadi
