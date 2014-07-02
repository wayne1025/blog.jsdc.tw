---
layout: post
title: 導入快速開發，打造出上等程式品質
author: smlsun
description: 快速開發，同時打造高品質程式，如何在這兩者間兼容且並行前進，都在本篇中一一介紹
image: https://fbcdn-sphotos-b-a.akamaihd.net/hphotos-ak-xpa1/t31.0-8/10498640_533783346727183_7443524669347072895_o.jpg
tags:
  - 專家介紹
  - 程式開發
tableOfContents:
  - text: 架構論壇
    link: #架構論壇
  - text: 程式開發
    link: #程式開發
---

## 內容大綱

程式語言何其多，確認程式的正確只有透過測試才能達到，在通往功能的正確與系統的穩定，需要從各種不同的測試來達到，無論是人肉測試或是自動測試。

在開發的過程中，除了撰寫程式，接著就是一連串的 try and Error，程式開發的速度，取決於驗證的速度，系統的穩定度取決關鍵程式碼的驗證。

透過撰寫測試程式來加速開發速度，不只是心理上的安全感，而是程式開發的快感！

追求程式碼的快、狠、準，從測試開始，透過持續整合將一連串加速的過程連綿不斷的輸出，成為頂級超跑不是夢想！

---

## 導讀介紹

如何快速開發程式！？寫出品質上等的程式?

撇去對開發語言的熟悉，屬於知識的範圍，更重要的是開發的觀念，程式開發要快最根本的是 coding 以及確認結果是否正確，關鍵就在於 test 的撰寫，就像當兵有一句話 「能坐就不站，能躺就不坐」，套在程式開發 「能 command 就不啟 server」，如果能透過 command 就確認程式正確，又何必啟動 server 實際到要測試的功能，多了好幾個步驟，如果不幸沒辦法一次到位，將會消耗 N 倍的時間。


所以從個人的角度，有測試的觀念利用撰寫 test 來加速開發循環，可惜，test 往往在專案緊急時最易被捨棄的，在專案緊急的狀況，又捨棄了最重要的驅動引擎，時間就在不停的開發確認程式正確的循環中消耗。

除此之外，在重覆的開發確認程式正確的過程中，因為沒有透過撰寫 test 來確認程式的正確，沒辦法累積測試足跡，進而在往後需要重構時作為確認程式正確的標準。

除了開發階段的工作，還有版本發佈的流程，就像前面所說的要能夠快速開發，關鍵在於每個循環是否夠快，發佈到測試機或是正式環境，長則半年短則一個禮拜或每天，節省時間最快的方式就是自動！完全不要開發人員介入，要做到自動就需要仰賴  CI 的幫忙。



程式的範圍一旦大到需要團隊一起開發，就不是單純個人的測試可以確保程式的健康，

從團隊的角度，透過 CI 不停的確認團隊開發的程式是否能夠正常運作，透過個人所完成的 test case，並且將每次編譯結果 deploy 到測試機，供測試人員進一步進行確認，

---

如何快速開發程式！？寫出品質上等的程式

持續整合，在實際的軟體開發中，被進度苦苦追趕的工程師們，往往不會想到要利用他來改善專案的穩定度

功能開發都來不急了，哪來的時間弄持續整合？

經驗不足的情況下，通常程式開發滿足需求就來不及了，哪來精神改善開發流程？

軟體開發通常不會是只有一個人的事，即使個人有極強的程式開發技巧，對於開發過程中總是能夠避開可能的問題，但實際的狀況是與你合作的 member 素質不一，通常一個 bug 發生不是對個人的管控與要求，而是需要提高到團隊的高度來進行，

CI 用比較傳統的程式建置流程來看，不外乎開發、編譯、測試、打包、發佈，這些環節，

![enter image description here][1]

就如同上圖一樣，軟體開發就是一直不停的重覆疊代從 開發、編譯、測試、打包、發佈這樣的過程，每次疊代所花的時間越少，專案開發的速度就有多快，就像引擎轉動一樣，轉動的越快，效率就越高

