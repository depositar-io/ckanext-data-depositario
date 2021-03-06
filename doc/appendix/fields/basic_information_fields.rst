.. list-table::
   :widths: 15 5 55 25
   :header-rows: 1

   * - 名稱
     - 必填
     - 說明
     - 資料範圍

   * - 標題
     - 否
     - 建議以簡單扼要的方式描述，如「台灣各縣市之人口密度」較「人口統計圖表」來的具識別性。
     - 必須是 unicode 字元。若此欄位為空值，則參照「網址」欄位。

   * - 網址
     - 是
     - 網址為本平台上資料集唯一的識別碼，僅能為英數字及部分符號。網址會在您輸入資料集標題時自動產生。若標題內含有英數字（及部分符號），則產生之網址為該英數字（同時去除所有非英數字之文字）；若標題不含英數字，則系統會為您產生一組隨機英數字。您可隨時修改自動產生之網址。
     - 不能為空值。必須是 unicode 字元。不得與其他資料集網址重複，且長度需介於 2 至 100 字元（包含 2 與 100）。

   * - 摘要
     - 否
     - 記錄關於此資料集的細節內容，或是任何其他使用者可以進一步了解此資料集的資訊。
     - Markdown 欄位。

   * - 資料類型
     - 是
     - 資料集所屬之類型。
     - 接受多值。依據 :ref:`parse-insight-content-types`。

   * - Wikidata 關鍵字
     - 否
     - 搜尋 Wikidata（維基資料）項目選取關鍵字以描述資料集。如圖所示 [#]_。只用於您專案或資料集的標記（如：計畫編號），請填寫於「標籤」欄位。瀏覽時會根據網站語系設定顯示對應之翻譯。
     - 接受多值。

   * - 標籤
     - 否
     - 標籤欄位可協助使用者更容易找到該筆資料集，例如您可加上「人口」、「犯罪」等標籤。此欄位只用於您專案或資料集的標記。
     - 接受多值。長度須介於 1 至 100 字元（包含 1 與 100）、須為 unicode 文數字或「-」、「_」與「.」符號。

   * - 語言
     - 否
     - 本項目說明資料集內容所使用之語言，如歷史文獻可能為華語、日語、西班牙語系等。選項將先列出主要語言（依據維基百科：`World language`_ 條目），再依照 ISO 639-3 語言編碼字母排序列出。語言名稱翻譯取自 debian iso-codes_ 專案。
     - 接受多值。限使用 ISO 639-3 語言編碼。

   * - 備註
     - 否
     - 描述資料集的額外資訊。
     - Markdown 欄位。

.. [#] .. image:: /images/keyword_wikidata.png
.. _World language: https://en.wikipedia.org/wiki/World_language#Living_world_languages
.. _iso-codes: https://hosted.weblate.org/projects/iso-codes/
