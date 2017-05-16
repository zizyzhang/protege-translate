## 目錄

[TOC]

## 練習2：建立一個新的OWL專案

1. 打開Protege
2. 當「New Project」對話框出現時，從左側「Project Format」列表中，中選擇「OWL Files」，并點擊「New」

## 練習3：新建Pizza，PizzaTopping和PizzaBase類別

1. 點擊「Create subclass」按鈕如圖4.2，這個按鈕可以在選中的類別下新建一個子類別（在這個案例中我們希望新建一個owl:Thing的子類別）。
2. 使用類別層級圖下的「Class name widget」重命名新建的類別為Pizza并按下回車鍵。
3. 重複前面的步驟，新增PizzaTopping和PizzaBase類別，確認在點擊「Create subclass」之前要先選中owl:Thing，這樣才會新建為owl:Thing的子類別。

## 練習4：讓Pizza,PizzaTopping和PizzaBase彼此互斥

1. 在類別層級圖中選擇選中Pizza
2. 在「disjoint class widget」中點擊「Add siblings」。這會讓PizzaBase和PizzaTopping（Pizza的同輩類別）和Pizza類別互斥。

## 練習5：使用「Create Group of Classes」精靈創建PizzaBase的一組子類別ThinAndCrispyBase和DeepPanBase

1. 在類別層級圖中選中「PiaazaBase」
2. 在Protege的菜單欄下選擇「Wizards」菜單并找到「Create Group of Classes」.
3. 您會看到圖4.6顯示的視窗。由於我們先前選擇了PizzaBase類別，第一個單選按鈕顯示為在PizzaBase下創建一組類別。如果我們在打開子類別組創建精靈之前忘記了選擇PizzaBase類別，我們可以再這個樹狀圖中選擇它。
4. 在精靈視窗上點擊「Next」﹣如圖4.7。我們現在需要告訴精靈我們要創建的子類別。在大的文字輸入框中，填入我們要新建的子類別名稱：「ThinAndCrispyBase」并按下回車，再輸入「DeepPanBase」如圖4.7
5. 按下「Next」，精靈會檢查我們輸入的類別名稱是否符合先前提到的規範（字符不能含有空格等），同時也會檢查類別是否是唯一的（不能有兩個名字一樣的類別）。如果在類別名稱中有任何的錯誤，錯誤訊息會在這個頁面中顯示出來，同時也會提示我們如何改正。
6. 按下「Next」，并確認我們選擇了「Make all new classes disjoint」，這樣我們就不需要再用「互斥小部件」來讓子類別互斥，精靈會自動的讓子類別互斥。
7. 點擊「Next」會顯示注釋頁面，在這裡我們可以添加注釋。大部分的注釋可以記錄Ontology的編輯信息（如誰創建了它，什麼時候創建了它,校訂的時間等）基礎的OWL注釋屬性預設是可以選擇的，不過我們現在並不需要增加任何注釋，所以我們直接按「Finish」即可。

## 練習6：在PizzaTopping下創建一些子類別

1. 在類別層級圖中選擇「PizzaTopping」
2. 用OWL精靈增加PizzaTopping的子類別：MeatTopping,VegetableTopping,CheeseTopping和SeafoodTopping。確認這些子類別互斥。
3. 接下來，我們增加不同種類的肉類Topping，點擊「Create Group Of Classes」精靈，增加MeatTopping的子類別：SpicyBeefTopping, PepperoniTopping, SalamiTopping和HamTopping. 再重複一次，請確認這些類別彼此互斥。
4. 增加不同的蔬菜類Topping：TomatoTopiing,  OliveTopping, MushroomTopping, PeperTopping, OnionTopping和CaperTopping，接下來創建PepperTopping的子類別：RedPepperTopping, GreenPepperTopping和JlapenoPepperTopping，確認這些PepperTopping的子類別也彼此獨立。
5. 現在，我們增加一些起司的Topping，在CheeseTopping下，新建MozzarellaTopping和ParmezanTopping，並讓他們彼此互斥。
6. 最後增加海鮮類Topping：TunaTopping, AnchovyTopping和PrawnTopping.

## 練習7：新建一個叫hasIngredient的屬性

1. 選擇「Propterties」的標籤,選擇「Create Object Property」按鈕（如圖4.13）建立一個新的物件屬性。一個帶有默認名字的屬性會被建立。
2. 把這個屬性重命名為hasIngredient，如圖4.14