在沒有導入 ci 的團隊經歷了一段時間，期初在每個環節用人工的方式控管還可以過的去，一旦專案變大客製變多，需要疊代的次數一多，就不是單純用人力可以應付的，

尤其是多人開發的情形，即使有版本控管的幫忙，也沒辦法確保所有程式是最新的，就是有人以為程式已有上傳到版控主機，進行測試時發現明明程式人員回報程式有改，但測試人員就是發現錯誤一樣

或是測試已經正常，但發現發佈出去的程式又錯！？可能的原因有很多，人為疏失來講就是包版時利用檔案傳遞可能又傳到錯誤或是不是最新的程式碼

不知道大家是否遇到同樣的狀況？至少我遇到了！在專案時程的壓力，bug 永遠解不完的情況下，上面說的狀況


在開始一個專案時，先不要急著寫程式，應該要先把專案的部屬流程搞定，越早搞定在往後的開發越節省時間

接著搞定測試環境，如果你開發 java 就應該要有 junit 的運行所需 lib，若你是寫 node js 就應該使用類似 mocha 這樣的套件，開始學習一樣的新的語言時，不應該學寫語法，應該要先學會寫該語言特性的測試碼。

前陣子有過 TDD 的論戰，要注意的是：寫 test code 不等於 TDD，寫 test code 是加速開發的必要手段(認真)，不要說你寫完的 code 一定百分之百對，程式開發簡單來說也是 try and error 一直循環，一直到得到預期結果為止，如何驗證預期結果？

最菜的時候，或是有經驗但不習慣寫 test 就是將程式或 server 啟動，實際操作應用程式來確定運行結果是否正常，這過程中，會花的時間有幾個

1. server 啟動的時間
2. 啟動完成後，操作到要測試的頁面

如果程式修改結果確認幸運的一次完成，那倒還好，重覆幾次你就會想殺人，造成思緒不連貫就算了，讓費時間在等待，往往會消磨工作的熱情

程式開發有快有慢，其實就在於開發過程的跌代還有確認程式的正確與否的每次所花的時間累積起來的


程式開發的熟悉，除了程式語言特性的熟悉之外，還有另外一個面相，就是確認程式正確與否的速度與技巧，後者跟所寫語言無關，不管任何語言的觀念都一樣，如果該程式語言沒辦法透過測試來驗證程式是否正確，是否要學習就要三思了

寫測試還有一個好處，就是跟不同的程式開發人員進行合作時，透過測試碼的撰寫可以讓合作的團隊成員可以很清楚的知道該如何呼叫你所完成的功能，預期的輸入與輸出結果，從此，在也不用因為找不到人沒辦法確定該怎麼乎要該程式，有這樣的習慣，在開源的世界也是一個很重要的觀念，很多開源的 readme 沒有文件沒有很詳細，這時你就可以從 test code 下手，有時，test code 會比 readme 清楚，更完整的使用範例，來幫助使用者更快了解使用的情境與輸入與輸出結果

寫測試可以看成最微觀的測試，從測試過程的累積，自然而然就可以達到導入整合 ci。

---

除了學習還有更多架構及知識面，歡迎到[華山論劍開發者論壇](https://ticket.aotter.net/76)上，透過站在巨人的肩膀上，找到最適合自己的著力點，跟著大家一起討論。

###活動報名

 * [華山論劍，報名連結](https://ticket.aotter.net/76)


[The Joel Test][2]
[何謂Continuous Integration][3]


  [1]: https://lh6.googleusercontent.com/-kHmKj9EoO1E/U6Kyq0QI_aI/AAAAAAAAOZw/q4_tkI4DCxg/s0/continuous-integration-design-process.png "continuous-integration-design-process.png"
  [2]: http://www.joelonsoftware.com/articles/fog0000000043.html
  [3]: https://www.ptt.cc/bbs/Soft_Job/M.1390977011.A.FC1.html