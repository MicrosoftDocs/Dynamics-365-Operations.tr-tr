<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="work-with-store-inventory.md" target-language="tr-TR">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>work-with-store-inventory.418f90.551a8408aa730bc1916f1c57b7cfd773966ce8bf.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>551a8408aa730bc1916f1c57b7cfd773966ce8bf</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\work-with-store-inventory.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Store inventory management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mağaza stok yönetimi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the types of documents that you can use to manage inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu konuda, stoku yönetmek için kullanabileceğiniz belge türleri açıklanmaktadır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Store inventory management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mağaza stok yönetimi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>When working with inventory in Dynamics 365 for Retail and using the POS application, it is important to note that POS provides limited support for inventory dimensions and certain inventory item types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Retail içine stok ile çalışırken ve POS uygulamasını kullanırken, POS'un stok boyutları ve çeşitli stok öğesi türleri için sınırlı destek sağladığını dikkate almak önemlidir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The POS solution does not support the following item configurations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS çözümü aşağıdaki öğe yapılandırmalarını desteklemez:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>BOM items (except kit products, which utilize some components of the BOM framework)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ürün reçetesi öğeleri (ürün reçetesi çerçevesinin bazı bileşenlerini kullanan paket ürünler hariç)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Catch weight items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fiili ağırlık maddeleri</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Batch-controlled items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toplu iş kontrollü maddeler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The POS application currently does not support the following tracking dimensions in the POS:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS uygulaması şu anda POS içindeki aşağıdaki izleme boyutlarını desteklemez:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Batch tracking dimension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toplu iş izleme boyutu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Owner dimension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sahip boyutu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The POS solution provides limited support for the following dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS çözümü, aşağıdaki boyutlar için sınırlı destek sağlar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Limited support indicates that the POS may default some of these dimensions into inventory transactions automatically based on warehouse/store setup configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sınırlı destek, POS'un bu boyutlardan bazılarını stok hareketlerine otomatik olarak ambar/mağaza kurulum yapılandırmasına varsayılana dönebileceğini belirtir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>POS will not fully support the dimensions in the way they are supported if a sales transaction is manually entered into the ERP.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">POS, bir satış hareketi ERP'ye el ile girilirse desteklendikleri gibi tam olarak boyutları desteklemez.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">**</bpt>Warehouse Location<ept id="p1">**</ept> – Users will not have the ability to manage the receiving warehouse location for items received into a store warehouse when the store has not been configured to use the warehouse management process.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Ambar Konumu<ept id="p1">**</ept> - Mağaza ambar yönetim işlemini kullanmak üzere yapılandırılmadığında kullanıcılar bir mağaza ambarına alınan maddeler için teslim alma ambar konumunu yönetme özelliğine sahip olmaz.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>A default receiving location defined on the store warehouse will be used for these items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu maddeler için mağaza ambarında tanımlanan varsayılan bir teslim alma yerleşimi kullanılacaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>If the warehouse management process has been enabled for the store, limited support that prompts the user to choose a receiving location for the entire receipt will be triggered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ambar yönetimi işlemi mağaza için etkinleştirilmişse, kullanıcıdan tüm giriş için bir teslim alma konumu seçmesini isteyen sınırlı destek tetiklenir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Items sold from the store will always be sold out of the default retail location as defined on the store warehouse setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mağazadan satılan maddeler, mağaza ambar kurulumunda tanımlandığı şekilde, her zaman varsayılan perakende konumundan satılır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The location for managing return inventory can be controlled through default return location definition on the store warehouse or based on return reason codes as defined in the return location policy.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Ambar iadesi yönetimi yerleşimi, mağaza ambarındaki varsayılan iade konumu tanımı aracılığıyla veya iade konumu ilkesinde tanımlandığı şekilde iade neden koduna dayalı olarak denetlenebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>License plate<ept id="p1">**</ept> – License plates are only applicable when <bpt id="p2">**</bpt>Use warehouse management process<ept id="p2">**</ept> has been enabled on the item and the store warehouse.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Plaka<ept id="p1">**</ept> - Plakalar yalnızca <bpt id="p2">**</bpt>Ambar yönetimi sürecini kullan<ept id="p2">**</ept> madde ve mağaza ambarında etkinleştirilmişse uygulanır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>In POS, if inventory is received into a store warehouse where the warehouse management process has been enabled, and the location chosen to receive the item into is tied to a location profile that requires license plate control, the POS application will systematically apply a license plate to the receiving line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS'ta, stok ambar yönetimi işleminin etkinleştirildiği bir mağaza ambarına teslim alınırsa ve maddeyi teslim almak için seçilen yerleşim plaka kontrolü gerektiren bir yerleşim profiline bağlıysa, POS uygulaması bir plakayı teslim alma satırına sistematik olarak uygular.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Users in POS will not have the ability to change or manage this license plate data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS'taki kullanıcıların bu palka verilerini değiştirme veya yönetme yetkisi yoktur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>If full management of license plates is required, it is suggested the store use the WMS mobile application or the back office ERP client to manage the receipt of these items.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Plakaların tam yönetimi gerekiyorsa, mağazanın bu maddelerin girişini yönetmek için WMS mobil uygulamasını veya arka ofis ERP istemcisini kullanması önerilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Serial number<ept id="p1">**</ept> – The POS application has limited support for single serial number to be registered on a transaction sales line for orders created in POS with serialized items.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Seri numarası<ept id="p1">**</ept> - POS uygulaması, serileştirilmiş maddelerle POS'ta oluşturulan siparişler için bir hareket satış satırına kaydedilecek tek seri numarası için sınırlı destek sağlar.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>This serial number is not validated against registered serial numbers already in inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu seri numarası zaten stokta bulunan kayıtlı seri numaraları ile doğrulanamaz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>If a sales order is created in the call center channel or fulfilled through the ERP and multiple serial numbers are registered to a single sales line during the fulfillment process in the ERP, these serial numbers will not be able to be applied or validated if a return is processed in POS for these orders.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Bir satış siparişi çağrı merkezi kanalında oluşturulursa veya ERP aracılığıyla karşılanırsa ve çoklu seri numaraları ERP'de karşılama işlemi sırasında tek bir satış satırına kaydedilirse, bu seri numaralar bu siparişler için POS'ta bir iada işlenmesi durumunda uygulanmaz veya doğrulanmaz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">**</bpt>Inventory status<ept id="p1">**</ept> – For items that use the warehouse management process and require an inventory status, this status field is not able to be set or modified through the POS application.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Stok durumu<ept id="p1">**</ept> - Ambar yönetimi sürecini kullanan ve stok durumu gerektiren maddeler için, bu durum alanı POS uygulaması aracılığıyla ayarlanamaz veya değiştirilemez.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The default inventory status as defined on the store warehouse configuration will be used when items are received into inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mağaza ambar yapılandırmasında tanımlanan varsayılan stok durumu, maddeler stoğa alındığında kullanılır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>All organizations must test item configurations through POS in development or test environments before deploying them to production.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tüm kuruluşların POS aracılığıyla madde yapılandırmalarını üretime dağıtmadan önce geliştirme veya test ortamlarında test etmeleri gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Test your items by performing regular cash and carry sales transacting and creating customer orders (if applicable) through the POS with your items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Öğelerinizi (eğer uygunsa) sıradan nakit ve taşıma satış hareketleri gerçekleştirerek ve müşteri siparişleri oluşturarak POS üzerinde maddeleriniz ile test edin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Testing must include running a full statement posting processes in your test environment and verifying that there are no issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Testin, test ortamınızda tam bildirim deftere nakil işlemini çalıştırmayı içermesi ve sorun olmadığını doğrulaması gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Configuring items in a way that is not supported by the POS application, without proper testing, can result in your statement posting process failing in production without an easy way to correct the issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Maddeleri POS uygulamasında desteklenmeyen bir şekilde, doğru biçimde test etmeden yapılandırmak, bildirim deftere nakil işleminizin, sorunları kolay bir düzeltme şekli olmadan üretimde başarısız olmasına neden olabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Partner or customer customizations to the application may optionally be considered to allow these posting processes to successfully complete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Uygulamadaki ortak veya müşteri özelleştirmeleri, isteğe bağlı olarak bu deftere nakil işlemlerinin başarıyla tamamlanmış kabul edilebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>If customizations are not needed, the organization must ensure that the product configuration of your products has been done in a way that is supported by the standard POS application/order creation/statement posting process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Özelleştirmeler gerekli değilse, kuruluşun ürünlerinizin ürün yapılandırmasının, standart POS uygulaması/sipariş oluşturma/bildirim deftere nakletme işlemi tarafından desteklenmiş bir şekilde yapıldığından emin olması gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Purchase orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satın alma siparişleri</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Purchase orders are created at the head office.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satınalma siparişleri merkez ofiste oluşturulur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail through the <bpt id="p1">**</bpt>Picking/Receiving<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satınalma siparişi başlığına bir perakende ambarı dahil edilirse, sipariş Microsoft Dynamics 365 for Retail'de <bpt id="p1">**</bpt>Malzeme çekme/Teslim alma<ept id="p1">**</ept> işlemi aracılığıyla Modern POS (MPOS) veya Cloud POS kullanılarak mağazada teslim alınabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>After the quantities that are received at the store are entered in the <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> field in POS for the purchase order document, they can be saved locally or committed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mağazada teslim alınan miktarlar satınalma siparişi belgesi için POS'ta <bpt id="p1">**</bpt>Şimdi Teslim Al<ept id="p1">**</ept> alanına girildiğinde, bunlar yerel olarak kaydedilebilir veya kabul edilebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Saving this data locally has no effect on in-stock inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu verilerin yerel olarak kaydedilmesi, stoktaki stok üzerinde herhangi bir etkiye sahip değildir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Saving should be done only if the user is not ready to post the receipt to HQ and just needs a way to temporarily store the previously entered <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yalnızca kullanıcının girişi HQ'ya göndermeye hazır olmaması ve önceden girilen <bpt id="p1">**</bpt>Şimdi Teslim Al<ept id="p1">**</ept> verilerini geçici olarak saklamak için bir yola gereksinim duyması durumunda kaydetme işlemi yapılmalıdır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>This saves the receive now data locally to the user's channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Böylece, şimdi teslim al verileri kullanıcının kanal veritabanına yerel olarak kaydedilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>After the document is processed using the <bpt id="p1">**</bpt>Commit<ept id="p1">**</ept> option, the <bpt id="p2">**</bpt>Receive Now<ept id="p2">**</ept> data is sent to HQ and the purchase order receipt will be posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Belge <bpt id="p1">**</bpt>Kaydet<ept id="p1">**</ept> seçeneği kullanılarak işlendikten sonra <bpt id="p2">**</bpt>Şimdi Teslim Al<ept id="p2">**</ept> verileri HQ'ya gönderilir ve satınalma siparişi girişi deftere nakledilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Transfer orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Transfer emirleri</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>A transfer order can specify that a particular store is the location that items can be shipped from or the location the inventory will be received into.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Transfer emri, belirli bir mağazanın maddelerin sevk edileceği yer veya stoğun teslim alınma konumu olduğunu belirtebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the POS user is the shipping warehouse for a transfer order, they will be able to enter <bpt id="p1">**</bpt>Ship Now<ept id="p1">**</ept> quantities from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS kullanıcısı bir transfer emri için sevkiyat ambarı ise, POS 'tan <bpt id="p1">**</bpt>Şimdi Sevket<ept id="p1">**</ept> miktarlarını girebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The data entered by the shipping store can be saved locally or committed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sevkiyat mağazası tarafından girilen veriler yerel olarak kaydedilebilir veya kabul edilebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>When saved locally, no updates are made to the transfer order document in HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yerel olarak kaydedildiğinde, HQ içindeki transfer emri belgesinde herhangi bir güncelleştirme yapılmaz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Saving should be done only if the user is not ready to post the shipment to HQ and needs a way to temporarily store the previously entered <bpt id="p1">**</bpt>Ship Now<ept id="p1">**</ept> data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yalnızca kullanıcının sevkiyatı HQ'ya nakletmeye hazır olmaması ve önceden girilen <bpt id="p1">**</bpt>Şimdi Sevket<ept id="p1">**</ept> verilerini geçici olarak saklamak için bir yola gereksinim duyması durumunda kaydetme işlemi yapılmalıdır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>After the store is ready to confirm shipment, the <bpt id="p1">**</bpt>Commit<ept id="p1">**</ept> option should be selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mağaza sevkiyatı onaylanmaya hazır olduktan sonra, <bpt id="p1">**</bpt>Kaydet<ept id="p1">**</ept> seçeneği seçilmelidir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>This posts the shipment of the transfer order in HQ so that the receiving warehouse will now be able to receive against it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Böylece, HQ'daki transfer emrinin sevkiyatı deftere nakledikir ve teslim alma ambarı artık teslim alabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>If the POS user is the receiving warehouse for a transfer order, they will be able to enter the <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> quantities from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS kullanıcısı bir transfer emri için teslim alma ambarı ise, POS'tan <bpt id="p1">**</bpt>Şimdi Teslim Al<ept id="p1">**</ept> miktarlarını girebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The data entered by the receiving store can be saved locally or committed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Teslim alma mağazası tarafından girilen veriler yerel olarak kaydedilebilir veya kabul edilebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Saving should be done only if the user is not ready to post the receipt to HQ and needs a way to temporarily store the previously entered <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yalnızca kullanıcının girişi HQ'ya göndermeye hazır olmaması ve önceden girilen <bpt id="p1">**</bpt>Şimdi Teslim Al<ept id="p1">**</ept> verilerini geçici olarak saklamak için bir yola gereksinim duyması durumunda kaydetme işlemi yapılmalıdır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>This saves the receive now data locally to the user's channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Böylece, şimdi teslim al verileri kullanıcının kanal veritabanına yerel olarak kaydedilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>After the document is processed using the <bpt id="p1">**</bpt>Commit<ept id="p1">**</ept> option, the <bpt id="p2">**</bpt>Receive Now<ept id="p2">**</ept> data is sent to HQ and the transfer order receipt will be posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Belge <bpt id="p1">**</bpt>Kaydet<ept id="p1">**</ept> seçeneği kullanılarak işlendikten sonra <bpt id="p2">**</bpt>Şimdi Teslim Al<ept id="p2">**</ept> verileri HQ'ya gönderilir ve transfer emri girişi deftere nakledilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>It's important to note that the receiving store will be restricted to only being able to commit receive quantities that are equal to or less than shipped quantities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Teslim alma mağazasının yalnızca sevk edilen miktarlara eşit veya bundan küçük olan teslim alma miktarlarını kaydedebildiğini unutmamanız gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>An attempt to receive quantities on a transfer order that have not previously shipped will result in errors and the receipt will not be confirmed in HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bir transfer emrindeki daha önce sevk edilmemiş miktarları teslim alma girişimi hatalara neden olur ve giriş HQ'da onaylanmaz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Stock counts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stok sayımları</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Stock counts can be either scheduled or unscheduled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stok sayımları zamanlanmış veya zamanlanmamış olabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Planlı stok sayımları sayılması gereken maddeleri belirten merkez ofiste başlatılır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Merkez ofis mağazada alınabilecek bir sayım belgesi oluşturur ve fiili eldeki stok miktarları burada MPOS'a veya Cloud POS'a girilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mağazada planlanmamış stok sayımları başlatılır ve fiili eldeki stok miktarları MPOS'ta veya Cloud POS'te güncelleştirilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Planlı stok sayımlarından farklı olarak, planlanmamış stok sayımlarında önceden tanımlanmış bir madde listesi yoktur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>When a stock count of either type is completed, it is committed and sent to the head office.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Her iki türün birinden bir stok sayımı tamamlandığında, özen ve merkez ofise gönderilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>At the head office, the count is validated and posted as a separate step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Merkez ofiste sayım doğrulanır ve ayrı bir adım olarak deftere nakledilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Inventory lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stok arama</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The current product quantity on hand for multiple stores and warehouses can be viewed on the <bpt id="p1">**</bpt>Inventory lookup<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Çok sayıda mağaza ve ambar için geçerli eldeki ürün miktarı, <bpt id="p1">**</bpt>Stok arama<ept id="p1">**</ept> sayfasından görüntülenebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Geçerli eldeki miktara ek olarak, gelecekte karşılanabilir (ATP) miktarlar, her bir mağaza için görüntülenebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>To do so, select the store that you want to view the ATP for and then click <bpt id="p1">**</bpt>Show store availability<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bunu yapmak için, ATP'sini görüntülemek istediğiniz mağazayı seçin ve <bpt id="p1">**</bpt>Mağaza kullanılabilirliğini göster<ept id="p1">**</ept> üzerine tıklayın.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>