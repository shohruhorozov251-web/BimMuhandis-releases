<p align="center">
  <img src="assets/logo.png" width="110" alt="BIM Muhandis">
</p>

<h1 align="center">BIM Muhandis MCP</h1>

<p align="center">
  <b>Revit · AutoCAD · LIRA-SAPR — sun'iy intellekt (AI) bilan ishlash</b><br>
  Claude, ChatGPT, Gemini, VS Code + Copilot va Cursor ilovalarini Revit, AutoCAD va LIRA-SAPR ga ulaydigan MCP server
</p>

<p align="center">
  <a href="https://github.com/shohruhorozov251-web/BimMuhandis-releases/releases?q=mcp-v&expanded=true"><b>⬇ Yuklab olish</b></a> ·
  <a href="https://t.me/bim_muhandis1">Telegram</a> ·
  <a href="https://youtube.com/@bimmuhandis1?si=dqrcSFMKpDfcP13T">YouTube</a>
</p>

---

**BIM Muhandis MCP** — O'zbekiston qurilish loyihalash amaliyoti uchun yaratilgan dastur. U AI ilovaga ochiq Revit modeli, AutoCAD chizmasi va LIRA-SAPR fayllari bilan to'g'ridan-to'g'ri ishlash imkonini beradi: siz oddiy so'z bilan vazifa yozasiz — AI modelni o'qiydi, elementlarni yaratadi, armaturalaydi, rasmiylashtiradi va natijani tekshiradi.

> «Kolonnalarni o'qlar kesishmasiga 400x400 qilib qo'y, 2-qavat rigellarini kolonnadan kolonnaga chiz va har bir rigelga xomut qo'y — tayanch yonida @100, o'rtada @200.»

- **350+ tool** (Revit uchun 310 dan ortiq) — temir-beton, metall, arxitektura, rasmiylashtirish, ko'rinishlar, eksport, Dynamo
- **Erkin C# kodi** — tayyor tool yetmagan joyda AI Revit/AutoCAD API bo'yicha o'zi kod yozadi
- **Firma qoidalari** — himoya qatlami, xomut qadamlari, нахлёст, markalash va boshqalar AI'ga beriladi
- **Xavfsiz** — hamma amal bitta tranzaksiyada (Ctrl+Z), «faqat o'qish» rejimi, tasdiq oynasi, jurnal
- **O'zbek / rus / ingliz** interfeysi, kunduzgi va tungi mavzu
- **ModPlus kabi avtomatik yangilanish** — fonda, o'rnatuvchisiz

---

## Qo'llab-quvvatlanadigan dasturlar