## 練習8：創建hasTopping和hasBase作為hasIngredient的子屬性

1. 為了讓hasTopping成為hasIngredient的子屬性，我們需要在屬性層級圖中右鍵點擊hasIngredient，如圖4.15所示
2. 選擇「Create subproperty」項目，一個新的物件屬性會被創建為hasIngredient屬性的子屬性。
3. 把新的屬性重命名為hasTopping。
4. 重複以上步驟建立hasBase屬性。

## 練習9：建立一些翻轉屬性

1. 使用「Properties」標籤下的「Create object property」按鈕，建立一個叫做isIngredietnOf的屬性（這個屬性會成為hasIngredient的翻轉屬性。
2. 按下「inverse property widget」下的「Assign existing property」按鈕如圖4.17,這會在選中的屬性下顯示一個對話框，選擇hasIngredient屬性，并按下「OK」，此時hasIngredient屬性應該顯示在了「Inverse Property」小部件下。在屬性層級圖中，我們也應該會看到hasIngredient和isIngredientOf屎彼此的翻轉屬性。
3. 選擇hasBase屬性。
4. 在「Inverse Property」小部件中點擊「Create new inverse property」按鈕。這會顯示一個包含了新建的屬性的對話框，利用這個對話框重命名新建的屬性為「isBaseOf」，并關閉這個對話框。可以看到現在isBaseOf屬性已經被建立為isIngredientOf屬性的子類別。這是因為hasBase是hasIngredient的子類別，而isIngredient是hasIngredient的翻轉類別。
5. 選擇hasTopping屬性。
6. 點擊「Create new inverse property」按鈕。使用屬性對話框重命名屬性為isToppingOf.我們可以看到isToppingOf已經成為了isIngredientOf的子類別。

## 練習10：讓hasIngredient屬性可傳遞

1. 在「Properties」標籤下選擇hasIngredient屬性。
2. 在「Property Characteristics」小部件中勾選「Transitive」。
3. 選擇isIngredientOf屬性，確保「transitive」也被勾選了

## 練習11：讓hasBase成為函數型的屬性

1. 選擇hasBase屬性
2. 在屬性角色面板中讓「Allows multiple values」標記為未選中狀態。

## 練習12：為hasTopping指定值域

1. 在屬性層級圖中選擇hasTopping屬性
2. 在「Range Widget」中點擊「Add named class」按鈕如圖4.25，此時會出現一個對話框讓您選擇類別。
3. 選擇PizzaTopping類別，并按下「Ok」。此時，PizzaTopping將會被顯示在值域的列表別中。

## 練習13：把Pizza指定為hasTopping的定義域

1. 在屬性層級圖中選擇hasTopping屬性
2. 在「Domain Widget」中選擇「Add named class」, 此時會出現一個對話框讓您選擇類別。
3. 選擇Pizza并按下「Ok」.此時，Pizza將會被顯示在定義域的列表別中。

## 練習14：為isToppingOf屬性指定值域和定義域

1. 選擇isToppingOf屬性
2. 就像之前的練習一樣，把PizzaTopping指定為isToppingOf的定義域。
3. 把isToppingOf的值域設定為Pizza.

## 練習15：設定hasBase以及它翻轉屬性(BaseOf)的值域和定義域

1. 選擇hasBase屬性
2. 設定hasBase屬性的定義域為Pizza
3. 設定hasBase屬性的值域為PizzaBase
4. 選擇isBaseOf屬性
5. 設定isBaseOf屬性的定義域為PizzaBase
6. 設定isBaseOf屬性的值域為Pizza

## 練習16：為Pizza類別增加一個限制條件，要求Pizza必須要含有PizzaBase

1. 從類別層級圖中選擇Pizza類別
2. 選擇「Conditional Widget」上的「NECESSARY」標題文字，如圖4.29。以建立一個「必要」條件
3. 選擇「Create restriction」按鈕（顯示為一個R），如圖4.29。此時會顯示一個「Create Restriction」對話框如圖4.30，我們可以用它來建立限制條件。
4. 接下題。

## 練習17：為Pizza類別增加一個限制條件，要求Pizza必須要含有PizzaBase（接上一練習）

