<p align="center">
  <img src="assets/logo.png" width="110" alt="BIM Muhandis">
</p>

<h1 align="center">BIM Muhandis MCP</h1>

<p align="center">
  <b>Revit · AutoCAD / Civil 3D · Navisworks · Tekla Structures · LIRA-SAPR · Dynamo — sun'iy intellekt (AI) bilan</b><br>
  Claude, ChatGPT, Gemini, VS Code + Copilot va Cursor ilovalarini muhandislik dasturlariga ulaydigan MCP server
</p>

<p align="center">
  <img src="https://img.shields.io/badge/versiya-1.4.0-1F3A5F" alt="versiya">
  <img src="https://img.shields.io/badge/tool'lar-460%2B-2E7D32" alt="tool'lar">
  <img src="https://img.shields.io/badge/dasturlar-2022–2027-0277BD" alt="2022–2027">
  <img src="https://img.shields.io/badge/til-o'zbek%20·%20рус%20·%20eng-6A1B9A" alt="til">
  <img src="https://img.shields.io/badge/yangilanish-avtomatik-F57C00" alt="avtomatik yangilanish">
</p>

<p align="center">
  <a href="https://github.com/shohruhorozov251-web/BimMuhandis-releases/releases?q=mcp-v&expanded=true"><b>⬇ Yuklab olish</b></a> ·
  <a href="https://t.me/bim_muhandis1">Telegram</a> ·
  <a href="https://youtube.com/@bimmuhandis1?si=dqrcSFMKpDfcP13T">YouTube</a>
</p>

---

**BIM Muhandis MCP** — O'zbekiston qurilish loyihalash amaliyoti uchun yaratilgan dastur. Siz oddiy so'z bilan vazifa yozasiz — AI modelni o'qiydi, elementlarni yaratadi, armaturalaydi, LIRA hisobi bilan solishtiradi, to'qnashuvlarni topadi, rasmiylashtiradi va natijani tekshiradi.

> «LIRA'dagi armatura jadvalini o'qib, 2-qavat rigellaridagi Revit armaturasi yetarlimi — tekshir. Yetmagan joylarni ko'rsat.»
>
> «Navisworks'da КЖ bilan ОВ orasidagi to'qnashuvlarni top va qizil qilib ko'rsat.»
>
> «Tekla'da 1-o'q bo'yicha balkalarni 4Ø20 / 3Ø16, xomut Ø8 @100/@200 bilan armaturala.»

### Bir qarashda

| | |
|---|---|
| ✅ **460+ tool** | Revit 340+, AutoCAD/Civil 3D 40+, Navisworks 34, Tekla 36, LIRA 8 |
| ✅ **6 ta dastur, 2022–2027** | bitta MCP server — hammasi bilan |
| ✅ **LIRA ↔ Revit solishtirish** | hisoblangan armatura (AS, ASW) Revit'da chizilgan sterjenlar bilan kesim-kesim taqqoslanadi |
| ✅ **Avtomatik clash** | Navisworks'da to'qnashganlar qizil/sariq, qolgani shaffof — bitta buyruq yoki o'zi |
| ✅ **КЖ va КМ qoidalari** | himoya qatlami, xomut qadamlari, нахлёст, СФ/МН/ИК markalari, ведомость, раскрой |
| ✅ **Xavfsiz** | har amal bitta tranzaksiya (Ctrl+Z), xatoda avtomatik bekor, to'liq ID tarixi, «faqat o'qish» |
| ✅ **Erkin C# kodi** | Revit, AutoCAD, Navisworks, Tekla — tayyor tool yetmasa AI o'zi API kodi yozadi |
| ✅ **Avtomatik yangilanish** | ModPlus kabi — fonda; «Yangilanishni tekshirish» bosilsa darhol o'rnatiladi |
| ✅ **O'zbek / рус / english** | interfeys, o'rnatuvchi, kunduzgi va tungi mavzu |

## 1.4.0 da yangi