| Dastur | Versiyalar | Qanday ishlaydi |
|---|---|---|
| **Autodesk Revit** | 2022 · 2023 · 2024 · 2025 · 2026 · 2027 | Revit ichidagi ulagich (lenta: «Надстройки» → «BIM Muhandis MCP») |
| **Autodesk AutoCAD** | 2022 · 2023 · 2024 · 2025 · 2026 · 2027 | Ulagich avtomatik yuklanadi, 2D chizish (AutoCAD LT qo'llab-quvvatlanmaydi) |
| **LIRA-SAPR** | 2022 – 2026 | Fayl orqali: matnli sxema (.txt), natija jadvallari (.xlsx, .csv, .html) — LIRA ochiq bo'lishi shart emas |
| **Dynamo for Revit** | Revit 2022 – 2027 bilan | AI Python grafini yozadi va Dynamo'da ishga tushiradi |

## Qaysi AI ilovalar bilan ishlaydi

| AI ilova | Ulanish | Tool'lar |
|---|---|---|
| **Claude Desktop** | «AI ilovalar» → «Ulash» (avtomatik) | hammasi (350+) |
| **Claude Code** | «Ulash» yoki `claude mcp add` | hammasi |
| **ChatGPT desktop** (Codex) | «Ulash» — `~/.codex/config.toml` | hammasi |
| **Gemini CLI / Antigravity** | «Ulash» — `~/.gemini/...` | hammasi |
| **VS Code + GitHub Copilot** | «Ulash» — `mcp.json` | ~110 asosiy + qidiruv orqali qolganlari |
| **Cursor** | «Ulash» — `~/.cursor/mcp.json` | ~35 asosiy + qidiruv orqali qolganlari |

VS Code bitta so'rovda ko'pi bilan 128 ta, Cursor esa 40 ta tool'ni qabul qiladi. Shu ilovalar uchun BIM Muhandis MCP asosiy tool'larni ko'rsatadi, qolganlari `bm_find_action` (qidirish) va `bm_run_action` (bajarish) orqali ishlaydi — imkoniyat cheklanmaydi.

> Oddiy veb-versiyalar (chatgpt.com, gemini.google.com) o'z MCP serverini ulashni qo'llamaydi — desktop ilova kerak.

## Qanday ishlaydi

```
 AI ilova (Claude, ChatGPT, Gemini, VS Code, Cursor)
        │  MCP (stdio yoki http://127.0.0.1:PORT/mcp)
        ▼
 BimMuhandisMCP.exe ──── lira_* tool'lari (LIRA-SAPR fayllari)
        │  nomli kanal (named pipe), faqat shu kompyuter ichida
        ├──────────────► Revit ulagichi    → rvt_*  (Revit API, asosiy oqimda)
        │                    └─► Dynamo     → rvt_dynamo_*
        └──────────────► AutoCAD ulagichi  → acad_* (AutoCAD .NET API)
```

Ma'lumotlar internetga chiqmaydi: AI ilova bilan dastur o'rtasidagi aloqa faqat kompyuter ichida bo'ladi.

---

## Imkoniyatlar (tool'lar)

Hamma uzunliklar **mm** da, koordinatalar `[x, y, z]` mm.

### Revit — temir-beton va armatura

| Tool | Nima qiladi |
|---|---|
| `place_column_rebar` | Kolonna armaturasi: bo'ylama sterjenlar va xomutlar (balandlik 3 ga bo'linadi: chetlarida @100, o'rtada @200) |
| `place_beam_longitudinal` | Rigel bo'ylama armaturasi, нахлёст va 1:6 otgib bilan |
| `place_beam_stirrups` | Rigel xomutlari: tayanchdan ≤50 mm, chetki choraklarda @100, o'rtada @200 |
| `place_masonry_mesh` | Kladka setkasi: har 675 mm, teshiklarda uziladi, betonga kirmaydi |
| `create_rebar_from_curves` | Chiziqlar bo'yicha erkin armatura |
| `set_rebar_layout` · `set_rebar_presentation` · `set_rebar_visibility` · `set_rebar_partition` | To'plam qadami/soni, vidda ko'rinishi, «beton ustidan ko'rinadigan», pozitsiya |
| `list_rebar_types` · `create_rebar_bar_type` | Diametrlar va shakllar, yangi armatura tipi |
| `rebar_summary` · `rebar_mass_by_diameter` · `get_rebar_details` | Massa diametrlar bo'yicha (ГОСТ 34028-2016), element bo'yicha hisob |
| `check_rebar_cover` · `check_rebar_outside_host` · `check_duplicates` · `check_positions` | Himoya qatlami, betondan chiqib qolgan, takroriy armatura, pozitsiyalar tekshiruvi |
| `get_rebar_hosts_summary` | Qaysi kolonna/rigel/devor/plita armaturalanmagan |

### Revit — modellashtirish

| Tool | Nima qiladi |
|---|---|
| `create_grid_system` · `create_grid` · `create_level` | O'qlar tizimi (1, 2, 3… / А, Б, В…), sathlar va ularning planlari |
| `create_wall` · `create_floor` · `create_ceiling` · `create_roof` | Devor, plita (fundament plitasi ham), shift, tom |
| `create_column` · `create_columns_at_grids` | Kolonna — nuqtalarda yoki barcha o'q kesishmalarida |
| `create_beam` · `create_beams_on_grids` | Balka/rigel — chiziq bo'yicha yoki o'qlar bo'ylab kolonnadan kolonnagacha |
| `create_isolated_foundation` · `create_wall_foundation` | Ustun osti va lenta poydevor |
| `create_wall_opening` · `create_floor_opening` · `place_family_on_wall` | Devor/plita teshigi, shaxta, shablondagi teshik oilasi |
| `join_geometry` · `unjoin_geometry` · `cut_geometry` | Birlashtirish va kesish tartibi (beton kladkani kesadi, сердечник devorni kesadi) |
| `create_section_type` · `create_wall_type` · `create_floor_type` · `create_material` | 500x700 kabi kesim tiplari, qatlamli devor/plita tiplari, materiallar |
| `rotate_elements` · `mirror_elements` · `array_elements` · `copy_to_levels` · `move_elements` | Burish, ko'zgu, massiv, boshqa qavatlarga nusxalash |
| `set_levels_offsets` · `set_beam_justification` · `set_wall_location_line` · `attach_walls` | Sathlar va siljishlar, balka joylashuvi, devor chizig'i |
| `place_family` · `load_family` · `duplicate_type` · `set_type_parameters` · `set_material` | Oilalar, tiplar, parametrlar, material |

### Revit — metall konstruksiya

`list_steel_profiles` · `create_steel_beam` · `create_steel_column` · `create_brace` · `set_frame_cutback` · `list_steel_connections` · `steel_takeoff` (ведомость металлопроката: profil, uzunlik, massa)

### Revit — arxitektura

`create_door` · `create_window` · `list_doors_windows` · `create_room` · `set_rooms` · `create_room_separator` · `tag_rooms` · `room_finish_takeoff` (pol, devor, shift maydonlari, teshiklarsiz) · `create_floor_finish` · `create_wall_finish`

### Revit — rasmiylashtirish

| Tool | Nima qiladi |
|---|---|
| `create_spot_elevation` | Высотная отметка: pastga qaragan yuzalarga «Вниз», yuqoriga — «Вверх» tipi, bir ustunda |
| `dimension_between` · `dimension_element` · `dimension_grids` | O'lchamlar — model yuzalariga va o'qlarga bog'langan |
| `tag_elements` · `find_untagged` | Markalar va markasiz elementlarni topish |
| `create_text` · `create_detail_lines` · `create_filled_region` · `place_detail_component` | Matn, detal chiziqlar, shtrixovka, обрыв va boshqa 2D elementlar |
| `create_schedule` · `edit_schedule` · `get_schedule_data` · `get_schedule_fields` | Spetsifikatsiyalar: maydonlar, filtr, saralash |
| `create_sheets` · `rename_sheets` · `place_views_on_sheet` · `place_schedule_on_sheet` · `move_viewport` · `set_sheet_parameters` | Listlar, shtamp parametrlari, joylashtirish |
| `create_revision` | Izohlar (revisions) |

### Revit — ko'rinishlar

`create_plan_view` · `create_3d_view` · `create_section` · `create_section_view` · `create_elevation` · `create_callout` · `create_drafting_view` · `duplicate_view` · `duplicate_legend` · `set_view_properties` · `set_view_range` · `crop_view_to_elements` · `set_view_template` · `create_view_template` · `create_view_filter` · `apply_filter` · `hide_elements` · `hide_categories` · `override_graphics` · `reset_graphics` · `color_elements` · `isolate_in_view` · `activate_view` · `zoom_to_elements`

### Revit — o'qish va tekshirish (modelni o'zgartirmaydi)

`model_info` · `get_selection` · `find_elements` · `find_by_mark` · `get_element_info` · `get_parameters` · `get_location` · `get_bounding_box` · `get_quantities` (hajm, maydon, material bo'yicha) · `get_wall_info` · `get_host_and_hosted` · `get_joined_elements` · `measure_distance` · `find_elements_in_box` · `find_intersecting` (to'qnashuvlar) · `find_duplicates_at_same_place` · `get_warnings` · `count_by_level` · `list_categories` · `list_families` · `list_types` · `list_materials` · `list_levels_grids` · `list_views` · `list_sheets` · `list_schedules` · `list_rooms` · `find_unplaced_views` · `find_empty_sheets` va boshqalar

### Revit — eksport va yordamchi

`export_pdf` · `export_dwg` · `export_ifc` · `export_image` · `export_schedule_csv` · `save_model` · `sync_with_central` · `purge_unused` · `select_by_category` · `select_elements`

### Revit — Dynamo

| Tool | Nima qiladi |
|---|---|
| `dynamo_run_python` | AI Python kodini Dynamo grafiga (.dyn) o'raydi va Revit ichidagi Dynamo'da ishga tushiradi; xato bo'lsa — traceback qaytadi, AI tuzatadi |
| `dynamo_run_graph` | Mavjud .dyn grafni ishga tushirish |
| `dynamo_result` · `dynamo_list_graphs` · `dynamo_info` | Natija, saqlangan graflar (Dynamo Player uchun), Dynamo versiyasi |

### Erkin C# kodi

| Tool | Nima qiladi |
|---|---|
| `rvt_run_csharp` | Revit API bo'yicha C# kod: `doc`, `uidoc`, `uiapp` tayyor; bitta tranzaksiya; model o'zgarsa — tasdiq oynasi, «Нет» — hammasi bekor |
| `acad_run_csharp` | AutoCAD .NET API bo'yicha C# kod: `doc`, `db`, `ed`, `tr`, `ms` tayyor; tasdiq bilan |

### AutoCAD — 2D chizish

| Tool | Nima qiladi |
|---|---|
| `draw` | Bitta amalda yuzlab element: chiziq, polyline, to'rtburchak, aylana, yoy, matn, mtext, shtrixovka, o'lchamlar, blok |
| `polyline_from_points` · `grid_axes` | Rasmdan olingan kontur, doirachali koordinata o'qlari |
| `create_layers` · `set_layer_state` · `set_current_layer` · `list_layers` | Qatlamlar |
| `create_text_style` · `create_dim_style` · `set_units` | Matn va o'lcham stillari (GOST), birliklar |
| `offset` · `mirror` · `rotate` · `scale` · `array_rect` · `move_copy` · `explode` · `join_to_polyline` · `erase` · `change_properties` | Tahrirlash |
| `list_blocks` · `insert_block` · `create_block` | Bloklar va atributlar |
| `create_table` · `find_text` · `replace_text` | Jadval (spetsifikatsiya), matn qidirish/almashtirish |
| `get_area` · `measure` · `list_entities` · `drawing_info` · `list_layouts` | Maydon, masofa, chizma ma'lumoti |
| `new_drawing` · `save_as` · `zoom_extents` · `purge` | Fayl amallari |

### LIRA-SAPR

| Tool | Nima qiladi |
|---|---|
| `lira_find_files` | Papkadagi LIRA fayllari (sxema, natija jadvallari) |
| `lira_read_text_model` | Matnli sxema: tugunlar, elementlar, bikrliklar, tayanchlar |
| `lira_read_table` | Natijalar: «Подобранная арматура» (AS1…AS4, ASW), «Усилия», «Перемещения» |
| `lira_match_elements` | LIRA sterjenlarini Revit elementlariga koordinatalar bo'yicha bog'lash |
| `lira_write_text_model` | Matnli sxemani yozish (beta) |

**LIRA → Revit:** AI LIRA'dan tanlangan armaturani o'qiydi, sterjenlarni Revit kolonna/rigellariga bog'laydi va armaturani shu natija bo'yicha joylaydi.

### Umumiy

`bm_status` (qaysi dastur ochiq) · `rvt_bm_rules` (firma qoidalari) · `bm_find_action` / `bm_run_action` (VS Code va Cursor uchun)

---

## Firma qoidalari

AI ishni boshlashdan oldin `%AppData%\BimMuhandis\Mcp\rules.md` faylini o'qiydi. Unda BIM Muhandis amaliyoti yozilgan va uni o'zingiz tahrirlaysiz:

- himoya qatlami — beton yuzasidan armatura **o'qigacha**; odatda 50 mm, teshik chetida 25 mm
- нахлёст 45d (B25), sterjen ≤ 11 700 mm, «1/6» otgib
- rigel: 4 chorak, chetlarida @100, o'rtada @200; ulanish zonalari
- kolonna: balandlik 3 ga bo'linadi
- plita, devor, poydevor, kladka qoidalari; СФ/МН/ИК markalari
- rasmiylashtirish: o'lcham 2.5 mm, обрыв, отметка «Вверх/Вниз», pozitsiya markalari
- armatura standarti — ГОСТ 34028-2016
- ShNK / KMK havolalari uchun bo'lim (hujjat nomi va band raqami bilan to'ldiriladi)

