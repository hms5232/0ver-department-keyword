# 0ver-department-keyword
0verKeyword of department search segmentation

## 介紹
因為系所關鍵字統計雖然依照經驗來搜尋不會差太多，但依照經驗總有點亂槍打鳥的感覺，深怕不小心遺漏掉重要趨勢。因此寫了一個簡易分詞小工具，至少在搜尋上有個依據。

## 需求
1. Python 3.7（分詞套件的官方是說 3.6 以上，但[由於相依套件的關係，目前最高只能至 3.7](https://github.com/ckiplab/ckiptagger/issues/28)）
2. pip3 & pipenv（幫你搞定一切）

## 環境
1. 沒有 pipenv 或 pip3 的話請先安裝這兩個：`sudo apt install python3-pip && pip3 install pipenv`（Windows 的 Python 3.4 以上已經內建 pip）
1. `pipenv install` 安裝所有需要的套件
    - 如果系統中有兩個以上的 Python 版本，請加上 `--python 3.7` 參數
    - 若過程中發現程式仍使用其他版本導致無法創建虛擬環境，請加上 `--deploy` 參數

## 使用
1. 將整理好的關鍵字 **csv** 檔案（**只有一行，一列一個關鍵字紀錄**）放進資料夾
4. 執行 `pipenv run python3 keyword.py`
5. 程式會產出 3 個 csv：
    | csv 檔案名稱 | 說明 |
    | ----------- | --- |
    | origin_ws.csv | 每列都是一個原本的關鍵字分詞後的結果 |
    | all_ws.csv | 將每個拆分出來的分詞結果通通放在第一行 |
    | count_keyword.csv | 計算分詞後每一個獨特關鍵字出現的次數 |

## LICENSE
[GNU General Public License v3.0](https://github.com/hms5232/0ver-department-keyword/blob/master/LICENSE)
