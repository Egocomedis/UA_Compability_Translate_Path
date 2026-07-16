# UA Compability Translate Path

Патч сумісності для Stellaris: один мод, що пакетно перекриває англійський
слот локалізації українським перекладом для десятків інших модів,
об'єднаних в одній збірці. Гра не підтримує українську мову офіційно, тому
переклад кладеться у файли `..._l_english.yml` з заголовком `l_english:`
всередині — рушій вважає, що це англійська, а показує український текст.

Опубліковано в Steam Workshop: `remote_file_id = 3640770247` (`descriptor.mod`).

## Як це працює

Кожен перекладений мод отримує власну підпапку у форматі:

```
localisation/replace/<Оригінальна назва моду> (<Steam Workshop ID>)/<файли>.yml
```

Внутрішня структура файлів усередині підпапки повторює оригінальну
(мінус мовна папка) — наприклад, якщо оригінальний мод тримав переклад у
`localisation/replace/foo_l_simp_chinese.yml`, тут буде
`.../<Назва моду> (id)/replace/foo_l_english.yml`. Це не обов'язково
функціонально (рушій шукає файли рекурсивно й визначає мову за заголовком
усередині файлу, а не за назвою папки), але зберігає відповідність
структурі оригіналу для зручності звірки.

Оскільки цей патч — окремий мод, він має завантажуватися **після** усіх
модів, чий текст він перекриває (нижче в списку активних модів = вищий
пріоритет при конфлікті файлів з однаковим відносним шляхом... а тут шлях
свідомо унікальний для кожного мода, тому пріоритет визначається лише тим,
що в грі буде видно останній *завантажений* варіант ключа локалізації —
детальніше дивіться нижче).

## Джерело перекладів