- 🔁 **LIRA ↔ Revit** — `lira_read_reinforcement` (Подобранная арматура: AS1…AS4, ASW), `lira_suggest_bars` (As → «4Ø20» yoki «Ø12 qadam 150»), `lira_compare_revit` (yetarli / yetmaydi, %, eng yomon joylar)
- 🏗 **Revit КМ** — markalash, ведомость металлоконструкций (ГОСТ 21.502, CSV), раскрой, ferma, Steel Connections tugunlari, tekshiruv
- 🔴 **Navisworks** — `quick_clash`, avtomatik clash rejimi, CSV/HTML hisobot, guruhlash, o'lchash, xossa bo'yicha ranglash, yig'indilar
- 🧱 **Tekla** — balka/kolonna/plita armaturasi bir chaqiruvda, poydevor, devor paneli, bolt, payvand, kesish, fitting, komponentlar, yig'malar, metall tekshiruvi
- 🗺 **Civil 3D** — sirtlar, nuqtadagi balandlik, kotlovan hajmi (qazish/to'kish), trassa va profil, nuqtalardan sirt
- ⚡ **Tezlik** — tool ro'yxati va ulagich holati xotirada saqlanadi

---

## Qo'llab-quvvatlanadigan dasturlar

| Dastur | 2022 | 2023 | 2024 | 2025 | 2026 | 2027 | Qanday ishlaydi |
|---|:-:|:-:|:-:|:-:|:-:|:-:|---|
| **Autodesk Revit** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | Revit ichidagi ulagich («Надстройки» → «BIM Muhandis MCP») |
| **AutoCAD / Civil 3D** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | Ulagich avtomatik yuklanadi; Civil 3D'da qo'shimcha `civil_*` tool'lar |
| **Navisworks Manage / Simulate** | ✅ | ✅ | ✅ | ✅ | ✅ | ⏳ | Plagin («Надстройки» → «BIM Muhandis MCP: ON/OFF»); 2027 — API paketi chiqishi bilan |
| **Tekla Structures** | ✅ | ✅ | ✅ | ✅ | ✅ | ⏳ | Open API; Tekla ochiq bo'lsa o'zi ulanadi; 2027 — Trimble chiqarishi bilan |
| **LIRA-SAPR** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | Fayl orqali (.txt sxema, .xlsx/.csv/.html natijalar) — LIRA ochiq bo'lishi shart emas |
| **Dynamo for Revit** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | AI Python grafini yozadi va Dynamo'da ishga tushiradi |

## Imkoniyatlar xaritasi

| Imkoniyat | Revit | AutoCAD | Navisworks | Tekla | LIRA |
|---|:-:|:-:|:-:|:-:|:-:|
| Modelni o'qish, qidirish, xossalar | ✅ | ✅ | ✅ | ✅ | ✅ |
| Elementlar yaratish | ✅ | ✅ | — | ✅ | ✅ (sxema) |
| Temir-beton armatura | ✅ | — | — | ✅ | ✅ (hisob) |
| Metall konstruksiya (КМ) | ✅ | — | — | ✅ | — |
| MEP (quvur, havo kanali, lotok) | ✅ | — | ✅ (clash) | — | — |
| To'qnashuvlar (clash) | ✅ | — | ✅ avtomatik | ✅ | — |
| Hisob, ведомость, спецификация | ✅ | ✅ | ✅ | ✅ | ✅ |
| Rasmiylashtirish, listlar, eksport | ✅ | ✅ | ✅ (hisobot) | ✅ (makros) | — |
| Erkin C# kodi | ✅ | ✅ | ✅ | ✅ | — |

## Qaysi AI ilovalar bilan ishlaydi

| AI ilova | Ulanish | Tool'lar |
|---|---|---|
| **Claude Desktop** | «AI ilovalar» → «Ulash» (avtomatik) | ✅ hammasi |
| **Claude Code** | «Ulash» yoki `claude mcp add` | ✅ hammasi |
| **ChatGPT desktop** (Codex) | «Ulash» — `~/.codex/config.toml` | ✅ hammasi |
| **Gemini CLI / Antigravity** | «Ulash» — `~/.gemini/...` | ✅ hammasi |
| **VS Code + GitHub Copilot** | «Ulash» — `mcp.json` | ✅ ~110 asosiy + qidiruv orqali qolganlari |
| **Cursor** | «Ulash» — `~/.cursor/mcp.json` | ✅ ~35 asosiy + qidiruv orqali qolganlari |

VS Code bitta so'rovda ko'pi bilan 128 ta, Cursor esa 40 ta tool'ni qabul qiladi. Shu ilovalar uchun asosiy tool'lar ko'rsatiladi, qolganlari `bm_find_action` (qidirish) va `bm_run_action` (bajarish) orqali ishlaydi — imkoniyat cheklanmaydi.

> Oddiy veb-versiyalar (chatgpt.com, gemini.google.com) o'z MCP serverini ulashni qo'llamaydi — desktop ilova kerak.

## Qanday ishlaydi

```
 AI ilova (Claude, ChatGPT, Gemini, VS Code, Cursor)
        │  MCP (stdio yoki http://127.0.0.1:PORT/mcp)
        ▼
 BimMuhandisMCP.exe ──── lira_*  (LIRA-SAPR fayllari; Revit bilan solishtirish)
        │  nomli kanal (named pipe), faqat shu kompyuter ichida
        ├──► Revit ulagichi        → rvt_*   (Revit API) ──► Dynamo → rvt_dynamo_*
        ├──► AutoCAD ulagichi      → acad_*  (AutoCAD .NET API, Civil 3D: acad_civil_*)
        ├──► Navisworks plagini    → nw_*    (Navisworks .NET API, Clash Detective)
        └──► Tekla ulagichi (exe)  → tekla_* (Tekla Open API)
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
| `nw_run_csharp` · `tekla_run_csharp` | Navisworks va Tekla Open API bo'yicha C# kod |
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


### Revit — MEP (инженерные сети)

| Tool | Nima qiladi |
|---|---|
| `create_pipe` · `create_duct` · `create_cable_tray` · `create_conduit` | Trassa nuqtalar bo'yicha, burilishlarda tirsak avtomatik |
| `connect_mep` · `get_mep_connectors` · `find_mep_disconnects` | Ulash (tirsak / tройник), ulagichlar, uzilgan joylar |
| `set_mep_size` · `set_pipe_slope` · `set_mep_system_type` · `place_mep_family` | O'lcham, qiyalik (уклон), tizim tipi, uskuna/armatura |
| `list_mep_types` · `list_mep_systems` · `mep_system_elements` · `mep_takeoff` | Tiplar, tizimlar, uzunliklar va fitinglar hisobi |
| `mep_structure_intersections` | ✅ Trassa × konstruksiya kesishmalari — отверстия uchun markaz va tavsiya etilgan teshik o'lchami |

### Revit — КМ (металлоконструкции)

| Tool | Nima qiladi |
|---|---|
| `km_list_members` | Balka, kolonna, bog'lovchilar: profil, po'lat, uzunlik, massa |
| `km_mark` | Markalash: bir xil profil + po'lat + uzunlik → bitta marka (Б-1, К-1, Св-1) |
| `km_vedomost` | ✅ Ведомость металлоконструкций (ГОСТ 21.502) + payvand massasi, CSV |
| `km_cutting_list` | Раскрой: savdo uzunligidan (12 m) nechta kerak, chiqindi % |
| `km_create_truss` | Ferma: warren yoki pratt, panellar soni |
| `km_list_connection_types` · `km_place_connection` | Steel Connections tugunlari |
| `km_check` | Erkin uchlar, takroriy, qisqa, materiali noto'g'ri, markasiz |

### LIRA-SAPR ↔ Revit

| Tool | Nima qiladi |
|---|---|
| `lira_read_reinforcement` | ✅ «Подобранная арматура»: element va kesim bo'yicha AS1…AS4, ASW (ustunlar o'zi taniladi) |
| `lira_suggest_bars` | As → eng tejamli variantlar: «4Ø20», «Ø12 qadam 150», ortiqchalik % |
| `lira_compare_revit` | ✅ Revit'dagi haqiqiy armatura LIRA talabi bilan: har kesim joyida bo'ylama (AS) va xomut (ASW), plitada har plastina markazida (sm²/m) — «yetarli / yetmaydi» |
| `rvt_rebar_layout` | Revit armatura joylashuvi (o'q bo'yicha, tomoni, diametri, qadami) |
| `lira_find_files` · `lira_read_text_model` · `lira_read_table` · `lira_match_elements` · `lira_write_text_model` | Fayllar, sxema, jadvallar, bog'lash, Revit → LIRA |

### Navisworks

| Tool | Nima qiladi |
|---|---|
| `quick_clash` | ✅ Bir chaqiruvda: test → ishga tushirish → to'qnashganlar **qizil/sariq**, qolgani shaffof |
| `auto_clash` | ✅ Avtomatik rejim: model yangilanganda testlar o'zi qayta ishlaydi va bo'yaladi |
| `clash_create_test` · `clash_run` · `clash_results` · `clash_set_status` · `clash_show_result` · `clash_color` · `clash_delete_test` | Clash Detective to'liq |
| `clash_report` · `clash_summary` | CSV/HTML hisobot; qaysi fayl/qatlam juftligida eng ko'p to'qnashuv |
| `find_items` · `get_properties` · `property_summary` · `sum_property` · `tree` | Qidiruv, xossalar, guruhlash, hajm/maydon yig'indisi |
| `select_items` · `hide_items` (isolate) · `color_items` · `color_by_property` · `zoom_to` · `measure` | Ko'rinish, ranglash (legend bilan), o'lchash |
| `list_viewpoints` · `apply_viewpoint` · `save_viewpoint` · `list_selection_sets` · `create_selection_set` · `select_set` | Ko'rinishlar va to'plamlar |
| `append_file` · `save_file` · `run_csharp` | Fayllar va erkin kod |

### Tekla Structures

| Tool | Nima qiladi |
|---|---|
| `rc_beam_rebar` | ✅ Balka/kolonna armaturasi bir chaqiruvda: «4Ø20» pastki, «3Ø16» yuqori, xomut @100/@200, himoya o'qigacha |
| `rc_slab_rebar` | ✅ Plita to'ri: X/Y, pastki/yuqori, diametr va qadam |
| `create_rebar` · `create_rebar_group` · `list_rebars` | Sterjen, guruh (xomutlar), ro'yxat |
| `create_footing` · `create_wall_panel` · `create_plate` · `create_beam` · `create_column` · `create_polybeam` · `create_columns_on_grid` · `create_grid` | Temir-beton va metall detallar |
| `create_bolts` · `create_weld` · `cut_with_part` · `fit_part` | Bolt, payvand, kesish, fitting |
| `insert_component` | ✅ Tekla komponentlari: ulanishlar (End plate, Base plate…), armatura komponentlari |
| `get_assembly` · `add_to_assembly` · `takeoff` · `steel_check` | Yig'malar, hisob (metall/beton/armatura), tekshiruv |
| `find_objects` · `get_properties` · `set_uda` · `modify_parts` · `move_objects` · `copy_objects` · `set_phase` · `run_macro` · `run_macro_code` · `run_csharp` | Qidiruv, UDA, tahrirlash, fazalar, makroslar, kod |

### AutoCAD Civil 3D

| Tool | Nima qiladi |
|---|---|
| `civil_info` · `civil_surfaces` | Sirtlar va trassalar, balandlik statistikasi |
| `civil_surface_elevation` | Nuqtalardagi yer balandligi |
| `civil_volume` | ✅ Kotlovan / planirovka hajmi: qazish, to'kish, maydon |
| `civil_alignments` · `civil_alignment_points` | Trassa, piketlar, yer va loyiha balandliklari |
| `civil_create_surface` | Geodeziya nuqtalaridan TIN sirt |

### Umumiy

`bm_status` (qaysi dastur ochiq) · `bm_select_target` (bir nechta nusxa) · `rvt_bm_rules` (firma qoidalari) · `bm_find_action` / `bm_run_action` (VS Code va Cursor uchun)

---


## Boshqa Revit MCP'lar bilan solishtirish

| Imkoniyat | **BIM Muhandis MCP** | rvt-mcp | mcp-server-for-revit | BimOn MCP |
|---|:-:|:-:|:-:|:-:|
| Revit 2022–2027 | ✅ | ✅ | ⚠️ | ⚠️ 2025+ |
| КЖ armatura va tekshiruvlar | ✅ | ⚠️ | ❌ | ❌ |
| КМ: markalash, ведомость, раскрой | ✅ | ❌ | ❌ | ❌ |
| MEP | ✅ | ✅ | ⚠️ | ❌ |
| LIRA-SAPR va LIRA ↔ Revit solishtirish | ✅ | ❌ | ❌ | ❌ |
| AutoCAD / Civil 3D | ✅ | ❌ | ❌ | ✅ |
| Navisworks (avtomatik clash) | ✅ | ❌ | ❌ | ✅ |
| Tekla Structures | ✅ | ❌ | ❌ | ❌ |
| O'zbek / rus interfeysi | ✅ | ❌ | ❌ | ❌ |
| Avtomatik yangilanish | ✅ | ⚠️ | ❌ | ❌ |

<sub>✅ bor · ⚠️ qisman · ❌ yo'q. 2026-yil noyabr holatiga, ochiq hujjatlar va sinovlar asosida.</sub>

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
| AutoCAD / Civil 3D ulagichi | `%AppData%\Autodesk\ApplicationPlugins\BimMuhandisMcp.bundle` |
| Navisworks plagini | `%AppData%\Autodesk Navisworks Manage 20XX\Plugins\BimMuhandis.Mcp.Navis` |
| Tekla ulagichi | `%LocalAppData%\Programs\BIM Muhandis MCP\Tekla\T20XX` |
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

✅ ModPlus kabi: Revit ochilganda (va trey dasturi har 6 soatda) yangi versiya tekshiriladi, **fonda yuklanadi va o'rnatilgan papkaga qo'yiladi** — o'rnatuvchi ishga tushmaydi, Revit'ni yopish shart emas.

✅ **«Yangilanishni tekshirish»** (Haqida bo'limi) bosilsa — yangi versiya **darhol** yuklanadi va o'rnatiladi; Navisworks plagini va Tekla ulagichi ham o'zi yangilanadi. Revit/Navisworks keyingi ochilganda yangi versiya ishlaydi.

## Sozlamalar (Revit ichida ochiladi)

Lenta: **«Надстройки» → «BIM Muhandis MCP» → «Sozlamalar»**

- Revit/AutoCAD/Navisworks ochilganda MCP avtomatik yoqilsin
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