1. 在對話框右邊選擇「someValuesFrom」按鈕，「someValuesFrom」是存在性限制條件的別名。
2. 在左邊屬性列表中選擇hasBase
3. 為了應用篩選條件為PizzaBase，您可以在篩選條件(Filter)中輸入PizzaBase，或者在表達式建立面板上點擊「Insert class」按鈕，如圖4.31，并從類別層級圖中選擇PizzaBase類別。
4. 按下「Ok」按鈕就可以建立限制條件并關閉對話框。如果操作正確的話，限制條件會顯示在「Condition Widget」中。如果操作中出現錯誤，錯誤訊息會顯示在表達式建立面板的下方，如果是這樣，您需要重新檢查限制條件、篩選條件、屬性是不是選擇正確。

## 練習18：建立Pizza的子類別NamedPizza，和NamedPizza的子類別MargheritaPizza

1. 在類別層級圖中選擇Pizza類別。
2. 選擇「Create subclass」按鈕，建立Pizza的子類別，并重命名為NamedPizza。
3. 建立NamedPizza的子類別：MargheritaPizza
4. 在注釋框內為MargheritaPizza加入注釋（注釋框在類別名稱小部件的下方）：A pizza that only has Mozarella and Tomatotoppings。為類別，屬性等增加注釋是一個很好的習慣。這樣可以與同事更好的溝通。

## 練習19：為MargheritaPizza類別建立一個存在性條件：通過指定hasTopping屬性讓MargheritaPizza至少會有一個MozzarellaTopping

1. 在類別層級圖中選中「MargheritaPizza」
2. 在「Conditions widget」上選擇「NECESSARY」標題文字
3. 在「Conditions widget」上點擊「Create restriction」按鈕。
4. 在出現的對話框中，選擇限制性條件的種類為「someValuesFrom」
5. 在屬性列表中選擇「hasTopping」
6. 在Filter中輸入MozzarellaTopping，當然您也可以點擊「insert class」來選擇MozzarellaTopping類別。
7. 按下「Ok」按鈕，來建立限制并關閉對話框，如果出現了任何錯誤，錯誤會被顯示在表達式建立面板下方。

## 練習20：為MargheritaPizza建立存在性限制條件，讓MargheritaPizza必須好有一個TomatoTopping。

1. 在類別層級圖中選擇「MargheritaPizza」。
2. 在「Conditions widget」上選擇「NECESSARY」標題文字
3. 在「Conditions widget」上點擊「Create restriction」按鈕。
4. 在出現的對話框中，選擇限制性條件的種類為「someValuesFrom」
5. 在屬性列表中選擇「hasTopping」
6. 在Filter中輸入TomotoTopping
7. 按下「Ok」按鈕，來建立限制并關閉對話框。




## 練習21：通過克隆并修改MargheritaPizza類別來建立AmericanaPizza類別

1. 在類別層級圖中右鍵點擊MargheritaPizza
2. 在彈出的菜單中選擇「Create clone」，這樣做會建立一個MargheritaPizza的拷貝，叫做MargheritaPizza_2。
3. 把MargheritaPizza_2重命名為AmericanaPizza
4. 確保AmericanaPizza是被選中的，然後我們點擊「NECESSARY」標題文字，為它新增必要性條件。
5. 點擊「Create restriction」按鈕，此時會出現建立限制條件的對話框。
6. 在對話框的右側面板中選擇「someValuesFrom」
7. 在左側面板選擇hasTopping屬性
8. 在「filter」中輸入PepperoniTopping（或者通過Insert class完成這一步）。
9. 點擊「OK」完成限制性條件的建立



## 練習22：建立AmericanHotPizza和SohoPizza類別

1. AmericanHotPizza和AmericanaPizza的唯一不同點是前者有JalapenoPeppers。所以我們可以克隆AmericanaPizza並且增加一個存在性限制條件，限制性即hasTopping屬性設定為JalapenoPepperTopping
2. 一個SohoPizza也幾乎和MargheriataPizza一樣，只是多了一些橄欖油和起司的topping，所以我們可以克隆MargheritaPizza，并增加兩個限制性條件，通過限制他們的hasTopping屬性分別為OliveTopping和ParmezanTopping。

## 練習23：建立NamedPizza的子類別，並讓他們彼此獨立

1. 選擇「MargheritaPizza」類別。
2. 在「Disjoints widget」中點擊「Add all siblings」按鈕，讓這些Pizza類別彼此獨立。