Увесь переклад веде окремий приватний робочий репозиторій
[`stellaris-modpack-dev`](https://github.com/Egocomedis/stellaris-modpack-dev) —
там повний лог роботи (`DEVLOG.md`), глосарій термінів (`glossary.md`) і
необроблені матеріали. Цей репозиторій (`UA_Compability_Translate_Path`) —
лише «дистрибутив»: сюди копіюється вже готовий, перевірений результат з
`translated-mods/` у форматі, придатному для публікації одним модом у
Steam Workshop.

**Якщо мод тут виглядає застарілим або неповним — виправляти в
`stellaris-modpack-dev`, а потім синхронізувати сюди, а не редагувати
напряму тут.**

## Список перекладених модів

| Steam Workshop ID | Назва мода | Джерело |
|---|---|---|
| [3250634000](https://steamcommunity.com/sharedfiles/filedetails/?id=3250634000) | Alice | modpack-dev |
| [1302897684](https://steamcommunity.com/sharedfiles/filedetails/?id=1302897684) | Astronomical Emblem Pack | modpack-dev |
| [3156472795](https://steamcommunity.com/sharedfiles/filedetails/?id=3156472795) | building solt + | modpack-dev |
| [2878396142](https://steamcommunity.com/sharedfiles/filedetails/?id=2878396142) | DAP扩展-永世飞升 | modpack-dev |
| [2411818376](https://steamcommunity.com/sharedfiles/filedetails/?id=2411818376) | Dark Blue UI Remake | modpack-dev |
| [2572843550](https://steamcommunity.com/sharedfiles/filedetails/?id=2572843550) | Elegant Chinese Random Names & Localisation Fix | modpack-dev |
| [2571844795](https://steamcommunity.com/sharedfiles/filedetails/?id=2571844795) | ! Ember UI Remake ! | modpack-dev |
| [2938897848](https://steamcommunity.com/sharedfiles/filedetails/?id=2938897848) | Endless Space 2: Cravers Shipset | modpack-dev |
| [2932557948](https://steamcommunity.com/sharedfiles/filedetails/?id=2932557948) | Endless Space 2: Horatio Shipset | modpack-dev |
| [2935276961](https://steamcommunity.com/sharedfiles/filedetails/?id=2935276961) | Endless Space 2: Sophon Shipset | modpack-dev |
| [2930813098](https://steamcommunity.com/sharedfiles/filedetails/?id=2930813098) | Endless Space 2: Unfallen Shipset | modpack-dev |
| [2930369811](https://steamcommunity.com/sharedfiles/filedetails/?id=2930369811) | Endless Space 2: United Empire Shipset | modpack-dev |
| [2950661639](https://steamcommunity.com/sharedfiles/filedetails/?id=2950661639) | Endless Space 2: Vodyani Shipset | modpack-dev |
| [1067631798](https://steamcommunity.com/sharedfiles/filedetails/?id=1067631798) | Expanded Stellaris Ascension Perks | ⚠️ старий, мода немає у збірці — окреме питання |
| [1998204784](https://steamcommunity.com/sharedfiles/filedetails/?id=1998204784) | Galaxy Generation | ⚠️ старий, мода немає у збірці — окреме питання |
| [2409209888](https://steamcommunity.com/sharedfiles/filedetails/?id=2409209888) | ! Immersive Stellaris Collection ! | modpack-dev |
| [2077186491](https://steamcommunity.com/sharedfiles/filedetails/?id=2077186491) | Machine Shipset | modpack-dev |
| [2868514243](https://steamcommunity.com/sharedfiles/filedetails/?id=2868514243) | Master of Orion: Antaran Shipset | modpack-dev |
| [2868168109](https://steamcommunity.com/sharedfiles/filedetails/?id=2868168109) | Master of Orion: Darlok Shipset | modpack-dev |
| [2887758432](https://steamcommunity.com/sharedfiles/filedetails/?id=2887758432) | Master of Orion: Terran Shipset | modpack-dev |
| [819148835](https://steamcommunity.com/sharedfiles/filedetails/?id=819148835) | Planetary Diversity | modpack-dev |
| [3241119393](https://steamcommunity.com/sharedfiles/filedetails/?id=3241119393) | Planetary Diversity - Ascension Worlds | modpack-dev |
| [3142294658](https://steamcommunity.com/sharedfiles/filedetails/?id=3142294658) | Planetary Diversity - City Sets | modpack-dev |
| [1732437279](https://steamcommunity.com/sharedfiles/filedetails/?id=1732437279) | Planetary Diversity - Exotic Worlds | modpack-dev |
| [1732447147](https://steamcommunity.com/sharedfiles/filedetails/?id=1732447147) | Planetary Diversity - More Arcologies | modpack-dev |
| [1740165239](https://steamcommunity.com/sharedfiles/filedetails/?id=1740165239) | Planetary Diversity - Unique Worlds | modpack-dev |
| [3082164342](https://steamcommunity.com/sharedfiles/filedetails/?id=3082164342) | Real Space - New Arcologies | modpack-dev |
| [1915620447](https://steamcommunity.com/sharedfiles/filedetails/?id=1915620447) | Real Space - Ships in Scaling | modpack-dev |
| [1836457943](https://steamcommunity.com/sharedfiles/filedetails/?id=1836457943) | Real Space - Star Cluster | modpack-dev |
| [2902512011](https://steamcommunity.com/sharedfiles/filedetails/?id=2902512011) | Real Space - The Infestation | modpack-dev |
| [1199002146](https://steamcommunity.com/sharedfiles/filedetails/?id=1199002146) | Reworked Advanced Ascension | ⚠️ старий чернетковий переклад, мод є в збірці (найбільший мод у паці, ~3.6МБ) — у черзі на переклад |
| [3250900527](https://steamcommunity.com/sharedfiles/filedetails/?id=3250900527) | Starbase Extended 3.0 | modpack-dev |
| [2972849902](https://steamcommunity.com/sharedfiles/filedetails/?id=2972849902) | Tall White Reborn | modpack-dev |
| [3267309850](https://steamcommunity.com/sharedfiles/filedetails/?id=3267309850) | The Abyss Contract: EPOCH | modpack-dev |
| [3086143878](https://steamcommunity.com/sharedfiles/filedetails/?id=3086143878) | Tradition UI 4.2~4.0 | modpack-dev |
| [3156474398](https://steamcommunity.com/sharedfiles/filedetails/?id=3156474398) | traits + | modpack-dev |
| [1623423360](https://steamcommunity.com/sharedfiles/filedetails/?id=1623423360) | UI Overhaul Dynamic | modpack-dev |
| [1890399946](https://steamcommunity.com/sharedfiles/filedetails/?id=1890399946) | UI Overhaul Dynamic - Ascension Slots | ⚠️ старий, мода немає у збірці — окреме питання |
| [2244483797](https://steamcommunity.com/sharedfiles/filedetails/?id=2244483797) | [United Fleet]Mobile Shipyard | modpack-dev |
| [2027015321](https://steamcommunity.com/sharedfiles/filedetails/?id=2027015321) | United Fleet Shipset | modpack-dev |
| [2409276081](https://steamcommunity.com/sharedfiles/filedetails/?id=2409276081) | ! Universal Game Rules Patch | modpack-dev |
| [1970249743](https://steamcommunity.com/sharedfiles/filedetails/?id=1970249743) | Warship Girls Advisor | modpack-dev |
| [899929086](https://steamcommunity.com/sharedfiles/filedetails/?id=899929086) | Warship Girls R Species Mod | modpack-dev |
| [3424792050](https://steamcommunity.com/sharedfiles/filedetails/?id=3424792050) | 多彩银河+ 多彩事件拓展 个人修复和修改 | modpack-dev |
| [3243731913](https://steamcommunity.com/sharedfiles/filedetails/?id=3243731913) | 小狐狸的底层框架 | modpack-dev |
| [2752229316](https://steamcommunity.com/sharedfiles/filedetails/?id=2752229316) | 少女前线群星故事集：危机联合扩展 | modpack-dev |
| [2824296980](https://steamcommunity.com/sharedfiles/filedetails/?id=2824296980) | 星之誓约扩展 - Eos曙光女神实验室 | modpack-dev |
| [3284159548](https://steamcommunity.com/sharedfiles/filedetails/?id=3284159548) | 星球建筑槽位扩建决议 | modpack-dev |
| [3261046175](https://steamcommunity.com/sharedfiles/filedetails/?id=3261046175) | 更多主线飞升：物质纪元 | modpack-dev |
| [2409022407](https://steamcommunity.com/sharedfiles/filedetails/?id=2409022407) | 更多旗帜 | modpack-dev |
| [2949117070](https://steamcommunity.com/sharedfiles/filedetails/?id=2949117070) | SHYNZ Portraits Pack | modpack-dev |
| [3160618037](https://steamcommunity.com/sharedfiles/filedetails/?id=3160618037) | 虚空的科技扩展 | modpack-dev |
| [3340600231](https://steamcommunity.com/sharedfiles/filedetails/?id=3340600231) | 迷迭香领袖 | modpack-dev |
| [3103861276](https://steamcommunity.com/sharedfiles/filedetails/?id=3103861276) | 领袖：不，我不要负面特质！ | modpack-dev |
| [2616955720](https://steamcommunity.com/sharedfiles/filedetails/?id=2616955720) | 额外传统 | modpack-dev |
| [3242109265](https://steamcommunity.com/sharedfiles/filedetails/?id=3242109265) | 额外领袖特质选项+99 | modpack-dev |
| [2841481791](https://steamcommunity.com/sharedfiles/filedetails/?id=2841481791) | 香草科研助手-Vanilla Research Helper | modpack-dev |
| [3292390779](https://steamcommunity.com/sharedfiles/filedetails/?id=3292390779) | 虚空的更多星系开局 | modpack-dev |

54 моди синхронізовано з `stellaris-modpack-dev` (2026-07-16), 5 модів —
старіші ручні переклади, що передували цьому проєкту.

## Відомі проблеми

**Planetary Diversity (819148835) виправлено (2026-07-16):** старий
чернетковий переклад мав 11 повністю відсутніх біомів (65 ключів:
ash, barnacle, carotene, magma, ravine, silvergrass, sodalite,
superbloom, supraglacial_lakes, thunder, travertine — в
`planetarydiversity_planet_classes_l_english.yml` та відповідні
змінні-посилання в інших файлах модуля), один ключ був перейменований
з `pd_volcano` на `pd_volcanic` (зіткнення з реальним `pd_volcanic` —
довелося повернути справжню назву й додати відсутній), два ключі з
іншого, ще не перекладеного мода (`mod_planet_artisans_unity_produces_add`,
`mod_planet_bio_trophies_unity_produces_add` з 2389589691;
`mod_job_trader_per_pop`(`_short`) з 2907350739) помилково опинилися
в файлах Planetary Diversity — видалено. Наскрізно виправлено
термінологію: «Гайя»/«Гая» → «Гея», «tidally-замкнений»/«тідально
заблокований» → «припливно захоплений» (усталений термін проєкту,
див. glossary.md), кілька суржикових слів («Приспособленість» →
«Придатність», «насучасшніий» → «найсучасніший», «Металосодержащі» →
«Металовмісні») та зламаних перемішаних кирилиця/латиниця слів
(«Кelp» → «Ламінарія»). Знайдено й виправлено зламане посилання
(`pd_domed_mining_site_3_desc` вказувало на опис moonbase замість
mining) і кілька випадків неузгодження роду/відмінку («Цей планет
має» → «Ця планета має» тощо, «Місячну Форпост» → «Місячний Форпост»).

**Dark Blue UI Remake (2411818376) виправлено (2026-07-16):** старий
чернетковий переклад замінено повним — додано 4 пропущені рядки
(`TRTE_btn_ldr_ENTRY_common_failtip_mod`, `MUI_option_REROLL_use_unity`,
`MUI_option_REROLL_use_influence_tip`, `MUI_btn_REROLL_all_tip`),
переписано 2 рядки з вигаданим текстом, що не відповідав оригіналу
(`MUI_option_REROLL_use_credits`/`use_influence` посилалися на
неіснуючі змінні `$@REROLL_credits$`/`$@REROLL_influence$`), виправлено
синтаксичну помилку з нерозірваними лапками (рядки 90, 96 → «ялинки»),
одну явну помилку перекладу («Есмінці» замість «Корвети») та одну
друкарську («Lютий» латиницею замість «Лютий»). Заразом виявлено чужий
файл `FW_MISC/ATEC_l_english.yml`, що насправді належить окремому моду
`! Core Framework of Kasako (2466607238)` (залежність Dark Blue UI, сам
ще не в черзі на переклад) — переміщено у власну підпапку, чернетка там
неповна (лишився невиправлений англійський/китайський текст), доперекласти
пізніше.

При перевірці 2026-07-16 у папках, позначених ⚠️ вище, ще лишилося:

- **Незавершений переклад**: у файлах лишився невиправлений китайський
  текст упереміш з українським —
  `Expanded Stellaris Ascension Perks (1067631798)/esap_l_english.yml`,
  `Galaxy Generation (1998204784)/00_emo_l_english.yml`,
  усі 3 файли `Reworked Advanced Ascension (1199002146)/`.
- **Синтаксична помилка** (літеральні лапки `"` усередині рядка розривають
  значення й ламають парсинг файлу рушієм Paradox — треба замінювати на
  «ялинки» `«...»`):
  - `Reworked Advanced Ascension (1199002146)/AAR_l_english.yml`, рядок 198

`UI Overhaul Dynamic - Ascension Slots (1890399946)` синтаксично чистий,
але не перевірявся на повноту перекладу.

**Виправлення (2026-07-16):** початкове твердження «ці 6 модів не входять
до збірки» було помилковим для трьох із них. Перевірено точно за списком
модів зі збірки (194 моди, файл `no-translate-mods/` у `stellaris-modpack-dev`):

- **Dark Blue UI Remake (2411818376)**, **Planetary Diversity (819148835)**,
  **Reworked Advanced Ascension (1199002146)** — це реальні моди зі збірки,
  просто ще не дійшли руки їх перекласти (два з них — найбільші моди в
  усій паці за обсягом тексту). Додано в чергу `stellaris-modpack-dev`,
  чернетки з помилками вище будуть замінені повноцінним перекладом у
  наступних хвилях.
- **Expanded Stellaris Ascension Perks (1067631798)**,
  **Galaxy Generation (1998204784)**,
  **UI Overhaul Dynamic - Ascension Slots (1890399946)** — дійсно **не
  входять** до збірки з 194 модів. Це залишки окремого ручного перекладу
  користувача під іншу збірку/сейв. У рамках основного проєкту не
  допрацьовуються — це окрема задача, якщо колись знадобиться.

## Формат для Steam Workshop

Готовий опис сторінки моду (з BBCode-розміткою Steam) — у файлі
[`STEAM_DESCRIPTION.bbcode`](./STEAM_DESCRIPTION.bbcode).
