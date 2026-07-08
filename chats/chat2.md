# 設計與施工時程規劃

_Started 2026-07-07 10:13 UTC_

---

## User

現在我要來推敲時程。
我要跟業主說明包含但不限於以下事件和程序的順序和所需時間：

[簽約前] 
PP階段：場勘、初步需求訪談、平面配置提案
[簽約] 
[簽約後] 
SD階段：概念設計簡報、工程預算推演、詳細時程表
DD階段：細部設計簡報、消防/機電/建築送審用繪圖
CD階段：施工圖冊製作、發包
CA階段：施工期間品質管理及監工

請以2027二月底前業主入駐、2026七月為PP階段，七底簽約後，緊接著八月開始SD，推算後續設計及審查、工期(以二個月抓)等時程，來推敲出時間軸。

請參考網路資料，合理推敲消機建的繪圖、掛件和審查所需時間。

## Assistant

_[tool: list_files]_

_[tool: web_search]_

_[tool: read_file]_

_[tool: web_search]_

_[tool: read_file]_

_[tool: web_search]_

_[tool: web_search]_

_[tool: read_file]_

## Assistant

_[tool: list_files]_

_[tool: read_file]_

_[tool: grep]_

_[tool: web_search]_

_[tool: web_search]_

_[tool: str_replace_edit]_

_[tool: str_replace_edit]_

_[tool: str_replace_edit]_

Now add the JS data for `tlSignDate`, `tlMoveInDate`, `tlMonths`, `tlRows`.

_[tool: dc_js_str_replace]_

_[tool: ready_for_verification]_

已加入「05 詳細時程規劃」章節，含 Gantt 時間軸與推估依據：

以 8/1 起算 SD（4週）→ DD設計定案（2週）→ DD送審圖繪製（2週）→ 消防/室裝送審審查（約6週，含補正複審）與 CD施工圖+發包（約7週，並行）→ 許可核發+進場準備（1週）→ CA施工（2個月）→ 竣工查驗+軟裝進場（3週）→ 驗收緩衝（2週），總計約7個月，2027/2月底入駐。送審時間依內政部消防署及建築師公會室裝審查法定天數（7–10工作天）並加計實務補正複審抓4–6週。後續章節編號已順移（06分工、07需求、08樣張）。

## User

Found issues — fixing…

## Assistant

_[tool: dc_html_str_replace]_

_[tool: show_html]_

_[tool: show_html]_

Need to scroll to the timeline section to check it.

_[tool: save_screenshot]_

_[tool: save_screenshot]_

_[tool: save_screenshot]_

Good, alignment now looks correct and rows aren't overlapping. Let me check the rest of the rows.

_[tool: save_screenshot]_

_[tool: show_html]_

_[tool: save_screenshot]_

All rows render cleanly with no overlap, correct alignment, and readable labels. Fixed.

_[tool: ready_for_verification]_

已修正 Gantt 列高問題，時程圖各列不再重疊、對齊正常。

## User

把2027/02/04~02/10這幾天block掉，是農曆年假

## Assistant

_[tool: dc_js_str_replace]_

_[tool: dc_js_str_replace]_

Now add the visual band + label in the template:

_[tool: dc_html_str_replace]_

Now add a footnote explaining the impact, and a legend swatch:

_[tool: dc_html_str_replace]_

_[tool: ready_for_verification]_

已在時程圖中標示 2027/02/04–02/10 農曆春節休假（灰色斜紋區塊），並加註：該假期落於竣工查驗／軟裝進場期間，已由 2 週驗收緩衝吸收，暫不影響月底入駐目標。

## User

請再淡化那個blocker，並避免"休"字與上方月份字樣重疊(可以拿掉)

## Assistant

_[tool: dc_html_str_replace]_

_[tool: dc_html_str_replace]_

_[tool: ready_for_verification]_

已移除月份列的「休」字，並將灰色標示區塊透明度降至 0.22，更淡化不搶視覺。

## User

legend要跟著改

## Assistant

_[tool: grep]_

_[tool: read_file]_

_[tool: str_replace_edit]_

_[tool: ready_for_verification]_

已將圖例中的春節假期色塊透明度同步調到 0.22，與時程圖上淡化後的區塊一致。

## User

Logo的"client"字樣拿掉

## Assistant

_[tool: str_replace_edit]_

_[tool: ready_for_verification]_

已移除 logo 下方的「CLIENT」字樣。