## 練習24：增加一個測試類別，名為ProbeInconsistentTopping，讓他同時是CheeseTopping和Vegetable的子類別。

1. 在類別層級圖中選擇CheeseTopping類別。
2. 為CheeseTopping增加一個叫ProbeInconsistentTopping的子類別
3. 在ProbeInconsistentTopping類別注釋中填寫「這個類別在Ontology推論后是有矛盾的」，這個注釋讓任何看到它的人可以發現我們是故意讓這個類別出錯的。
4. 確保ProbeInconsistentTopping被選中，並且我們在「Conditions widget」中點擊「NECESSARY」標題文字。
5. 點擊「Add named class」按鈕，選擇「VegetableTopping」并點擊「OK」，此時VegetableTopping會被添加為必要條件如圖4.44.

## 練習25：進行Ontology的推論，并確認ProbeInconsistentTopping是有矛盾的

1.  點擊OWL 工具欄的「Classify Taxonomy」按鈕

## 練習26：移除CheeseTopping和VegetableTopping類別的disjoint陳述，看看會發生什麼

1. 在類別層級圖中選擇CheeseTopping
2. 在「Disjoints wigdet」里面可以看到CheeseTopping的同辈类别，选择VegetableTopping。
3. 点击「Remove selected class from list」按鈕，如圖4.5, 移除CheeseTopping和MeatTopping的独立性。
4. 点击OWL工具欄中的「Classify Taxonomy」按鈕，等待結果產生。

## 練習27：讓CheeseTopping和Vegetable彼此獨立，來修復ontology

1. 選擇「CheeseTopping」類別。
2. 在「Disjoints widget」中可以看到MeatTopping和SeafoodTopping。
3. 點擊「Add disjoint class」按鈕，此時會彈出選擇類別的對話框，在這裡選擇VegetableTopping。
4. 再次按下「Classify Taxonomy」按鈕，我們可以看到PrebeInconsistentTopping高亮成紅色，顯示它在此變得有矛盾了。

## 練習28：建立Pizza的子類別CheesyPizza，并限制它至少有一種CheeseTopping

1. 在類別層級圖中選擇「Pizza」類別。
2. 點擊「Create subclass」按鈕來建立Pizza的子類別。重命名為「CheesyPizza」。
3. 確認CheesyPizza被選中。選擇「NECESSARY」標題文字，你必須在「Conditions Widgets」中勾選「Asserted」標籤（默認它選中了「Inferred」標籤）
4. 點擊「Create restriction」按鈕來建立規則。
5. 選擇右邊對話框的「someValuesFrom」
6. 選擇左邊屬性列表裡的hasTopping
7. 在filter文字框中輸入CheeseTopping（或者用Insert class來選擇），按下「OK」以完成規則建立

## 練習29：轉換CheesyPizza的必要規則為充分必要規則

1. 在類別層級圖中選中「CheesyPizza」。
2. 在「Conditions Widget」中選中「hasTopping CheeseTopping」限制
3. 把「hasTopping CheeseTopping」從「NECESSARY」標題下拖動到「NECESSARY ＆ SUFFICIENT」標題下。
4. 選中「Pizza」類別。
5. 把Pizza從「CENCESSARY」標題下拖動到「hasTopping CheeseTopping」上方。（注意：不是拖動到「NECESSARY ＆ SUFFICIENT」標題上方）

## 練習30：使用推論器自動計算CheesyPizza的子類別

1. 確保「RACER」推論器工作正常
2. 在工具欄點擊「Classify Taxonomy...」按鈕如圖4.42


## 練習31：建立一個類別來描述VegetarianPizza

1. 建立一個Pizza的子類別「VegetarianPizza」
2. 確認VegetarianPizza被選中，並點擊「NECESSARY」標題文字。
3. 點擊「Create restriction」按鈕來顯示建立規則的對話框。
4. 右侧面板点击「allValuesFrom」
5. 左侧面板点击hasTopping属性
6. 在「filter」中，我们要填写CheeseTopping或者VegetableTopping。因此，我们首先在「filter」中输入CheeseTopping或者用「insert class」按钮选择，然后再点击规则建立面板的「Insert unionOf」按钮来加入聯集规则，最后再输入VegetableTopping或在「Insert class button」中选择VegetableTopping。
7. 按下「OK按钮。」

