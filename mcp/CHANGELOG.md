# BIM Muhandis MCP — o'zgarishlar tarixi

## 1.5.3

- Esc ×3 — AI ishini to'xtatish va «Saqlaymi?» oynasi («Yo'q» — oxirgi AI o'zgarishi qaytariladi)
- Uzoq ishda bildirishnomada «Revit band: … — 2:15» va o'tgan vaqt
- Og'ir kod (Revit'ni daqiqalab qotiradigan) bajarilishidan oldin ushlanadi
- Amallar tarixi Claude qayta ochilganda ham saqlanadi
- Bildirishnoma oynasi ochroq va ekran chetidan uzoqroq; yangilanish izohi qisqa

## 1.5.2

- sinov natijasida tuzatishlar — rvt_get_open_dialogs Revit band bo'lganda ham javob beradi (oyna matni Revit oqimini kutmasdan o'qiladi)
- rvt_get_project_info bir xil nomli parametrlarda xato bermaydi
- wf_model_audit — annotatsiya oilalari «ishlatilmagan» deb sanalmaydi, armatura va bir xil elementlarning umumiy markasi bahoni tushirmaydi
- bildirishnoma oynasi oldindan tayyorlanadi (birinchi chaqiruv kutmaydi)
- bm_find_action / bm_run_action har doim ro'yxatda (AI ilovasi yangi tool'larni ko'rmasa ham ishlatish mumkin)
- bm_self_test «id kerak» kabi javoblarni xato deb sanamaydi

## 1.5.1

- Revit oynasida bildirishnoma (chap yuqorida): bajarilayotgan amal va uchta ko'rsatkich — Bajarildi · Xato · Qaytarildi
- ish tugasa 3 soniyada yo'qoladi, xato bo'lsa turadi, X bosilsa keyingi amalgacha yopiladi
- Revit band bo'lsa ham chiziladi, fokusni olmaydi, Revit mavzusiga moslashadi
- Sozlamalar → «Revit'da bildirishnoma oynasi». Tezlik: statistika xotirada (har chaqiruvda diskka yozilmaydi)

## 1.5.0

