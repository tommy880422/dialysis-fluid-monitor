# 居家水分監測（課堂作業原型）

[English version](#home-fluid-monitoring-class-project-prototype)

給血液透析病人在家使用的水分監測網頁原型。病人輸入兩種非侵入式量測的結果（ReDS 背心的肺水 %LW、MoistureMeter 的皮膚水分），加上體重、血壓和喘的程度，系統依文獻訂的規則計分，給出綠、黃、紅燈號，並畫出水分變化趨勢。

**線上瀏覽：** https://tommy880422.github.io/dialysis-fluid-monitor/

> 這是課堂作業原型，判讀規則僅供示範，不能取代醫療判斷。網頁內是示範資料；自己輸入的資料只存在你的瀏覽器裡。

## 功能

- **首頁**：燈號、距離上次透析天數、長間隔提醒、個人基準建立進度
- **量測精靈**（7 步）：量測前檢查（熱或流汗時倒數 15 分鐘）、體重、血壓心跳、皮膚水分連量 3 次（自動算 CV，> 10% 要求重量）、ReDS 肺水、喘的程度
- **結果頁**：燈號、建議、逐條計分明細
- **趨勢頁**：肺水、皮膚水分、體重的折線圖，標出透析日與個人基準範圍
- **紀錄頁**、**判讀標準頁**（每條規則附 PubMed 連結與證據強度）
- **設定頁**：病人自填區、醫護設定區（示範密碼 1234）、個人基準（自動計算）

## 判讀規則摘要

| 條件 | 分數 |
|---|---|
| 肺水 %LW ≥ 35%（安全底線） | +2 |
| 肺水 %LW 26.5–34.9% | +1 |
| 肺水比個人基準高 ≥ 個人門檻（4 點或 2 倍個人波動，取較大者） | +1 |
| 比目標體重多 ≥ 4 kg（安全底線）／3–4 kg | +2／+1 |
| 皮膚水分比基準高 ≥ 20%（需有其他指標同時有分） | +1 |
| 喘的程度 4–6 分（或比醫護設定的平常分數多 ≥ 2 分） | +2 |
| 喘的程度 ≥ 7 分 | 直接紅燈 |

綠燈 0–1 分、黃燈 2–3 分、紅燈 ≥ 4 分。前 6 次透析後量測為校正期，只用安全底線判讀。

<a name="references"></a>

## 主要參考文獻

- Caughey MC, et al. *BMC Nephrol.* 2025;26:373. doi:10.1186/s12882-025-04306-w
- Chen Y, et al. *Blood Purif.* 2025;54(8):483-496. PMID 40532691
- Amir O, et al. *Int J Cardiol.* 2016;221:841-6. PMID 27434357
- Uriel N, et al. *J Am Heart Assoc.* 2018;7:e009175. PMID 30571493
- Alvarez-Garcia J, et al. *JACC Heart Fail.* 2024;12(4):695-706. PMID 38430084
- Kalantar-Zadeh K, et al. *Circulation.* 2009;119(5):671-9. PMID 19171851
- Hecking M, et al. *Am J Nephrol.* 2013;38(1):78-90. PMID 23838386
- Fujioka H, et al. *J Cardiovasc Dev Dis.* 2022;9(2):57. PMID 35200710
- Hori M, et al. *Int Heart J.* 2022;63(1):73-76. PMID 35095079
- Izumida T, et al. *Int Heart J.* 2023;64(5):865-869. PMID 37778989
- Imamura T, et al. *J Clin Med.* 2023;12(13):4415. PMID 37445449
- Mayrovitz HN, et al. *Clin Physiol Funct Imaging.* 2020;40(2):76-82. PMID 31677329
- Mayrovitz HN. *Clin Physiol Funct Imaging.* 2025;45(1):e12916. PMID 39550685

數字取自文獻摘要。多數門檻來自心衰竭研究，用在透析病人的證據有限；個人化規則（校正期、2 倍標準差）屬於作業假設，需要實際資料驗證。

## Home Fluid Monitoring (Class Project Prototype)

This prototype helps people on hemodialysis track fluid status at home. Users enter two noninvasive measurements (lung fluid percentage, or %LW, from a ReDS vest and skin moisture from a MoistureMeter), along with their weight, blood pressure, and shortness-of-breath rating. The prototype applies scoring rules drawn from the literature, displays a green, yellow, or red status, and charts changes over time.

[Open the demo](https://tommy880422.github.io/dialysis-fluid-monitor/)

> This class project demonstrates a set of scoring rules and cannot replace clinical judgment. The demo includes sample data. Any data you enter stays in your browser.

### Features

- **Home** shows the current status, days since the last dialysis session, a reminder when the gap between sessions is long, and progress toward establishing a personal baseline.
- **Measurement wizard** guides users through seven steps, including a pre-measurement check with a 15-minute countdown if they are hot or sweating, weight, blood pressure and pulse, three skin moisture readings, a ReDS lung fluid reading, and a shortness-of-breath rating. It calculates the coefficient of variation (CV), a measure of how much the skin moisture readings vary, and prompts users to repeat them if the CV exceeds 10%.
- **Results** shows the status, suggestions, and the points assigned by each rule.
- **Trends** charts lung fluid, skin moisture, and weight, with dialysis days and personal baseline ranges marked.
- **History and scoring criteria** show past records and the rules, with PubMed links and an evidence rating for each rule.
- **Settings** includes patient-entered information, clinician settings (demo password `1234`), and an automatically calculated personal baseline.

### Scoring summary

| Condition | Points |
|---|---|
| Lung fluid (%LW) ≥ 35% (safety threshold) | +2 |
| Lung fluid (%LW) 26.5–34.9% | +1 |
| Lung fluid exceeds the personal baseline by at least the individual threshold (4 percentage points or twice the personal standard deviation, whichever is higher) | +1 |
| Weight is ≥ 4 kg above target (safety threshold) or 3–4 kg above target | +2 or +1, respectively |
| Skin moisture is ≥ 20% above baseline and at least one other indicator scores points | +1 |
| Shortness-of-breath rating is 4–6 or at least 2 points above the usual rating set by a clinician | +2 |
| Shortness-of-breath rating is ≥ 7 | Red status immediately |

Green corresponds to 0–1 points, yellow to 2–3 points, and red to 4 or more points. During calibration, the prototype uses only the safety thresholds for the first six post-dialysis measurements.

### References and limitations

Both versions use the same [reference list](#references). The numeric values come from published abstracts. Most thresholds come from heart failure studies, and evidence for their use in people on dialysis is limited. The personalized rules, including the calibration period and the use of twice the standard deviation, are class project assumptions that need validation with real data.