## 練習32：把VegetarianPizza的必要規則轉換成充分必要規則

1. 確認「VegetarianPizza」被選中
2. 選擇限制了「hasTopping」屬性的那個規則。
3. 把這條規則從「NECESSARY」標題文字下拖拽到「NECESSARY&SUFFICIENT」標題文字上方
4. 選擇「Pizza」類別。
5. 把「Pizza」類別從「NECESSARY」標題文字拖拽到「hasTopping」上方（注意：這次不是拖到「NECESSARY&SUFFICIENT」上方）

## 練習33：使用推論器來分類ontology

1. 確保「Racer」推論器在運行中，此時點擊「Classify taxonomy」按鈕。



## 練習34：為MargheritaPizza類別增加一個限制了閉包公理的hasTopping屬性。

1. 在類別層級圖中選擇「MargheritaPizza」
2. 點擊「NECESSARY」標題文字
3. 點擊「Create restriction」按鈕來打開規則建立對話框。
4. 右側面板選擇「allValuesFrom」
5. 左側面板選擇hasTopping屬性
6. 在「filter」中輸入「MozzarellaTopping or TomatoTopping」（or會直接轉換成聯集的符號），或者如練習32按下「Insert unionOf」來增加這個篩選條件。
7. 按下「OK」按鈕

## 練習35：為SohoPizza增加一個限制了閉包公理的 hasTopping屬性

1. 在類別層級圖中選擇「SohoPizza」
2. 選擇「NECESSARY」標題文字
3. 按下「Create restriction」按鈕來顯示建立規則的對話框。
4. 右側規則選「allValuesFrom」
5. 左側面板選擇「hasTopping」屬性。
6. 然後在filter中輸入「ParmezanTopping or MozzarellaTopping or TomatoTopping or OliveTopping」。
7. 按下「OK」按鈕。


## 練習36：為AmericanaPizza自動建立一個限制了閉包公理的 hasTopping屬性

1. 在類別層級圖中選擇「AmericanaPizza」
2. 在「Condition Widgets」右鍵點擊一條hasTopping規則，在彈出的菜單中選擇「Add closure axiom」，一個包含hasTopping的閉包公理就會自動創建。

## 練習37：為AmericanHotPizza自動建立一個限制了閉包公理的 hasTopping屬性

1. 在類別層級圖中選擇「AmericanHotPizza」
2. 在「Condition Widgets」右鍵點擊一條hasTopping規則，在彈出的菜單中選擇「Add closure axiom」，一個包含hasTopping的閉包公理就會自動創建。

## 練習38：使用推論器推論Ontology

1. 選擇「Classify taxonomy」按鈕來激活推論器。



## 練習39：建立一個「ValuePartition」來代表一個Pizza的辣度

1. 在「Wizards」菜單欄中選擇「Create Value Partition」，激活「ValuePartition」精靈。


2. 在精靈的第一個頁面中在把 「SpicinessValuePartition」作為「ValuePartition」的名字。然後按下「Next」。
3. 輸入「hasValuePartition」作為「ValuePartition」的屬性。然後按下「Next」
4. 我們現在需要指定值的類型。在文字輸入區域輸入「Mild」然後按下「Return」鍵，輸入「Medium」按下「Return」鍵，輸入「Hot」然後按下「Return」。這會為「SpicinessValuePartition」創建三個子類別。按下「Next」。
5. 「ValuePartition」的名字會被驗證，然後按下「Next」.
6. 此時會出現注釋頁面，如果你願意的話可以為這個「ValuePartition」加入注釋，這次我們就先不加，直接按下「Next」。
7. 精靈的最後一頁需要我們為這些值指定一個「root」，在這裡推薦大家把這些值都創建在「ValuePartition」這個類別下，也就是默認的選項。按下「Finish」按鈕。

## 練習40:使用屬性矩陣精靈來指定pizza topping的辣度