## Xavfsizlik

- Har bir tool bitta tranzaksiya — Revit'da **Ctrl+Z** bilan qaytariladi
- Xato bo'lsa o'zgarishlar **avtomatik bekor qilinadi**, Revit ogohlantirishlari natijaga va jurnalga yoziladi
- Har bir amaldan keyin **qo'shilgan / o'zgargan / o'chirilgan elementlarning to'liq ID ro'yxati** qaytariladi
- Revit ichida **«Hisobot» oynasi** — AI bajargan ishlar, elementga bosib ko'rish va tanlash
- C# kodini **faqat kompilyatsiya qilib tekshirish** (`compile_only`) — modelga tegmasdan
- Bir nechta Revit ochiq bo'lsa **PID bo'yicha tanlash** (`bm_select_target`)
- Revit'dagi **ochiq dialog oynalarni ko'rish va yopish** (`get_open_dialogs`, `close_dialog`)
- **Faqat o'qish** rejimi — AI modelni o'zgartira olmaydi
- **Yozishdan oldin so'rash** — har o'zgarishdan oldin tasdiq oynasi
- **Ruxsat etilgan tool'lar** — guruhlarni (armatura, o'chirish, eksport, C# kodi, Dynamo…) alohida yoqish/o'chirish; o'chirish sukut bo'yicha yopiq
- **Jurnal** — AI qilgan har bir amal (vaqt, tool, natija); C# kodi matni ham yoziladi
- Aloqa faqat kompyuter ichida (named pipe); HTTP yoqilsa — faqat `127.0.0.1` va kalit bilan

