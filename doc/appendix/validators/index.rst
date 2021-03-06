校驗（轉換）器說明
==================

CKAN 具有校驗器（validator）機制，用以檢查欄位是否符合規定，故亦可視為值域。另有轉換器（converter），用以轉換欄位值俾符合規定。

.. _internal_validators:

------------------
內建校驗（轉換）器
------------------

.. automodule:: ckanext.data_depositario.validators
   :members:
   :undoc-members:

.. automodule:: ckanext.data_depositario.converters
   :members:
   :undoc-members:

.. _external_validators:

------------------------------
外部校驗（轉換）器（僅供參考）
------------------------------

if_empty_same_as(name)
  若空值則參照「網址」欄位

unicode
  必須是 unicode 字元

not_empty
  不能為空值

package_name_validator
  不得重複、長度需介於 2 至 100 字元（包含 2 與 100）

scheming_required
  若欄位為必填則不能為空值（套用 not_empty），反之則接受空值（套用 ignore_missing）

scheming_choices
  必須是空值或給定候選項之一

ignore_missing
  若欄位為空值，接受該空值並忽略位於其後之所有校驗器（若欄位非空值，則其後之所有校驗器仍有效）

tag_string_convert
  標籤長度須介於 1 至 100 字元（包含 1 與 100）、標籤須為 unicode 文數字或「-」、「_」與「.」符號

ignore_empty
  接受空值

wikidata_keyword
  （經 API 上傳資料集時）只接受以 Python list 格式（如 ``["Q1", "Q2"]`` ）或字串形式（如 ``"Q1, Q2"`` ）呈現之資料

scheming_multiple_choice
  （經 API 上傳資料集時）只接受以 Python list 格式（如 ``["Q1", "Q2"]`` ）或字串形式（如 ``"Q1, Q2"`` ）呈現之資料。資料值需為給定候選項中之一至多個

is_positive_integer
  必須是正整數

owner_org_validator
  必須為無指定專案或指定一個已存在之專案

email_validator
  必須符合 `電子郵件格式 <https://html.spec.whatwg.org/#e-mail-state-(type=email)>`_

remove_whitespace
  去除文字首尾空白

if_empty_guess_format
  若欄位為空值，嘗試猜測檔案格式

clean_format
  將檔案格式轉為小寫

----------------------------
後設資料使用之校驗（轉換）器
----------------------------

^^^^^^^^^^
資料集層級
^^^^^^^^^^

.. note::

   *選填欄位基本校驗器*：:ref:`ignore_missing <external_validators>` :ref:`unicode <external_validators>`

   *必填欄位基本校驗器*：:ref:`not_empty <external_validators>` :ref:`unicode <external_validators>`

""""""""
基本資訊
""""""""

.. include:: basic_information_validators.rst

""""""""
時空資訊
""""""""

.. include:: spatio_temporal_information_validators.rst

""""""""
管理資訊
""""""""

.. include:: management_information_validators.rst

^^^^^^^^
資源層級
^^^^^^^^

.. include:: resource_validators.rst