1. 在「Wizards」菜單中選擇「Properties Matrix」項目。
2. 屬性矩陣精靈的最初的頁面如圖4.63可以進行類別選擇。我們可以用頁面底部中間的按鈕來左右轉移類別。選擇所有的Pizza Topping 類別，把他們轉移到右邊如圖4.63，
3. 此时应该会如图4.74。选择「hasSpiciness」属性，并用「>>」按钮移到右侧栏按下「Next」
4. 最后一个页面我们要指定属性的筛选条件。我们双击每一个类别，并且给他们指定筛选条件。Mild筛选条件会指定给所有类别除了PepperoniTopping、SalamiTopping（这两个类别的筛选条件是「medium」）、JalapenoPepperTopping和SpicyBeef(这两个类别的筛选条件是Hot)。此时精灵会長得像圖4.65.
5. 按下「Finish」按鈕建立規則。我們可以看到所有topping類別現在都有了hasSciciness屬性的應用了SpicinessValuePartition的子類別的限制條件

## 練習41：創建Pizza的子類別SpicyPizza

1. 創建一個名為SpicyPizza的Pizza的子類別。
2. 在類層次結構中選擇SpicyPizza，在條件窗口小部件中選擇「NECESSARY＆SUFFICIENT」標題你文字。


3. 按條件窗口小部件上的「Create restriction」按鈕顯示創建限制對話框。
4. 選擇“∃someValuesFrom”作為限制類型。
5. 選擇hasTopping作為要限制的屬性。
6. 「filter」填寫的應該是：「PizzaTopping⊓∃ hasSpiciness Hot」。這個填充描述了一個匿名類，它包含作為類PizzaTopping的以及Hot的成員。換句話說，PizzaToppings的的辣度是Hot。在 「filter」 中 輸入「PizzaTopping and some hasSpiciness Hot」。 「and」關鍵字將被轉換為交叉符號⊓，“some”關鍵字將被轉換為存在符號∃。
7. 創建限制對話框應該類似於圖4.67所示。按OK按鈕關閉對話框並創建限制。
8. 最後，將Pizza從「NECESSARY」標題文字下拖到新創建的限制之上（∃hasTopping（PizzaTopping⊓∃hasSpiciness Hot））。

## 練習42：使用推論器推論Ontology

1. 選擇「Classify taxonomy」按鈕來激活推論器。

## 練習43：創建一個至少有三個澆頭的InterestingPizza類別

1. 切換到OWLClasses選項卡，確保選擇了Pizza類。
2. 創建一個名為InterestingPizza的Pizza的子類別。
3. 在條件窗口小部件中選擇「NECESSARY＆SUFFICIENT」標題。
4. 按「Create restriction」，彈出創建限制對話框。
5. 選擇「≥minCardinality」作為要創建的限制類型。
6. 選擇「hasTopping」作為要限制的屬性。
7. 通過在「filter」編輯框中鍵入3來指定最小基數為3。
8. 按「確定」按鈕關閉對話框並創建限制。
9. 條件窗口小部件現在應該具有Pizza的「必需」條件，並且充分必要的條件為hasTopping≥3。我們需要使「Pizza」成為必要和充分條件的一部分。 拖拉Pizza，放在hasTopping≥3的條件之上。

## 練習44：使用推論器推論Ontology

1. 選擇「Classify taxonomy」按鈕來激活推論器。

## 練習45：創建NonVegetarianPizza作為Pizza的子類，並使其與Vegetarian-Pizza獨立

1. 在「OWLClasses」選項卡上的類層次結構中選擇Pizza。創建一個新類作為Pizza的子類。
2. 將新類別重新命名為「NonVegetarianPizza」。
3. 使NonVegetarianPizza與VegetarianPizza獨立 - 選擇NonVegetarianPizza后，按下「disjoint classes widget」上的「Add named class」按鈕（圖4.5）。


## 練習46：使「VegetarianPizza」成為「VegetarianPizza」的補充

1. 確保在「OWLClasses」選項卡上的類層次圖中選擇了「NonVegetarianPizza」。
2. 在條件窗口小部件中選擇「NECESSARY＆SUFFICIENT」標題。
3. 按創建新表達式按鈕，將彈出內聯表達式編輯器，如圖5.1所示。內聯表達式編輯器包含用於鍵入表達式的編輯框和表達式生成器面板（與「創建限制對話框」中相同），可用於將類名和邏輯符號插入到編輯框中。
4. 在編輯框中輸入「not VegetarianPizza」。 「not」關鍵字將被轉換為符號「¬」。如果要使用表達式生成器面板輸入表達式，請使用圖5.3所示的「Insert complementOf」按鈕插入「complementOf」符號，並使用「insert class」按鈕（圖5.3）輸入「VegetarianPizza」.
5. 按回車鍵，創建並分配表達式。如果所有內容都輸入正確，則內聯表達式編輯器將關閉，且表達式將被創建。 （如果有錯誤，請檢查「VegetarianPizza」的拼寫）。