- ishonchlilik — Revit/AutoCAD qayta ochilsa yoki boshqa hujjat faol bo'lsa yozuvchi amal to'xtatiladi (TARGET_CHANGED, bm_confirm_target)
- har amalga raqam va holat (bm_operation_status, bm_recent_operations — javob kelmasa ham model o'zgardimi bilinadi)
- rvt_batch — bir nechta amal bitta Ctrl+Z da, xato bo'lsa hammasi qaytariladi
- ToolBaker — yaxshi ishlagan kodni doimiy tool qilib saqlash (*_bk_*), firma kutubxonasi GitHub orqali hammaga, bm_suggestions — takrorlangan kod va sekin/xato tool'lar bo'yicha takliflar, bm_tool_stats, bm_self_test
- tayyor ish oqimlari — model auditi (ball), to'qnashuvlar sharhi (qizil rang), hajmlar hisoboti (CSV+HTML), nomlash tekshiruvi, vidlarni tozalash ro'yxati
- eksport — NWC, FBX, DGN, DWF/DWFx, gbXML, STL, OBJ
- spetsifikatsiyalar — ГОСТ/СПДС shakllari (КЖ armatura, КМ, materiallar: ustun kengligi, shrift ГОСТ 2.304, sarlavhalar, guruh sarlavha), ko'p shartli filtr, formula bo'yicha hisoblash, kalit spetsifikatsiya, material takeoff, .rte shablon
- get_schedule_data 10+ marta tez va qatorlari to'liq
- MEP — routing preferences (fitinglar), izolyatsiya, elektr zanjirlari, ikki uskunani avtomatik trassa bilan ulash, teshik o'lchami quvur tashqi diametri bo'yicha

## 1.4.0

- LIRA ↔ Revit — hisoblangan armaturani o'qish (Подобранная арматура), As bo'yicha sterjen tanlash va Revit'da chizilgan armatura bilan kesim-kesim solishtirish (yetarli / yetmaydi, %)
- Revit KM — markalash, ведомость металлоконструкций, раскрой, ferma, tugunlar, tekshiruv
- Navisworks — tezkor clash bir chaqiruvda va avtomatik rejim (to'qnashganlar qizil/sariq, qolgani shaffof), clash hisoboti (CSV/HTML), guruhlash, o'lchash, xossa bo'yicha ranglash, yig'indilar
- Tekla — balka/kolonna/plita armaturasi bir chaqiruvda, poydevor, devor paneli, bolt, payvand, kesish, fitting, komponentlar (ulanish/armatura), yig'malar, setka bo'yicha kolonnalar, metall tekshiruvi
- Civil 3D — sirtlar, balandlik, hajm (kotlovan), trassa va profil, sirt yaratish
- versiyalar 2022–2027
- tezlik — tool ro'yxati va ulagich holati xotirada

## 1.3.0

- Navisworks ulagichi (nw_: model daraxti, qidiruv, xossalar, tanlash, yashirish/ajratish, ranglash, viewpoint, tanlov to'plamlari, Clash Detective — test yaratish, ishga tushirish, natijalar, holat; fayl qo'shish, saqlash, rasm; erkin C#)
- Tekla Structures ulagichi (tekla_: qidiruv, xossalar va UDA, balka/kolonna/plastina/polibalka, o'zgartirish, siljitish, nusxalash, setka, armatura — sterjen va guruh, hisob, fazalar, makroslar, erkin C#; Tekla ochiq bo'lsa o'zi ulanadi)
- Revit MEP tool'lari (quvur, havo kanali, kabel lotogi, elektr kanali trassalari, ulash, tройник/tirsak, ochiq uchlar, o'lcham, qiyalik, tizimlar, MEP hisobi, konstruksiyalar bilan kesishish — отверстия uchun)

## 1.2.6

- Revit tool'lari 310 dan ortiq (parametrlarni ommaviy tahrirlash, CSV eksport/import, КЖ tekshiruvlari, beton hajmi va qolip, armatura pozitsiyalari, vidlar, listlar, annotatsiya, bog'lamalar, tanlov to'plamlari)
- har bir amaldan keyin qo'shilgan / o'zgargan / o'chirilgan elementlarning to'liq ID ro'yxati
- xato bo'lsa o'zgarishlar avtomatik bekor qilinadi, ogohlantirishlar jurnalga yoziladi
- Revit ichida «Hisobot» oynasi (elementga bosib ko'rish)
- C# kodini faqat kompilyatsiya qilib tekshirish
- bir nechta Revit ochiq bo'lsa PID bo'yicha tanlash
- ochiq dialog oynalarni ko'rish va yopish

## 1.2.5

- tezlik — so'rov kelganda Revit darhol uyg'otiladi (sichqonchani qimirlatishni kutmaydi), C# kodi Revit'dan tashqarida kompilyatsiya qilinadi, kesh va oldindan isitish bilan

## 1.2.4

- C# kodi tasdiq oynasida «Ha, doim ruxsat berish» — bir marta tanlansa boshqa so'ralmaydi

## 1.2.3

- YouTube kanal havolasi, mavzu tugmalari tartibga keltirildi, logotip burchaklari yumaloq, rvt_create_spot_elevation tool'i tuzatildi

## 1.2.2

- sarlavhada mavzu tugmalari (kunduzgi · tungi · avtomatik), til tanlashda bayroqlar, «Haqida»da Telegram kanali va asoschilar

## 1.2.1

- oyna mavzusi Revit mavzusiga ergashadi (tungi/kunduzgi)

## 1.2.0

- 250+ tool — modellashtirish (devor, plita, kolonna, balka, poydevor, teshik), arxitektura (eshik, deraza, xona, pardoz), metall konstruksiya, vidlar va filtrlar, rasmiylashtirish (отметка, o'lcham, обрыв, spetsifikatsiya), eksport (PDF, DWG, IFC), AutoCAD uchun 21 yangi tool
- firma qoidalari fayli (bm_rules)
- Dynamo bilan bog'lanish (AI Python grafini yozadi va Dynamo'da ishga tushiradi)
- VS Code va Cursor uchun tool soni cheklovi

## 1.1

- erkin C# kodi, Sozlamalar Revit ichida, ModPlus kabi yangilanish