---

## O'rnatish

1. [Releases](https://github.com/shohruhorozov251-web/BimMuhandis-releases/releases?q=mcp-v&expanded=true) bo'limidan oxirgi `BimMuhandisMCP-Setup-X.Y.Z.exe` ni yuklab oling.
2. O'rnating (administrator huquqi shart emas). Windows SmartScreen chiqsa: **«Подробнее» → «Выполнить в любом случае»**. Revit ochiq bo'lsa ham o'rnatsa bo'ladi.
3. O'rnatgach oyna ochiladi: **«AI ilovalar»** bo'limida kerakli ilovani **«Ulash»** bosing.
4. AI ilovani to'liq yoping (treydan **«Выйти»/«Quit»**) va qayta oching.
5. Revit'ni oching — **«Надстройки»** tabida **«BIM Muhandis MCP»** paneli paydo bo'ladi, **«MCP: ON»** yoqilgan bo'lsin.
6. AI ilovada yozing: «Revit bilan bog'lan» — AI `bm_status` bilan tekshiradi.

| Nima | Qayerda |
|---|---|
| Dastur | `%LocalAppData%\Programs\BIM Muhandis MCP` |
| Sozlamalar, jurnal, qoidalar | `%AppData%\BimMuhandis\Mcp` |
| Revit ulagichi | `%AppData%\Autodesk\Revit\Addins\20XX\BimMuhandis.Mcp.addin` |
| AutoCAD ulagichi | `%AppData%\Autodesk\ApplicationPlugins\BimMuhandisMcp.bundle` |
| Dynamo graflari | `%AppData%\BimMuhandis\Mcp\dynamo` |
| Claude Desktop sozlamasi | `%AppData%\Claude\claude_desktop_config.json` |

### Qo'lda ulash («Ulash» ishlamasa)

Claude Desktop: **Настройки → Разработчик → «Изменить конфигурацию»** va `mcpServers` ichiga qo'shing:

```json
"bim-muhandis": {
  "command": "C:\\Users\\<FOYDALANUVCHI>\\AppData\\Local\\Programs\\BIM Muhandis MCP\\BimMuhandisMCP.exe",
  "args": ["--stdio"]
}
```

Boshqa ilovalar uchun tayyor JSON: **«AI ilovalar» → «JSON nusxalash»**.

**Ulanmasa — tekshiring:**
- AI ilova to'liq yopilib qayta ochildimi (faqat oynani yopish yetmaydi)
- Revit'da **«MCP: ON»** yoqilganmi
- `Настройки → Разработчик` da `bim-muhandis` yonida **«Выполняется» / «running»** yozuvi bormi; xato bo'lsa — «Просмотреть логи»
- Yangi suhbat ochildimi (ochiq suhbatga yangi server qo'shilmaydi)

## Yangilanish

ModPlus kabi: Revit ochilganda (va trey dasturi har 6 soatda) yangi versiya tekshiriladi, **fonda yuklanadi va o'rnatilgan papkaga qo'yiladi** — o'rnatuvchi ishga tushmaydi, Revit'ni yopish shart emas. Revit keyingi ochilganda yangi versiya ishlaydi va «Yangiliklar» oynasi chiqadi. Qo'lda: **Haqida → «Yangilanishni tekshirish»**.

## Sozlamalar (Revit ichida ochiladi)

Lenta: **«Надстройки» → «BIM Muhandis MCP» → «Sozlamalar»**

- Revit/AutoCAD ochilganda MCP avtomatik yoqilsin
- HTTP manzil (stdio'ni qo'llamaydigan ilovalar uchun)
- Faqat o'qish · yozishdan oldin so'rash · C# kodi o'zgartirsa so'rash · har bosqichdan keyin saqlash
- Ruxsat etilgan tool guruhlari
- Til: o'zbekcha / русский / english
- Mavzu: ☀ kunduzgi · ☾ tungi · 🖥 avtomatik (Revit mavzusiga ergashadi)

---

## BIM Muhandis plagini

Shu repozitoriyada Revit uchun **BIM Muhandis** plagini (`v0.99.x` relizlari) ham chiqariladi: armatura, kladka setkasi, uzellar kutubxonasi, markalar, spetsifikatsiyalar, listlar, PDF/DWG eksport va AI yordamchi — ModPlus uslubidagi lenta bilan. Plagin sozlamalarida **«BIM Muhandis MCP ni yuklab oling»** bo'limi bor.

## Aloqa

- Telegram: [t.me/bim_muhandis1](https://t.me/bim_muhandis1)
- YouTube: [@bimmuhandis1](https://youtube.com/@bimmuhandis1?si=dqrcSFMKpDfcP13T)

**Asoschilar — BIM Muhandis jamoasi:**
Keldiyor Shokir Toshtemirov · Shohruh O'tkir O'rozov

<p align="center"><i>«BIM Muhandis» plagini va «BIM Muhandis MCP» ga bildirgan ishonchingiz uchun rahmat!</i></p>