## 練習47：為NonVegetarianPizza添加充分必要條件「Pizza」

1. 確保在「OWLClases」中的類層次結構中選擇了NonVegetarianPizza標籤。
2. 在條件窗口小部件中選擇「Pizza」。
3. 將Pizza從「NECESSARY」標題下拉到「¬VegetaianPizza」條件上，讓它和「NonVegetarianPizza」成為同一組。

## 練習48：使用推論器來分類ontology

1. 確保「Racer」推論器在運行中，此時點擊「Classify taxonomy」按鈕。

## 練習49：創建一個「NamedPizza」的子類讓它含有一種Mozzarella Topping

1. 創建名為「UnclosedPizza」的「NamedPizza」子類。
2. 確保在條件窗口小部件中選擇了「UnclosedPizza」，選擇「NECESSARY」標題。
3. 按創建限制按鈕顯示創建限制對話框。
4. 選擇「∃someValuesFrom」創建一個存在限制。
5. 選擇hasTopping作為要限制的屬性。
6. 在「 filter」中輸入Mozzarella，指定澆頭必須是MozzarellaTopping類成員的實例。
7. 按「確定」按鈕關閉對話框並創建限制。

## 練習50：使用推論器來分類ontology

1. 選擇「Classify taxonomy」按鈕來激活推論器。




## 練習51：創建一個名為「Country」的类别，並加入一些实例

1. 創建「Country」作為Thing类别的子類。
2. 切換到圖6.1所示的「Individuals」選項卡，然後在类别树状图中選擇「Country」
3. 按「Create Instance」按鈕創建實例，如圖6.2所示。 （記住「Instance」是本體術語中「Individual」的另一個名稱）。
4. 一个Country的成員将会自动生成。 使用「Name」小部件（位於類視圖和實例列表右側的「individuals」選項卡）重命名实例為「Italy」。
5. 使用上述步驟，創造一些更多實例：America，England，France和Germany。這些實例是「Country」類別的成員。



## 練習52：創建一個hasValue限制，指定MozzarellaTopping的起源為「Italy」

1. 切換到「Properties」選項卡。 創建一個新的對象屬性並將其命名為hasCountryOfOrigin。
2. 切換到「OWLClasses」選項卡並選擇MozzarellaTopping類。
3. 在條件窗口小部件中選擇「NECESSARY」標題。
4. 按條件窗口小部件上的創建限制按鈕，彈出創建限制對話框。
5. 選擇「∋hasValue」作為要創建的限制類型。
6. 選擇「hasCountryOfOrigin」作為要限制的屬性。
7. 在「filter」中，輸入「Italy」。或者按下表達式構建器面板上的「Insert idividual」按鈕，彈出對話框選中「Italy」。
8. 按「OK」關閉對話框並創建限制。



## 練習53：將類Country轉換為枚舉類

1. 切換「OWLClasses」選項卡，然後選擇「Country」。
2. 在條件窗口小部件中選擇「NECESSARY＆SUFFICIENT」標題。
3. 按創建新表達式按鈕，此時可以看到內聯表達式編輯器彈出。
4. 在表達式編輯框中輸入{America England France Germany Italy}（請注意要用圓括號括起內容）。 鍵入實例的前幾個字母，然後按Tab鍵可以進行自動補全。
5. 按「return」鍵確認並關閉表達式編輯器。



## 練習54：創建一個類來定義三角形，使用多組必要和充分的條件

1. 創建一個Thing的子類：命名為Polygon。
2. 創建名為Triangle的Polygon子類。
3. 創建一個名為hasSide的對象屬性。
4. 創建一個名為hasAngle的對象屬性。
5. 在「OWLClasses」選項卡上，選擇「Triangle」類。在條件窗口小部件中選擇「NECESSARY＆SUFFICIENT」標題。按條件窗口小部件上的創建限制按鈕顯示創建限制對話框。
6. 選擇「= cardinality」作為要創建的限制類型。選擇hasSide作為限制的屬性。在filter中輸入3。按「確定」關閉對話框並創建限制
7. 再次在條件窗口小部件中選擇「NECESSARY＆SUFFICIENT」標題。按創建限制按鈕顯示創建限制對話框。
8. 選擇「= cardinality」作為要創建的限制類型。選擇hasAngle作為限制的屬性。在filter中輸入3。按「確定」關閉對話框並創建限制。
9. 從「NECESSARY」標題下拖動「Polygon」，並將其放在hasSide = 3限制上方。
10. 選擇「hasAngle = 3」 那條限制。單擊「Add named class...」按鈕來顯示包含類層次結構的對話框。選擇「Polygon」類，然後單擊「Ok」按鈕關閉對話框。

