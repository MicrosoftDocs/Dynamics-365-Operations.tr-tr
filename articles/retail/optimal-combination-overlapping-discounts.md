<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="optimal-combination-overlapping-discounts.md" target-language="tr-TR">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>optimal-combination-overlapping-discounts.e4f3cd.e327f652855f898e50f1dd853ae20f3a0ff41d9e.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>e327f652855f898e50f1dd853ae20f3a0ff41d9e</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\optimal-combination-overlapping-discounts.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Çakışan iskontoları için en uygun birleşimi belirleme</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İskontolar çakıştığında, en düşük hareket toplamını veya en yüksek toplam iskontoyu oluşturacak çakışan iskonto birleşimi belirlemeniz gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common 'Buy 1, get 1 X percent off' (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yaygın olarak kullanılan '1 satın al, 1 al X yüzdesi' (BOGO) perakende iskontosunda olduğu gibi, iskonto tutarı satın alınan ürünlerin fiyatına göre değişiklik gösterdiğinde, bu işlem birleşimsel iyileştirme konusu durumuna gelir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Çakışan iskontoları için en uygun birleşimi belirleme</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İskontolar çakıştığında, en düşük hareket toplamını veya en yüksek toplam iskontoyu oluşturacak çakışan iskonto birleşimi belirlemeniz gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common "Buy 1, get 1 X percent off" (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yaygın olarak kullanılan '1 satın al, 1 al X yüzdesi' (BOGO) perakende iskontosunda olduğu gibi, iskonto tutarı satın alınan ürünlerin fiyatına göre değişiklik gösterdiğinde, bu işlem birleşimsel iyileştirme konusu durumuna gelir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This article applies to Microsoft Dynamics AX 2012 R3 with KB 3105973 (released November 2, 2015) or later, and to Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu makale, Microsoft Dynamics AX 2012 R3, KB 3105973 (yayınlanma tarihi 2 Kasım 2015) veya sonrası ve Microsoft Dynamics 365 for Retail için geçerlidir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To determine the combination overlapping discounts to apply in a timely manner, we have introduced a method for applying overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zamanında uygulayabilmek için çakışan iskonto karmasını belirlemek için, çakışan iskontoları uygulamak için bir yöntem geliştirdik.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>We call this new method <bpt id="p1">**</bpt>marginal value ranking<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu yeni yönteme <bpt id="p1">**</bpt>Marjinal değer sıralaması<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Marginal value ranking is used when the time that is required in order to evaluate the possible combinations of overlapping discounts exceeds a threshold that is configurable on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Marjinal değer sıralaması, olası çakışan iskonto birleşimlerini değerlendirmek için gerekli süre, <bpt id="p1">**</bpt>Perakende parametreleri<ept id="p1">**</ept> sayfasında yapılandırılabilen eşiği aştığında kullanılır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In the marginal value ranking method, a value is calculated for each overlapping discount by using the discount's value on the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Marjinal değer sıralama yönteminde, iskontonun paylaşılan ürünlerdeki değeri kullanılarak her çakışan iskonto için hesaplanır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The overlapped discounts are then applied from the highest relative value to the lowest relative value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Çakışan iskontolar, en yüksek göreli değerden en küçük göreli değere doğru uygulanır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For details about the new method, see the "Marginal value" section, later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yeni yöntem hakkında daha fazla bilgi için bu makalenin ilerleyen kısımlarındaki "Marjinal değer" bölümüne bakın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Marginal value ranking isn't used when the discount amounts for a product aren't affected by another product in the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ürün iskonto tutarları hareketteki başka bir ürün tarafından etkilenmiyorsa, marjinal değer sıralaması kullanılmaz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>For example, this method isn't used for two simple discounts, or for a simple discount and a single product quantity discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Örneğin, bu yöntem iki basit iskonto veya bir basit iskonto ve tek bir ürün miktarı iskontosu için kullanılmaz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Discount examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İskonto örnekleri</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can create an unlimited number of retail discounts on a common set of products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ortak bir ürün kümesi üzerinde sayısız perakende iskontosu oluşturabilirsiniz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>However, because there is no limit, performance issues can occur when you try to calculate the discounts that should be used on the various products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ancak, herhangi bir sınır olmadığından, çeşitli ürünlerde kullanılması gereken iskontoları hesaplamaya çalıştığınızda performans sorunları ortaya çıkabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The following examples illustrate this issue in more detail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu sorun daha ayrıntılı şekilde aşağıdaki örneklerde gösterilmektedir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In example 1, we start with two products and two overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Örnek 1'de, iki ürün ve çakışan iki iskontoyla başlıyoruz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Then, in example 2, we show how the issue evolves as more products are added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Daha sonra örnek 2'de, daha fazla ürün eklendikçe sorunun nasıl değişeceğini gösteriyoruz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Example 1: Two products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Örnek 1: İki ürün ve iki iskonto</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>In this example, two products are required in order to qualify for each discount, and the discounts can't be combined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu örnekte, her iskonto için uygun olarak belirlenecek iki ürün gereklidir ve iskontolar birleştirilemez.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The discounts in this example are <bpt id="p1">**</bpt>Best price<ept id="p1">**</ept> discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu örnekteki iskontolar <bpt id="p1">**</bpt>En iyi fiyat<ept id="p1">**</ept> iskontolarıdır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Both products qualify for both discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Her iki ürün de her iki iskonto için uygundur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Here are the two discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">İki iskonto şunlardır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Example of two Best price discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">En iyi fiyat iskontolarına iki örnek</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>For any two products, the better of these two discounts depends on the prices of the two products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Her iki ürün için de bu iki iskontodan en iyi olanı her iki ürünün fiyatına bağlıdır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>When the price of both products is equal or almost equal, discount 1 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Her iki ürünün fiyatı eşit veya birbirine çok yakın olduğunda iskonto 1 daha iyi bir seçenektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>When the price of one product is significantly less than the price of the other product, discount 2 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bir ürünün fiyatı diğer ürünün fiyatından belirgin şekilde daha az olduğunda iskonto 2 daha iyi bir seçenektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Here is the mathematical rule for evaluating these two discounts against each other.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Bu iki iskontoyu birbirine karşı değerlendirmek için matematiksel bir formül buradadır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Rule for evaluating the discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">İndirimleri değerlendirme kuralı</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>When the price of product 1 is equal to two-thirds of the price of product 2, the two discounts are equal.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Ürün 1'in fiyatı, ürün 2'nin fiyatının üçte ikisine eşitse, iki iskonto eşittir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In this example, the effective discount percentage for discount 1 varies from a few percent (when the prices of the two products are far apart) to a maximum of 25 percent (when the two products have the same price).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu örnekte, iskonto 1 için etkin iskonto yüzdesi, yüzde birkaç birim (iki ürünün fiyatı birbirinden farklı olduğunda) ile maksimum yüzde 25'e kadar (iki ürünün fiyatı aynı olduğunda) değişenlik gösterir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The effective discount percentage for discount 2 is fixed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Etkin iskonto yüzdesi iskonto 2 için sabittir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>It's always 20 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Daima yüzde 20'dir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Because the effective discount percentage for discount 1 has a range that can be more than or less than discount 2, the best discount depends on the prices of the two products that must be discounted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İskonto 1'in etkin iskonto yüzdesi iskonto 2'den daha fazla veya daha az olabilecek bir aralığa sahip olduğundan, en iyi iskonto iskonto yapılması gereken ürünlerin fiyatlarına bağlı olacaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In this example, the calculation is completed quickly, because only two discounts are applied on only two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu örnekte, yalnızca iki ürüne iki iskonto uygulanacağından, hesaplama hızlıca yapılmıştır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>There are only two possible combinations: one application of discount 1 or one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yalnızca iki olası birleşim vardır: bir iskonto 1 uygulaması veya bir iskonto 2 uygulaması.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>There are no permutations to calculate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hesaplanacak permütasyon yoktur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The value of each discount is calculated by using both products, and the best discount is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Her iskontonun değeri her iki ürün kullanılarak hesaplanır ve en iyi indirim kullanılır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Example 2: Four products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Örnek 2: Dört ürün ve iki iskonto</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Next, we will use four products and the same two discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bundan sonra, dört ürün ve aynı iki iskontoyu kullanacağız.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>All four products qualify for both discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Her dört ürün de her iki iskonto için uygundur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>There are twelve possible combinations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Olası on iki birleşim vardır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>In the end, two discounts will be applied to the transaction in one of three combinations: two applications of discount 1, two applications of discount 2, or one application of discount 1 and one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sonuç olarak, harekete üç birleşimden birinde iki iskonto uygulanacak: iki iskonto 1 uygulaması, iki iskonto 2 uygulaması veya bir iskonto 1 uygulaması ve bir iskonto 2 uygulaması.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>To illustrate the possible combinations, we will look at two different sets of four products that have different prices:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Olası birleşimleri göstermek için, farklı fiyatlara sahip dört üründen oluşan iki farklı kümeye bakacağız:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>All four products have the same price, $15.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dört ürünün hepsi aynı fiyata sahip: $15,00.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In this case, the best discount combination is two applications of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu durumda, en iyi indirim birleşimi iki iskonto 1 uygulamasıdır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Two products will be full price, and two will be 50 percent off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İki ürün tam fiyata sahip olacak ve ikisinde yüzde 50 indirim olacaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The discounted total for the transaction is $45 (15 + 15 + 7.50 + 7.50), which is $15 (25 percent) off the undiscounted total of $60.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hareket için iskonto toplamı $45 (15 + 15 + 7,50 + 7,50) olacaktır, bu da iskonto uygulanmamış $60 toplam tutar üzerinden $15 indirim (yüzde 25) demektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Discount 2 is only $12 (20 percent).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İskonto 2 yalnızca $12 (yüzde 20)'dir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Two products are $20 each, one product is $15, and one product is $5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İki ürününü her biri $20, bir ürün $15 ve bir ürün $5'dir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In this case, the best discount combination is one application of discount 2 and one application of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu durumda, en iyi iskonto birleşimi bir iskonto 2 uygulaması ve bir iskonto 1 uygulamasıdır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The following tables illustrates the discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aşağıdaki tablolarda iskontolar gösterilmiştir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>To read the tables, use one product from a row and one product from a column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tabloları okumak için, bir satırdan bir ürün ve bir sütundan bir ürün kullanın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For example, in the table for discount 1, when you combine the two $20 products, you get $10 off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Örneğin, iskonto 1 için verilen tabloda, $20 değerinde olan iki ürünü birleştirdiğinizde, $10 indirim yaparsınız.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the table for discount 2, when you combine the $15 product and the $5 product, you get $4 off.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">İskonto 2 için verilen tabloda, $15 değerinde olan ürün ile $5 değerinde olan ürünü birleştirdiğinizde, $4 indirim yaparsınız.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Example that uses four products for the same two discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Aynı iki iskonto için dört ürünü kullanan örnek</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>First, we find the largest discount that is available from any two products by using either discount.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Önce, herhangi bir iskontoyu kullanarak iki üründen herhangi biri için mevcut olan en geniş iskontoyu buluyoruz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The two tables show the discount amount for all combinations of the two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İki tablo, iki ürünün tüm kombinasyonları için iskonto tutarını gösterir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The shaded portions of the tables represent either cases where a product is paired with itself, which we can't do, or a reverse pairing of two products that produces the same discount amount and can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tabloların gölgeli kısımları, bir ürünün kendisi ile eşleştirildiği, (bunu yapamayız) veya iki ürünün aynı iskonto tutarını oluşturacak şekilde ters eşleştirildiği ve yok sayılabilecek durumları gösterir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>By looking at the tables, you can see that discount 1 for the two $20 items is the largest discount that is available for either discount on all four products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tablolara bakarak, bu $20 değerindeki iki ürün için iskonto 1'in dört ürünün hepsi üzerindeki iskonto için kullanılabilecek en geniş iskonto olduğunu görebilirsiniz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>(This discount is highlighted in green in the first table.) That leaves only the $15 product and the $5 product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Bu indirim ilk tablodaki yeşil renkle vurgulanır.) Bu, yalnızca $15 değerinde ürün ve $5 değerinde ürün bırakır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>By looking at the two tables again, you can see that, for these two products, discount 1 gives a $2.50 discount, whereas discount 2 gives a $4 discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İki tabloya tekrar baktığınızda, bu iki ürün için iskonto 1'in $2,50 değerinde bir iskonto sağlarken iskonto 2'nin $4 değerinde iskonto sağladığını görebilirsiniz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Therefore, we select discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu nedenle, iskonto 2'yi seçiyoruz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The total discount is $14.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toplam iskonto $14 olur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>To make this discussion easier to visualize, here are two additional tables that show the effective discount percentage for all possible two-product combinations for both discount 1 and discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu tartışmayı daha kolay şekilde görselleştirmek için, hem iskonto 1 hem de iskonto 2 için iki ürüne ilişkin tüm olası birleşimlerle ilgili etkin iskonto yüzdesini gösteren iki ek tablo sağlanmıştır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Only half the list of combinations is included, because, for these two discounts, the order in which the two products are put into the discount doesn't matter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu iki iskonto için, iki ürününü hangi sırayla iskontoya konulduğu önemli olmadığından, birleşimler listesinin yalnızca yarısı dahil edilmiştir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The highest effective discount (25 percent) is highlighted in green, and the lowest effective discount (10 percent) is highlighted in red.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">En yüksek etkili iskonto (yüzde 25) yeşil renkle vurgulanır ve en düşük etkili iskonto (yüzde 10) kırmızı renkte vurgulanır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Effective discount percentage for all two-product combinations for both discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Her iki iskonto için her iki ürün kombinasyonu için etkili iskonto yüzdesi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>When prices vary, and two or more discount compete, the only way to guarantee the best combination of discounts is to evaluate both discounts and compare them.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Fiyatlar farklılık gösterdiğinde ve iki veya daha fazla iskonto rekabet ettiğinde, en iyi iskonto birleşimini garanti etmenin tek yolu her iki iskontoyu değerlendirmek ve karşılaştırmaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Total possible combinations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toplam olası birleşimler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section continues the example from the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu bölümde önceki bölümde verilen örnekler devam etmektedir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>We will add more products and another discount, and see how many combinations must be calculated and compared.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Daha fazla ürün ve başka bir iskonto ekleyecek ve kaç birleşimin hesaplanması ve karşılaştırılması gerektiğini göreceğiz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The following table shows the number of possible discount combinations as the product quantity increases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aşağıdaki tabloda, ürün miktarı arttıkça olası iskonto birleşimlerinin sayısı gösterilmektedir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>The table shows what happens both when there are two overlapping discounts, as in the previous example, and when there are three overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tablo, hem önceki örnekte olduğu gibi çakışan iki iskonto olduğunda hem de çakışan üç iskonto olduğunda ne olacağını gösterir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The number of possible discount combinations that must be evaluated soon exceeds what even a fast computer can calculate and compare quickly enough to be acceptable for retail transactions.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Değerlendirilmesi gereken olası iskonto birleşimlerinin sayısı, hızlı bir bilgisayarın bile perakende hareketleri için yeterince hızlı olacak şekilde hesaplayıp karşılaştırabileceği sayıyı aşar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Number of possible discount combinations as the product quantity increases</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Ürün miktarı arttıkça olası iskonto birleşimlerinin sayısı.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>When even larger quantities or more overlapping discounts are applied, the total number of possible discount combinations quickly goes into the millions, and the time that is required in order to evaluate and select the best possible combination quickly becomes noticeable.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Daha yüksek miktarlar veya daha fazla çakışan iskonto uygulandığında, olası toplam iskonto birleşimi sayısı hızla milyonlara ulaşır ve en iyi olası birleşimi değerlendirmek ve seçmek için gereken süre hızla dikkate değer bir süreye ulaşır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Some optimizations have been done in the retail price engine to reduce the total number of combinations that must be evaluated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Değerlendirilmesi gereken birleşimlerin toplam sayısını azaltmak için perakende fiyatı altyapısında bazı iyileştirmeler yapılmıştır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>However, because the number overlapping discounts and the quantities in a transaction aren't limited, a large number of combinations will always have to be evaluated whenever there are overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ancak, bir hareketteki çakışan indirimlerin ve miktarların sayısı sınırsız olduğundan, çakışan iskontolar olduğunda daima çok sayıda birleşimin değerlendirilmesi gerekecektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This issue is the issue that the marginal value ranking method addresses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu sorun, marjinal değer sıralaması yönteminin eğildiği bir sorundur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Marginal value method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Marjinal değer yöntemi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>To resolve the issue of an exponentially increasing number of combinations that must be evaluated, an optimization exists that calculates the value per shared product of each discount on the set of products that two or more discounts can be applied to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Katlanarak artan değerlendirilecek birleşim sayısı sorununu çözmek için, iki veya daha fazla iskonto uygulanabilecek ürün kümesindeki her iskonto için paylaşılan ürün başına değeri hesaplayan bir iyileştirme bulunmaktadır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>We refer to this value as the <bpt id="p1">**</bpt>marginal value<ept id="p1">**</ept> of the discount for the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu değere, paylaşılan ürünler için iskontonun <bpt id="p1">**</bpt>marjinal değeri<ept id="p1">**</ept> olarak başvuruyoruz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>The marginal value is the average per product increase in the total discount amount when the shared products are included in each discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Marjinal değer, her bir iskontoya paylaşılan ürünler eklendiğinde toplam iskonto tutarında ürün başına ortalama artış değeridir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The marginal value is calculated by taking the total discount amount (DTotal), subtracting the discount amount without the shared products (DMinus<ph id="ph1">\\</ph> Shared), and dividing that difference by the number of shared products (ProductsShared).</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Marjinal değer, toplam iskonto tutarı (DTotal) alınıp, paylaşılan ürünler olmadan iskonto tutarı (DMinus<ph id="ph1">\\</ph> Shared) düşülerek ve bu fark paylaşılan ürünlerin sayısına (ProductsShared) bölünerek hesaplanır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Formula for calculating marginal value</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Marjinal değeri hesaplama formülü</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>After the marginal value of each discount on a shared set of products is calculated, the discounts are applied to the shared products in order, exhaustively, from highest marginal value to lowest marginal value.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Paylaşılan ürün kümesindeki her iskontonun marjinal değeri hesaplandıktan sonra, iskonotolar, kapsamlı olarak, yüksek marjinal değerden düşük marjinal değere doğru sıralanarak paylaşılan ürünlere uygulanır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For this method, all remaining discount possibilities aren't compared every time after a single instance of a discount is applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu yöntem için, her tek iskonto örneği uygulandıktan sonra kalan iskonto olasıklıkları karşılaştırılmaz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Instead, the overlapping discounts are compared one time and then applied in order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bunun yerine, çakışan iskontolar bir kez karşılaştırılır ve sonra sırayla uygulanır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>No additional comparisons are done.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hiçbir ek karşılaştırma yapılmaz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>You can configure the threshold to switch to the marginal value method on the <bpt id="p1">**</bpt>Discount<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eşiği <bpt id="p2">**</bpt>Perakende parametreleri<ept id="p2">**</ept> sayfasının <bpt id="p1">**</bpt>İskonto<ept id="p1">**</ept> sekmesindeki marjinal değerine geçecek şekilde yapılandırabilirsiniz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>The acceptable time to calculate the total discount varies across retail industries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toplam iskontoyu hesaplamak için kabul edilebilir süre perakende endüstrileri arasında farklılık gösterir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>However, this time generally falls in the range of tens of milliseconds to one second.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ancak, bu süre genellikle on milisaniye ile bir saniye aralığında olur.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>