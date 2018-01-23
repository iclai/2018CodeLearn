## html -流覽器溢出...如何確保跨流覽器，跨平臺測試和相容性

### 你如何決定何時或將會放棄對流覽器版本的支持？

看看流覽器使用的統計資料。有很多資源，如[statcounter](http://www.w3counter.com/globalstats.php)，[w3counter](http://www.w3counter.com/globalstats.php)，[w3cschools](http://www.w3schools.com/browsers/browsers_stats.asp)，或[WiKi](http://en.wikipedia.org/wiki/Usage_share_of_web_browsers)。如果可能的話，在您的頁面上添加一個分析跟蹤器，您將獲得關於訪問者訪問該網站所使用的設備，平臺，流覽器和版本的資料。

在開發過程中你做什麼事情來減少流覽器更新出現代碼中斷的可能性？

關鍵是要根據現有的標準使用明確的方法。繼續閱讀個人建議。

工作流程，以減輕交叉流覽

第1步：引導

起初決定：[優雅降級與漸進增強](http://www.w3.org/wiki/Graceful_degredation_versus_progressive_enhancement)。兩者都是有效的技術，但使用第一個修復現有項目是有意義的，第二個是新創建的項目。

然後選擇庫以[避免輸入現有代碼](http://en.wikipedia.org/wiki/Don't_repeat_yourself)，重點關注三種語言：JavaScript，CSS和HTML。HTML5（+ CSS3）今天是更好的選擇，但必須提供對舊版流覽器的支援。以下庫緩解支持他們：

* [modernizr](http://modernizr.com/)用於js或css的特徵檢測和條件載入。
* [jQuery](http://jquery.com/)的Ajax和DOM相關的任務。
* [normalize.css](http://necolas.github.io/normalize.css/)
  用於標準化預設的流覽器樣式，而不僅僅是“重置”它們。

**請注意，上面列出的所有js庫允許自訂構建**，這是性能問題時的重要內容。

[Html5 Boilerplate](http://html5boilerplate.com/)提供了一個強大的範本，從中開始佈局。它包括modernizr，jQuery和normalize.css。[它的github存儲庫](https://github.com/h5bp/html5-boilerplate)是瞭解關於跨流覽技術的很好的資源。[這個wiki](https://github.com/h5bp/html5-boilerplate/wiki/library)上的[文章](https://github.com/h5bp/html5-boilerplate/wiki/library)有一個很好的連結開始學習。

第二步：做好工作

設計應該是移動優先的，並且是回應式的。[這篇關於html5rocks的文章](http://www.html5rocks.com/en/mobile/responsivedesign/)介紹了為什麼以及如何。

在做“工作”的同時：

* 遵循[w3c標準](http://www.w3.org/standards/)。盡可能避免使用hack，特別是CSS hack。經常檢查[HTML5規範，](http://www.w3.org/TR/html51/single-page.html)因為它非常不穩定。
* 編寫javascript時請注意[ECMAScript 5的](http://www.ecmascript.org/)功能。依靠庫來避免由於流覽器實現不足導致的代碼中斷。[不要擴展DOM](http://perfectionkills.com/whats-wrong-with-extending-the-dom/)。
* 盡可能[自動化測試](http://en.wikipedia.org/wiki/Test_automation)。佈局和特殊佈局的拋光，包括動畫，[手動測試，](http://en.wikipedia.org/wiki/Manual_testing)因為它更快，但UI功能，如形式submision可以完美地測試與自動化測試。
* 使用工具來緩解任務。**Chrome + devtools**或者**Firefox + firebug**是非常基本的必須使用，但是有一些工具可以簡化跨流覽測試，甚至可以自動執行這些測試。

### 跨流覽器測試

* [**Browserstack**](http://www.browserstack.com/)。允許在所有設備，平臺，流覽器和版本上進行測試。
* [**Browserling**](https://browserling.com/)是流覽器的替代品。它由Peter. Krumins和James Halliday[開發和維護](https://browserling.com/)，他們都是[node.js社區的](http://nodeguide.com/community.html)知名成員，也是知名的開發人員。他們還發佈了一個工具來自動化稱為 [**testling-ci**](https://ci.testling.com/) 的過程，但是這只與在後端使用node.js有關。
* [**modern.ie**](http://www.modern.ie/)提供工具來緩解Internet Explorer上的測試。
  該網站由微軟開發，通過預先安裝的軟體通過流覽器和可下載的虛擬機器鏡像進行即時測試。

適應性測試“響應式設計”

* [**respon.si**](http://respon.si/) 是一個線上工具，旨在測試佈局的外觀。它允許選擇一個解析度，這對於響應式佈局測試非常有用。請注意，任何其他選擇解析度的工具都可以輕鬆完成相同的工作。

**測試新流覽器時有什麼建議？**

作為我們[完成定義的](http://www.scrum.org/Resources/Scrum-Glossary/Definition-of-Done)一部分，我們支持以下桌面流覽器：

* IE8 +
* Firefox 3.6
* Firefox（最新）
* Chrome（最新）
* Safari 6

Firefox / Chrome的最新版本的支援是好的，因為它們都提供了自動更新，所以如果任何人在老版本的流覽器上遇到問題，它就不在我們的手中，應該更新。

大多數的Firefox / Chrome測試都可以在我們的機器上完成，但是不同的作業系統如何處理字體，以及一些本機形式的元素，可能會或可能不會傳遞到Windows上的版本，顯然是不一致的。

要在OS X上測試Firefox版本，請使用我創建的“[安裝所有Firefox](https://github.com/omgmog/install-all-firefox)”腳本，以允許我並行運行多個版本的Firefox。

我們的開發團隊使用Ubuntu和Mac OS作為他們的環境，所以我們有一個專用的機器，每個版本的IE和Windows上的Chrome / Firefox以及OS X上的Safari 6都有虛擬機器。

這些虛擬機器使用[modern.ie](http://modern.ie/)提供的圖像進行設置。我們正在使用虛擬機器遠端存取機器，以便我們不需要中斷我們的工作流程並轉到另一台機器上。

**在開發過程中你做什麼事情來減少流覽器更新出現代碼中斷的可能性？**

顯而易見的事情是避免CSS hacks，並確保所編寫的HTML / CSS / JavaScript符合我們的代碼標準和我們的完成定義。

如果我們使用實驗CSS功能，我們確保我們提供了供應商首碼和最後w3定義的屬性：

`-moz-foo: bar;`

`-ms-foo: bar;`

`-o-foo: bar;`

`-webkit-foo: bar;`

`foo: bar;`

顯然，這引入了一些技術債務，但是如果您使用的是CSS的前置處理器，則可以減少這種開銷。

我們為IE保留一個單獨的樣式表，並使用條件注釋載入它，這樣我們可以修復IE中的問題，而不影響其他流覽器前端其餘部分的完整性。最近有一個動作，將其轉移到一個shame.css雖然，你可以在這裡閱讀：[http](http://csswizardry.com/2013/04/shame-css/):shame.css

**而且，您如何決定何時或將會放棄對流覽器版本的支持？**

Google分析。在Google Analytics中按流覽器類型細分非常有用。當特定流覽器的使用率下降到10％以下時，現在是停止開發新功能的好時機。

你可以做一些激進的事情，就像扔掉流覽器的所有駭客/風格一樣，但為了更平滑的過渡（並鼓勵人們升級），最好是停止為舊流覽器開發，也許有條件地顯示消息。

我們最近放棄了對IE7的支持，現在使用IE7的訪問者會收到一條消息告訴他們升級，他們沒有得到任何更多的修復或附加功能。

移動是一個完整的其他水壺，如果你的網站是完全回應這是一個額外的痛苦層。

我們有許多不同尺寸/版本的Android設備，一些舊的iPhone和iPad在我們用來測試大多數移動流覽器的辦公室裡踢。

顯然，螢幕尺寸，DPI，流覽器版本等方面都存在差異。在這方面你可以做的最好的是迎合最常見的情況，並解決任何問題。