## 練習55：創建命名空間和前綴以引用Wine Ontology的類，屬性和個人

1. 按圖7.1所示的「Namespace prefix」小部件上的「Add prefix」按鈕，創建一個新的命名空間。 將創建一個新的命名空間「http://www.domain2.com#」，其前綴為p1。
2. 雙擊前綴p1進行編輯。 將其更改為vin，它是葡萄酒本體中使用的命名空間前綴。
3. 雙擊命名空間「http://www.domain2.com#」進行編輯。 將其更改為「http://www.w3.org/TR/2004/REC-owl-guide-20040210/wine#」。 如果命名空間沒有正確輸入，即如果命名空間不是有效的URI，並且它不以'/'或'＃'為結束，OWL將拒絕該條目并回復到原來的值。
4. 我們現在可以參照葡萄酒本體中的概念，並在葡萄酒本體命名空間中創建類和屬性。 例如創建一個新的對象屬性並將其命名為「vin:myWineProperty」。

## 練習56：將「koala」本體導入本體論

1. 切換到「Metadata」選項卡。
2. 按下位於「Namespace prefix」窗口小部件上的「Add prefix」按鈕。 一個新的命名空間和命名空間前綴將被創建。
3. 編輯命名空間前綴，將其改為「koala」。
4. 我們現在需要指定命名空間。 當導入本體時，命名空間應該是本體所在的實際URL，後跟'/'或'＃'。 編輯「koala」前綴的命名空間，將其更改為「http://protege.stanford.edu/plugins/owl/owl-library/koala.owl#」。
5. 現在勾選位於與「koala」前綴和命名空間同一行的「Imort tick box」。 您將看到一個對話框，表明修改只會在在保存并重新加載文件生后效。 單擊對話框上的「Yes」按鈕。 如果您尚未保存項目，將顯示保存對話框。



## 練習57：指定導入的本體的替代位置

1. 在「Namespace Prefixes」窗口小部件中選擇相關的本體。
2. 按下圖7.1所示的「Namespace Prefixes」小部件上的「Add to ont-policy file」按鈕。 這將打開圖7.2所示的本體策略文件對話框。
3. 從圖7.2可以看出，「koala」本體將被添加到策略中（最後一行）。 要指定替代位置，雙擊koala本體行上的「Alternative URI」框，在這裡可以輸入有效的URI。 按「OK」關閉對話框。

## 練習58：導入Dublin核心元數據元素本體

1. 從OWL菜單中選擇「Dublin Core metadata」。
2. 此時將出現一個對話框。 勾選對話框上的勾選框，導入本體。
3. 此時將顯示一條消息，表明Protege-OWL需要重新加載本體。 按「YES」按鈕。
4. 幾分鐘之後，Dublin核心元數據本體將被導入。 按下「Close」按鈕關閉「Dublin核心元數據」對話框。
5. 切換到「Properties」選項卡。 如圖7.3所示，可以看到已經導入了很多註釋屬性（表示Dublin核心元數據關鍵字）。 這些註釋屬性可以以標準方式使用（如第6.4節）。



## 練習59：導入Prote ge-OWL元數據本體

1. 從OWL菜單中選擇「Preferences」項目，將顯示如圖4.41所示的首選項對話框。
2. 勾選「Import protege metadata ontology」勾選框。 您將看到一個「Confirm Reload」對話框，要求您重新加載本體，以使更改生效。 按「Yes」按鈕。

## 英文注釋

- ###### ingredient  配料

- ###### disjoint  互斥

- ###### Propterties  屬性

- ###### inverse 反转，相反

- ###### functional property  函數型的屬性

- ###### range  值域

- ###### domain  定義域

- ###### filter  篩選器

- ###### taxonomy  分類



