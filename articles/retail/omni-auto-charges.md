<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="omni-auto-charges.md" target-language="tr-TR">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>omni-auto-charges.2f6e37.47829a6fcae37e03510929dc46b942455016df0b.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>47829a6fcae37e03510929dc46b942455016df0b</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>ffc37f7c2a63bada3055f37856a30424040bc9a3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/16/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\omni-auto-charges.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Çoklu kanal gelişmiş otomatik ücretleri</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes capabilities for managing additional order charges for Retail channel orders using advanced auto charges features.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu konu perakende kanal düzeni masraflar otomatik gelişmiş özelliklerini kullanmak için ek sipariş masrafları yönetmek için kullanılan özellikleri açıklar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Çoklu kanal gelişmiş otomatik ücretleri</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides information on configuration and deployment of the advanced auto-charges feature which are available in Dynamics 365 for Retail version 10.0.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu konu Dynamics 365 for Retail sürüm 10.0. içerisinde yapılandırma ve dağıtım içinde kullanılabilir olan gelişmiş otomatik masraflar özelliği hakkında bilgi sağlar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When the advanced auto-charges features are enabled, orders created in any supported Retail channel (point of sale (POS), call center, and online), can take advantage of the <bpt id="p1">[</bpt>auto-charges<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations defined in the ERP application for both header and line-level related charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gelişmiş otomatik masraflar özellikleri etkinleştirildiğinde, desteklenen herhangi bir Perakende kanalında (satış noktası (POS), çağrı merkezi ve çevrimiçi) içinde oluşturulan siparişler <bpt id="p1">[</bpt>otomatik masraflar<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> yapılandırmalarından hem başlık hem de satır düzeyi ile ilişkili masraflar için faydalanabilirler.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In releases prior to Dynamics 365 for Retail version 10.0, <bpt id="p1">[</bpt>auto-charge<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations are only accessible by orders created in e-Commerce and call center channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Retail sürüm 10.0 öncesi sürümlerde, <bpt id="p1">[</bpt>otomatik masraf<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> yapılandırmaları yalnızca e-ticaret ve çağrı merkezi kanallarında oluşturulan siparişler tarafından erişilebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In versions 10.0 and later, POS-created orders can leverage the auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sürümler 10.0 ve sonrasında, POS tarafından oluşturulan siparişler otomatik masraf yapılandırmalarını kullanabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>That way, additional miscellaneous charges can systematically be added to sales transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu şekilde, ek sair masraflar sistematik olarak satış işlemlerine eklenebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>When using releases prior to version 10.0, a POS user is prompted to manually enter a shipping fee during the creation of a "ship all" or "ship selected" POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.0 öncesi sürümler kullanılırken, bir POS kullanıcısının sevkiyat masrafını "sevk tüm" veya "seçilen sevk" POS hareketi sırasında el ile girmesi istenir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>While the miscellaneous charges capabilities of the application are utilized in respect to how the charges are written to the order, no systematic calculation is provided – the calculation relies on the user's input to determine the value of the charges.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Uygulamanın sair masraflar yeteneği, masrafların siparişe nasıl yazıldığıyla ilgilidir, sistematik hesaplama sağlanmaz; hesaplama, masrafların değerini belirlemek için kullanıcının girdisine dayanmaktadır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The charges can only be added as a single "shipping" related charges code and cannot easily be edited or changed in the POS after they are created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">masraflar yalnızca tek bir "sevkiyat" ile ilgili masraf kodu satırı olarak eklenebilir ve POS içinde oluşturulduktan sonra değiştirilemez veya düzenlenemez.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The use of manual prompts to add shipping charges is still available in versions 10.0 and later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sevkiyat masrafları eklemek için el ile uyarıların kullanımı sürüm 10.0 ve sonrasında kullanılabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>If an organization does not enable the <bpt id="p1">**</bpt>Advanced Auto-charges<ept id="p1">**</ept> parameter, the POS prompts for manual entry of charges will remain the same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bir kuruluş <bpt id="p1">**</bpt>Gelişmiş Otomatik masraflar<ept id="p1">**</ept> parametresini etkinleştirmezse, POS masrafların el ile girişini aynı kalacaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>With the advanced auto-charges feature, POS users can have systematic calculations for any defined miscellaneous charges based on auto-charges setup tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gelişmiş otomatik masraflar özelliğiyle, POS kullanıcıları tanımlanan herhangi bir sair masraflara dayanan sistematik masraflara sahip olabilirler.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In addition, users will have the ability to add or edit an unlimited amount of additional charges and fees to any POS sales transaction at the header or line-level (for a cash and carry or customer order).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ek olarak, kullanıcılar sınırsız sayıda ek masraf ve ücreti herhangi bir POS satışı hareketine başlık veya satır düzeyinde ekleme ve düzenleme olanağına sahip olurlar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Enabling advanced auto-charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gelişmiş otomatik masrafları etkinleştirmek</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>On the <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Headquarters setup <ph id="ph2">\&gt;</ph> Parameters <ph id="ph3">\&gt;</ph> Retail parameters<ept id="p1">**</ept> page, go to the <bpt id="p2">**</bpt>Customer orders<ept id="p2">**</ept> tab. On the <bpt id="p3">**</bpt>Charges<ept id="p3">**</ept> FastTab, set <bpt id="p4">**</bpt>Use advanced auto-charges<ept id="p4">**</ept> to <bpt id="p5">**</bpt>Yes<ept id="p5">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Perakende <ph id="ph1">\&gt;</ph> Genel merkez kurulumu <ph id="ph2">\&gt;</ph> Parametreler <ph id="ph3">\&gt;</ph> Perakende parametreleri<ept id="p1">**</ept> sayfasında, <bpt id="p2">**</bpt>Müşteri siparişleri<ept id="p2">**</ept> sekmesine gidin. <bpt id="p3">**</bpt>Masraflar<ept id="p3">**</ept> hızlı sekmesinde, <bpt id="p4">**</bpt>Gelişmiş otomatik masrafları kullan<ept id="p4">**</ept>'ı <bpt id="p5">**</bpt>Evet<ept id="p5">**</ept> olarak ayarlayın.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Advanced Auto-Charges Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gelişmiş Otomatik masraflar Parametresi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>When advanced auto-charges are enabled, users are no longer prompted to manually enter a shipping charge at the POS terminal when creating a ship-all or ship-selected customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gelişmiş otomatik masraflar etkin olduğunda, kullanıcıların bir sevkiyat masrafını POS terminalinde, tümünü sevk veya seçilen müşteri siparişini sevk seçeneği seçildiğinde sevkiyat masrafını el ile girmeleri daha fazla gerekmez.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>POS order charges are systematically calculated and added to the POS transaction (if a corresponding auto-charges table that matches the criterion of the order being created are found).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS sipariş masrafları sistematik olarak hesaplanır ve POS hareketine eklenir (oluşturulan siparişin kriteriyle eşleşen, karşılık gelen otomatik masraf tablosu bulunursa).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Users can also add or maintain header or line-level charges manually through newly added POS operations that can be added to the POS screen layouts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanıcılar ayrıca, POS ekranı düzenlerine eklenebilecek başlık veya satır düzeyi masrafları el ile yeni eklenen POS işlemleri üzerinden ekleyebilir veya koruyabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>When advanced auto-charges are enabled, the existing <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> for <bpt id="p2">**</bpt>Shipping charges code<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> are no longer utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gelişmiş otomatik masraflar etkinleştiğinde, mevcut <bpt id="p2">**</bpt>Sevkiyat masrafları kodu<ept id="p2">**</ept> ve <bpt id="p3">**</bpt>Geri ödeme sevkiyat masrafları<ept id="p3">**</ept> için <bpt id="p1">**</bpt>Perakende parametreleri<ept id="p1">**</ept> artık kullanılmaz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>These parameters are only applicable if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu parametreler yalnızca <bpt id="p1">**</bpt>Gelişmiş otomatik masraflar kullan<ept id="p1">**</ept> parametresi <bpt id="p2">**</bpt>Hayır<ept id="p2">**</ept> olarak ayarlandığında uygulanabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Before you enable this feature, ensure that you have tested and trained your employees, as this will change the business process flow of how shipping or other charges are calculated and added to POS sales orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu özelliği etkinleştirmeden önce, çalışanlarınızı eğittiğinizden ve test ettiğinizden emin olun, çünkü bu, sevkiyat veya diğer masrafların nasıl hesaplandığı ve POS satış siparişlerine eklendiği iş işlemi akışını değiştirecektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Make sure that you understand the impact of the process flow to the creation of transactions from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS'tan işlemlerin oluşturulması işlem akışı üzerindeki etkisini anladığınızdan emin olun.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For call center and e-Commerce orders, the impact of enabling advanced auto-charges is minimal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Çağrı merkezi ve e-ticaret siparişleri için gelişmiş otomatik masrafların etkisi asgari düzeydedir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Call center and e-Commerce applications will continue to have the same behavior they have had historically related to the auto-charges tables to calculate additional order fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Çağrı merkezi ve e-ticaret uygulamaları, geçmişte otomatik masraflar tablosunda ek sipariş ücretleriyle ilgili sahip oldukları eski davranışa sahip olacaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Call center channel users will continue to have the ability to manually edit any system calculated auto-charges at the header or line level, or manually add additional miscellaneous charges at the header or line level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Çağrı merkezi kanalı kullanıcıları, sistem tarafından hesaplanan otomatik masrafları başlık veya satır düzeyinde el ile düzenleme olanağına sahip olmaya devam edecektir veya sair masrafları başlık veya satır düzeyinde el ile ekleyebilirler.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Additional POS operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ek POS işlemleri</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>For advanced auto-charges to work properly in your POS application environment, new POS operations have been added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gelişmiş otomatik masrafların POS uygulaması ortamınızda doğru çalışması için yeni POS operasyonları eklenmiştir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>These operations must be added to your <bpt id="p1">[</bpt>POS screen layouts<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> and deployed to the POS devices as you deploy advanced auto-charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu işlemlerin <bpt id="p1">[</bpt>POS ekran düzenlerine<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> eklenmesi ve gelişmiş otomatik masraflar dağıttığınızda POS cihazlarına dağıtılması gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>If these operations are not added, users will not be able to manage or maintain miscellaneous charges on the POS transactions and will have no way of adjusting or changing the charges values that are systematically calculated based on auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu işlemler eklenmezse, kullanıcılar sair masrafları POS hareketleri üzerinde yönetemez veya koruyamaz ve sistematik olarak otomatik masraf yapılandırmalarına dayanan masraf değerlerini değiştiremez veya ayarlayamazlar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>At minimum, it is suggested that you deploy the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation to your POS layout.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">En azından, <bpt id="p1">**</bpt>masrafları yönet<ept id="p1">**</ept> operasyonunu POS düzeninizde dağıtmanız önerilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The new operations are as follows.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Yeni operasyonlar şu şekildedir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>142 - Manage charges<ept id="p1">**</ept> – Use this operation to allow POS users to view and edit miscellaneous charges for the POS transaction that were either added manually or systematically through auto-charges calculations.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>142 - masrafları yönet<ept id="p1">**</ept> - Bu işlemi POS kullanıcılarının el ile veya otomatik masraf hesaplamaları ile sistematik olarak eklenmiş POS hareketleri için sair masrafları görüntülemelerini ve düzenlemelerini sağlar.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>141 - Add header charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a header-level miscellaneous charge to any POS sales transaction (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>141 - Başlık masrafları ekle<ept id="p1">**</ept> - Bu işlemi, kullanıcıya başlık düzeyinde sair masrafı herhangi bir POS hareketine el ile ekleme yeteneği sağlamak (ve kullanılacak masraf kodunu seçmek) için kullanın.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>140 - Add line charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a line level miscellaneous charge to any POS sales transaction line (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>140 - Satır masrafları ekle<ept id="p1">**</ept> - Bu işlemi, kullanıcıya satır düzeyinde sair masrafı herhangi bir POS hareketi satırına el ile ekleme yeteneği sağlamak (ve kullanılacak masraf kodunu seçmek) için kullanın.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>143 - Recalculate charges<ept id="p1">**</ept> – Use this operation to perform a full re-calculation of the charges for the sales transaction.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>143 - masrafları yeniden hesapla<ept id="p1">**</ept> - Bu işlemi satış hareketi için masrafların tamamen yeniden hesaplanmasını gerçekleştirmek için kullanın.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Any previously user-overwritten auto-charges will be recalculated based on the current cart configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Daha önceden kullanıcı tarafından üzeri yazılan otomatik değişiklikler geçerli sepet yapılandırmasına dayanarak yeniden hesaplanır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>As with all POS operations, security configurations can be made to require manager approval in order to execute the operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tüm POS işlemlerinde olduğu gibi, güvenlik yapılandırmalarının işlemin gerçekleştirilebilmesi için yönetici onayına ihtiyaç duyması sağlanabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>It is important to note that the above listed POS operations can also be added to the POS layout even if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yukarıda listelenen POS operasyonlarının ayrıca POS düzenine, <bpt id="p1">**</bpt>Gelişmiş otomatik masrafları kullan<ept id="p1">**</ept> parametresi devre dışıysa bile eklenebileceğini anımsamak önemlidir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In this scenario, organizations will still get added benefits of being able to view manually added charges and edit them using the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu senaryoda, kuruluşlar, el ile eklenen masrafları görüntüleyebilme ve bunları <bpt id="p1">**</bpt>Masrafları yönet<ept id="p1">**</ept> işlemini kullanarak düzenleme faydalarına sahip olurlar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Users may also use the <bpt id="p1">**</bpt>Add header charges<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Add line charges<ept id="p2">**</ept> operations for POS transactions even when <bpt id="p3">**</bpt>Use advanced auto-charges<ept id="p3">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanıcılar <bpt id="p1">**</bpt>Başlık masrafları ekle<ept id="p1">**</ept> ve <bpt id="p2">**</bpt>Satır masrafları ekle<ept id="p2">**</ept> operasyonlarını POS hareketler için <bpt id="p3">**</bpt>Gelişmiş otomatik masraflar kullan<ept id="p3">**</ept> parametresi devre dışıysa bile kullanabilirler.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation has less functionality if used when <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Masrafları yeniden hesapla<ept id="p1">**</ept> işlemi, <bpt id="p2">**</bpt>Gelişmiş otomatik masrafları kullan<ept id="p2">**</ept> seçeneği devre dışı bırakılmışsa daha az işleve sahiptir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In this sceanrio, nothing would be recalculated and any charges manually added to the transaction would just reset to $0.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu senaryoda, hiçbir şey yeniden hesaplanmaz ve otomatik olarak harekete eklenen tüm masraflar 0,00 $ tutarına sıfırlanır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Use case examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanım örneği</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In this section, sample use cases are presented to help you understand the configuration and usage of auto-charges and miscellaneous charges within the context of Retail channel orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu bölümde, örnek kullanım vakaları size otomatik masraflar ve sair masrafların Perakende kanalı siparişleri bağlamında yapılandırılması ve kullanılmasını anlamanızda yardımcı olmak için sunulur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>These examples illustrate the behavior of the application when the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter has been enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu örnekler, <bpt id="p1">**</bpt>Gelişmiş otomatik sair masraflar kullan<ept id="p1">**</ept> parametresi etkinleştirildiğinde uygulamanın davranışını gösterir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Auto-charges header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Otomatik masraflar başlık masrafları örneği</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanımı vakası senaryosu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>A retailer wants to automatically add charges for freight when transactions are created in any Retail channel that require a shipment of products to the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bir perakendeci, ürünlerin müşteriye nakledilmesi gereken hareketler Perakende kanalında oluşturulduklarında bir navlun için otomatik olarak masrafları eklemek için kullanmak istiyor.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The retailer offers 2 methods of delivery: Ground and Air.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Perakendeci 2 teslimat seçeneği sunmaktadır: kara ve hava yolu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>If a customer chooses Ground delivery and the order value is less than $100, the retailer wants to charge the customer a freight charge of $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bir müşteri Karayolu teslimatını seçerse ve değer 100$'dan az ise, perakendeci müşteriden 10.00$ navlun ücreti talep etmek istemektedir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>If the order is over $100 in value and the customer chooses ground shipping, the customer will not be charged any additional freight fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sipariş 100$ değerin üzerindeyse ve müşteri karayolu sevkiyatını seçerse, kullanıcıdan ek navlun ücretleri talep edilmeyecektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If the customer chooses the Air method of delivery for all orders, regardless of their total value, will be charged a freight fee of $20.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanıcı tüm siparişleri için Hava yöntemini seçerse, toplam değerlerinden bağımsız olarak 20,00$ navlun ücreti talep edilecektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kurulum ve yapılandırma</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This scenario requires the configuration of two auto-charges tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu senaryo, iki otomatik masraf tablosunun yapılandırılmasını gerektirmektedir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Go to <bpt id="p1">**</bpt>Accounts receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sırasıyla <bpt id="p1">**</bpt>Alacak hesapları <ph id="ph1">\&gt;</ph> masraflar kurulumu <ph id="ph2">\&gt;</ph> Otomatik masraflar<ept id="p1">**</ept> seçimlerini yapın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Configure two different header-level auto charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İki farklı başlık seviyesi otomatik masrafı yapılandırmak.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Configure one for the "Ground mode" of delivery and one for the "Air mode" of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"Karayolu modu" teslimatı için bir adet ve "Havayolu modu" teslimatı için bir adet yapılandırın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>For this scenario, configure them to be used for "All customers".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu senaryo için, "Tüm müşteriler" için kullanılmak üzere yapılandırın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>For the ground delivery charges, in the lines section of the <bpt id="p1">**</bpt>Auto-charges<ept id="p1">**</ept> page, define a charge that will be applied for orders between $.01 and $100 as $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Karayolu teslimatı masrafları için <bpt id="p1">**</bpt>Otomatik masraflar<ept id="p1">**</ept> sayfasının satırlar bölümünde, 0,01$ ve 100$ arasındaki siparişler için uygulanacak masrafı 10,00$ olarak ayarlayın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Create another charges line to indicate orders over $100.01 will have no charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">100,01$ üzeri siparişler için masraf olmadığını belirtmek üzere başka bir masraf satırı oluşturun.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Otomatik masraflar örneği</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>For the air delivery charges, in the lines section of the auto-charges form, define a charge of $20.00 that will be applied to all orders (between a value of $.01 to $9,999,999).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hava teslimatı masrafları için otomatik masraflar formunun satırlar bölümünde, tüm siparişlere uygulanacak 20,00$ tutarında bir masraf ayarlayın (0,01$ ve 9.999.999$ arasında değer için).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Send the changes to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Değişiklikleri Perakende Sunucusu/Kanalı Veritabanına gönderin böylece POS onları <bpt id="p1">**</bpt>1040 dağıtım zamanlaması<ept id="p1">**</ept> işini çalıştırırken kullanabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu senaryo için satış işleme</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>After the configuration steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have the ground or air delivery methods set at the header level will utilize these charges and automatically apply them to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yukarıdaki yapılandırma işlemleri tamamlandıktan ve değişiklikler kanal veritabanına uygulandıktan sonra, POS, çağrı merkezi veya e-ticaret kanallarında oluşturulan ve havayolu veya karayolu yöntemlerini başlık seviyesinde uygulanmış olan tüm müşteri siparişleri veya satış hareketleri, bu masrafları otomatik olarak satışa uygulayacaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>At this time the charges will apply to all sales transactions created within the legal entity that utilize these delivery modes, as there is no functionality to designate that an auto-charge configuration will only apply to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Şu anda, masraflar bu teslimat modunu kullanan tüzel varlık içindeki tüm satış hareketlerine uygulanacaktır çünkü otomatik masraf yapılandırmasını yalnızca belirli bir satış kanalına uygulanmak üzere atayacak bir işlevsellik mevcut değildir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For POS and e-Commerce scenarios, because there is no clearly defined "header" on these orders, header-level charges will only apply if all sales lines on the transaction are set to ship with the exact same mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS ve e-ticaret senaryoları için bu siparişler üzerinde net olarak tanımlanmış bir "başlık" olmadığından, başlı düzeyi masrafları yalnızca hareket üzerindeki tüm satış satırları tam olarak aynı teslimat modu ile sevk edilmek üzere ayarlanır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>If there are "mixed-modes" of fulfillment on the transactions created by POS or e-Commerce, only line-level auto-charges will be considered and applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS veya e-ticaret tarafından oluşturulmuş hareketler üzerinde "karışık modlar" varsa, yalnızca satır düzeyi otomatik masraflar dikkate alınır ve uygulanır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>In call center scenarios, the user has control over the setting of the delivery mode at the order header, therefore header-level charges will apply for these orders even if some of the sales lines have been configured to use a different mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Çağrı merkezi senaryolarında, kullanıcı teslimat modu ayarları üzerinde sipariş başlığı üzerinde denetime sahip olacaktır, bu nedenle de başlık düzeyi masraflar bu siparişlere bazı sipariş satırları başka bir teslimat modu kullanmak üzere yapılandırılmış bile olsa uygulanacaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Header-level charges for call center orders will always be based on the mode of delivery that is defined at the order header level of the sales order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Çağrı merkezi için başlık düzeyi masrafları her zaman satış siparişinin sipariş başlık düzeyinde tanımlanmış teslimat modunu kullanacaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Auto-charges line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Otomatik masraflar satır masrafları örneği</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanımı vakası senaryosu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>A retailer wants to add an additional charge to the customer for setup fees when the customer purchases a particular model of computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bir perakendeci, müşteri belirli bir bilgisayar modeli sipariş etmek istediğinde müşteri kurulumu ücretlerine ek bir masraf eklemek istemektedir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>This computer requires additional non-optional setup actions that the retailer will perform for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu bilgisayar, perakendecinin müşteri için gerçekleştireceği ek ve isteğe bağlı olmayan kurulum işlemleri içermektedir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The retailer has informed customers that there will be an additional fee for this setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Perakendeci, müşteriye bu kurulum için ek ücret söz konusu olacağını bildirmiştir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The retailer prefers to manage the charges related to this fee separately from the product sales price for financial reporting purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Perakendeci, bu ücretle ilişkili masrafları finansal raporlama amaçları yüzünden ürün satış fiyatından ayrı olarak yönetmeyi tercih etmektedir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>A setup fee of $19.99 will be charged to the customer when this specific computer is purchased in any retail channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">19,99$ tutarında bir kurulum ücreti, müşteri herhangi bir perakende kanalından bu belirli bilgisayarı satın alırsa ücretlendirilecektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kurulum ve yapılandırma</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This scenario requires the configuration of one line-level auto charges table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu senaryo, bir satır düzeyi otomatik masraf tablosunun yapılandırılmasını gerektirmektedir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Go to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sırasıyla <bpt id="p1">**</bpt>Alacak Hesapları <ph id="ph1">\&gt;</ph> masraflar kurulumu <ph id="ph2">\&gt;</ph> Otomatik masraflar<ept id="p1">**</ept> seçimlerini yapın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Set the <bpt id="p1">**</bpt>Level<ept id="p1">**</ept> drop-down menu to <bpt id="p2">**</bpt>Line<ept id="p2">**</ept>, and create a new auto-charges record for all customers and for the specific product or product group where the setup fees will be charged.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Düzey<ept id="p1">**</ept> açılır menüsünü <bpt id="p2">**</bpt>Satır<ept id="p2">**</ept> olarak ayarlayın ve kurulum ücretinin uygulanacağı belirli ürün veya ürün grubu için tüm müşteriler için yeni bir otomatik masraf kaydı oluşturun.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Otomatik masraflar örneği</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">masrafları Perakende Sunucusu/Kanalı Veritabanına gönderin böylece POS onları <bpt id="p1">**</bpt>1040 dağıtım zamanlaması<ept id="p1">**</ept> işini çalıştırırken kullanabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu senaryo için satış işleme</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>After the configurations steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have this item on the order will trigger a line-level charge to be systematically added to the order total.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yukarıdaki yapılandırma adımları tamamlandıktan ve değişiklikler kanal veritabanına uygulandıktan sonra, bu ögeye siparişte sahip olan tüm POS, çağrı merkezi, e-ticaret kanalı tüm müşteri siparişi veya satışı toplam siparişe sistematik olarak bir satır düzeyi masrafın eklenmesini tetikleyecektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>At this time the charges will apply to any sales line that matches the configuration of the line-level auto charges within the legal entity, as there is no functionality to configure a line-level auto-charge to apply only to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu noktada, masraflar tüzel varlık içinde otomatik masraf satır düzeyi yapılandırmasında eşleşen tüm satışlara uygulanacaktır, çünkü satır düzeyi otomatik masrafın yalnızca belirli bir satış kanalına uygulanmasını sağlayacak bir işlev mevcut değildir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Manual header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">El ile başlık masrafları örneği</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Use case scenario description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanımı vakası açıklaması</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>A retailer is making an exception to typical processes by offering to provide a special home delivery of products to a customers who order products in the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bir perakendeci, mağazadan ürün sipariş eden bir müşteriye özel eve teslim sunmak için tipik işlemlerde bir istisna sunmaktadır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The retailer and the customer have agreed that the customer will pay an additional $25 handling fee for this service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Perakendeci ve müşteri, müşterinin bu hizmet için 25$ işlem ücreti ödemesini kabul etmişlerdir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The order-taker needs to add this additional fee to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Siparişi alanın bu ek ücreti işlem eklemesi gerekmektedir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Because the fee is a blanket fee and not related to any single product on the order, a header charge will be utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ücreti, genel ücret olduğundan ve siparişteki tek bir ürünle ilişkili olmadığından bir başlık masrafı uygulanacaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kurulum ve yapılandırma</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Senaryo için uygun masraf konunu tanımlamak için bu senaryoda kullanılacak masraf kodunun, <bpt id="p1">**</bpt>Alacak Hesapları <ph id="ph1">\&gt;</ph> masraflar kurulumu <ph id="ph2">\&gt;</ph> masraflar<ept id="p1">**</ept>'e giderek doğru şekilde yapılandırıldığından emin olun.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">masraflar örneği</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">masraf, ilgili indirim veya promosyonlar amacıyla "sevkiyat" ile ilgili masraf olarak dikkate alınacaksa, <bpt id="p1">**</bpt>Nakliye masrafı<ept id="p1">**</ept>'ni masraflar kodu üzerinde <bpt id="p2">**</bpt>Evet<ept id="p2">**</ept> olarak ayarlayın</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>If this charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Masrafın sistematik olarak iade işlemi sırasında POS uygulamasında sistematik olarak iade edilmesine olanak sağlanıyorsa, <bpt id="p1">**</bpt>İade edilebilir<ept id="p1">**</ept>'i <bpt id="p2">**</bpt>Evet<ept id="p2">**</ept> olarak ayarlayın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>İade edilebilir<ept id="p1">**</ept> bayrağı yalnızca <bpt id="p2">**</bpt>Gelişmiş otomatik masraflar<ept id="p2">**</ept> parametresi <bpt id="p3">**</bpt>Evet<ept id="p3">**</ept> olarak ayarlanmışsa uygulanabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">masrafları Perakende Sunucusu/Kanalı Veritabanına gönderin böylece POS onları <bpt id="p1">**</bpt>1040 dağıtım zamanlaması<ept id="p1">**</ept> işini çalıştırırken kullanabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>The <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 141).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Masraf başlığı ekle<ept id="p1">**</ept> işleminin <bpt id="p2">[</bpt>POS ekran düzeninizde<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> yapılandırılmış olması gerekir, böylece kullanıcıya POS üzerinden erişilebilir bir düğme bu işlemi çağırmak (işlem 141) üzere mevcut olacaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ekran düzeni değişiminin perakende kanalına, dağıtım zamanlaması işlevi üzerinden de dağıtılması gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Sales processing of manual header charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">El ile başlık masraflarının satış işlemi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Senaryoyu POS uygulamasında gerçekleştirmek için POS kullanıcısının satış hareketini normal biçimde oluşturması, ürünleri ve diğer tüm yapılandırmaları satışa eklemesi gerekecektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Prior to collecting payment, the user should execute the <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation, which will prompt the user to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ödeme almadan önce kullanıcının <bpt id="p1">**</bpt>Başlık masraf ekle<ept id="p1">**</ept> işlemini gerçekleştirmesi gerekir, bu, kullanıcının bir masraf kodunu seçmesini ve masraf değerini girmesi konusunda uyaracaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Once the user completes the process, the charge will be added to the sales order as a header-level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanıcı işlemi tamamladıktan sonra, masraf satış siparişine bir başlık düzeyi masrafı olarak eklenecektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>This process can be applied in the call center by using the existing <bpt id="p1">**</bpt>Charges<ept id="p1">**</ept> feature found on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab on the toolbar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu işlem çağrı merkezinde, araç çubuğundaki <bpt id="p2">**</bpt>Satış<ept id="p2">**</ept> sekmesinde bulunan mevcut <bpt id="p1">**</bpt>Masraflar<ept id="p1">**</ept> özelliğini kullanarak uygulanabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page, the user can add a new charges line to the order header.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Masrafları koru<ept id="p1">**</ept> sayfasında, kullanıcı sipariş başlığına yeni masraflar satırı ekleyebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Manual line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">El ile satır giderleri örneği</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanımı vakası senaryosu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>A customer has requested that 2 of the 5 items on their sales order be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bir müşteri, satış siparişindeki 5 ögeden 2'sinin hediye paketi yapılmasını talep etti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>The retailer offers this optional service for a fee of $2.00 per item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Perakendeci, bu isteğe bağlı hizmeti öge başına 2,00$ karşılığında sunmaktadır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The order-taker will need to add these fees to the specific items that need to be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Siparişi alanın bu ücretleri, hediye paketi yapılacak belirli öğelere eklemesi gerekecektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kurulum ve yapılandırma</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Senaryo için uygun masraf konunu tanımlamak için bu senaryoda kullanılacak masraf kodunun, <bpt id="p1">**</bpt>Alacak Hesapları <ph id="ph1">\&gt;</ph> masraflar kurulumu <ph id="ph2">\&gt;</ph> masraflar<ept id="p1">**</ept>'e giderek doğru şekilde yapılandırıldığından emin olun.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set the <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Gider, ilgili indirim veya promosyonlar amacıyla "sevkiyat" ile ilgili gider olarak dikkate alınacaksa, <bpt id="p1">**</bpt>Nakliye gideri<ept id="p1">**</ept>'ni giderler kodu üzerinde <bpt id="p2">**</bpt>Evet<ept id="p2">**</ept> olarak ayarlayın</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>If the charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Masrafın sistematik olarak iade işlemi sırasında POS uygulamasında sistematik olarak iade edilmesine olanak sağlanıyorsa, <bpt id="p1">**</bpt>İade edilebilir<ept id="p1">**</ept>'i <bpt id="p2">**</bpt>Evet<ept id="p2">**</ept> olarak ayarlayın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>İade edilebilir<ept id="p1">**</ept> bayrağı yalnızca <bpt id="p2">**</bpt>Gelişmiş otomatik masraflar<ept id="p2">**</ept> parametresi <bpt id="p3">**</bpt>Evet<ept id="p3">**</ept> olarak ayarlanmışsa uygulanabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">masrafları Perakende Sunucusu/Kanalı Veritabanına gönderin böylece POS onları <bpt id="p1">**</bpt>1040 dağıtım zamanlaması<ept id="p1">**</ept> işini çalıştırırken kullanabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>The <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 140).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Masraf satırı ekle<ept id="p1">**</ept> işleminin <bpt id="p2">[</bpt>POS ekran düzeninizde<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> yapılandırılmış olması gerekir, böylece kullanıcıya POS üzerinden erişilebilir bir düğme bu işlemi çağırmak (işlem 140) üzere mevcut olacaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ekran düzeni değişiminin perakende kanalına, dağıtım zamanlaması işlevi üzerinden de dağıtılması gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Sales processing of the manual line charge</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">El ile satır masrafının satış işlemi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Senaryoyu POS uygulamasında gerçekleştirmek için POS kullanıcısının satış hareketini normal biçimde oluşturması, ürünleri ve diğer tüm yapılandırmaları satışa eklemesi gerekecektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Prior to collecting payment, the user should select the specific line where the charge will apply from the POS item list display and execute the <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ödeme almadan önce kullanıcının masrafın POS ögesi liste görünümünden ekleneceği belirli satırı seçmesi ve <bpt id="p1">**</bpt>Satır masrafı ekle<ept id="p1">**</ept> işlemini seçmesi gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The user will be prompted to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanıcı, bir masraf kodu seçmek ve masraf değeri girmek üzere uyarılacaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Once the user completes the process, the charge will be linked to the line and added to the order total as a line level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanıcı işlemi tamamladıktan sonra, masraf satıra bağlanacaktır ve sipariş toplamına bir satır düzeyi masrafı olarak eklenecektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The user can repeat the process to add additional line charges to other items lines on the transaction if needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanıcı, işlemi ek satır değişikliklerini diğer öge satırlarına işlem üzerine eklemek üzere tekrar edebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The same process can be applied in the call center by using the "maintain charges" feature found under the <bpt id="p1">**</bpt>Financials<ept id="p1">**</ept> drop-down menu in the <bpt id="p2">**</bpt>Sales order lines<ept id="p2">**</ept> section on the <bpt id="p3">**</bpt>Sales order<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aynı işlem, çağrı merkezinde, <bpt id="p3">**</bpt>Satış siparişi<ept id="p3">**</ept> sayfasındaki <bpt id="p2">**</bpt>Satış siparişi satırları<ept id="p2">**</ept> bölümünde bulunan <bpt id="p1">**</bpt>Finansal<ept id="p1">**</ept> açılır menüsünde "masrafları koru" özelliğini kullanarak uygulanabilir</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>This will open the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page where the user can add a new line specific charge to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu, <bpt id="p1">**</bpt>Masrafları koru<ept id="p1">**</ept> sayfasını açacaktır, burada kullanıcı işleme belirli bir yeni satır ekleyebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Additional features</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ek özellikler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Editing charges on a POS sales transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS satış işlemindeki masrafları düzenlemek</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>The <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation (142) should be added to the <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a user can view and edit or override any system-calculated or manually-created header or line-level charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Masrafları yönet<ept id="p1">**</ept> işlemi (142), <bpt id="p2">[</bpt>POS ekran düzenine<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> eklenmelidir, böylece kullanıcı sistem tarafından hesaplanan veya el ile oluşturulan başlık veya satır düzeyi masrafları görüntüleyebilir ve düzenleyebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>If the operation is not added, users will not be able to adjust the value of the charges on the POS transaction, nor will they be able to view the details of the charges such as the type of charges code tied to the charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İşlem eklenmezse, kullanıcılar POS hareketindeki masrafların değerini ayarlayamayacaktır ve masrafların türü ve masraf kodu gibi masrafa ilişkin ayrıntıları görüntülemeyecektirler.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>On the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> page in POS, the user can view both header and line-level charges details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS'taki <bpt id="p1">**</bpt>Masrafları yönet<ept id="p1">**</ept> sayfasında, kullanıcı hem başlık hem de satır düzeyi ayrıntıları görüntüleyebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The user can use the <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> function available on this page to make changes to the amount charged to a specific charges line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanıcılar bu sayfada bulunan <bpt id="p1">**</bpt>Düzenle<ept id="p1">**</ept> işlevini, belirli bir gider satırına uygulanan tutarda değişiklikler yapmak için kullanabilirler.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Once a charges line is overwritten manually, it will not be systematically recalculated unless the user initiates the <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bir masraf satırı el ile değiştirildikten sonra, kullanıcı <bpt id="p1">**</bpt>Yeniden hesapla<ept id="p1">**</ept> işlemini başlatmadığı sürece sistematik olarak yeniden hesaplanmayacaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>If the <bpt id="p1">**</bpt>Charge override reason code<ept id="p1">**</ept> has been configured on the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> setup page, the user will be prompted to provide a reason code when charges have been modified in the POS application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Masraf geçersiz kılma neden kodu<ept id="p1">**</ept>, kurulum sayfasında <bpt id="p2">**</bpt>Perakende parametreleri<ept id="p2">**</ept> içinde yapılandırılmışsa, kullanıcı masraflar POS uygulamasında değiştirilirse bir neden kodu girmek üzere uyarılır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>If reason codes have been captured for overwritten charges, a new report is also available to review and audit these overrides.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Neden kodları üzeri yazılan masraflar için yakalanmamışsa, yeni bir rapor da bu geçersiz kılmaları gözden geçirmek ve değerlendirmek için mevcut olacaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>The report can be found in <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge override history<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu rapor <bpt id="p1">**</bpt>Perakende <ph id="ph1">\&gt;</ph> Sorgular ve raporlar <ph id="ph2">\&gt;</ph> Geçersiz kılma geçmişi<ept id="p1">**</ept> içinde bulunabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Refunding charges on a POS return transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS iade hareketinde masrafları iade etmek</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>If the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>, the existing retail parameter for <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> is no longer applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Gelişmiş otomatik masrafları kullan<ept id="p1">**</ept> parametresi <bpt id="p2">**</bpt>Evet<ept id="p2">**</ept> olarak ayarlanmışsa, <bpt id="p3">**</bpt>Sevkiyat masraflarını iade et<ept id="p3">**</ept> için mevcut perakende parametresi artık uygulanamaz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>To indicate which charges should be systematically refunded to a customer when using advanced auto-charges, ensure the related charges code has been configured as <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hangi masrafların sistematik olarak bir müşteriye gelişmiş otomatik masraflar kullanılırken iade edileceğini belirtmek için ilgili masraf kodları <bpt id="p1">**</bpt>İade edilebilir<ept id="p1">**</ept> olarak <bpt id="p2">**</bpt>Masraf kodları<ept id="p2">**</ept> ayar sayfasında yapılandırılmıştır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Make sure that the settings have been synchronized to your Retail channel databases through distribution schedule processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ayarların Perakende kanalı veritabanınıza dağıtım zamanlama işleme üzerinden eşitlenmiş olduğundan emin olun.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Refunding charges on a return order transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sipariş iade hareketinde masrafları iade etmek</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Charges are not systematically refunded to <bpt id="p1">**</bpt>Return orders<ept id="p1">**</ept> created in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Masraflar sistematik olarak Perakende içinde oluşturulmuş <bpt id="p1">**</bpt>İade siparişlerine<ept id="p1">**</ept> iade edilmez.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Users are required to select the <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> option when creating the <bpt id="p2">**</bpt>Return order<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanıcıların <bpt id="p2">**</bpt>Sipariş iadesi<ept id="p2">**</ept> oluştururken <bpt id="p1">**</bpt>Masrafları kopyala<ept id="p1">**</ept> seçeneğini seçmesi gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is not selected, charges from the original sales transaction will not be automatically refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Masrafları kopyala<ept id="p1">**</ept> seçili değilse, orijinal satış işlemindeki masraflar otomatik olarak iade edilmez.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is selected, all charges will be copied to the return order and the user can manually edit or remove any charges they do not want to have refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Masrafları kopyala<ept id="p1">**</ept> seçiliyse, tüm masraflar iade siparişine kopyalanır ve kullanıcı iade edilmesini istemedikleri masrafları el ile düzenleyebilir veya kaldırabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The call center return order process currently does not acknowledge the <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Çağrı merkezi iade siparişi işlemi şu anda <bpt id="p2">**</bpt>Masraf kodları<ept id="p2">**</ept> ayarındaki <bpt id="p1">**</bpt>İade edilebilir<ept id="p1">**</ept> bayrağını tanımamaktadır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Configuring POS receipts to show charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Masrafları göstermek için POS girişlerini yapılandırmak</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>The following receipt elements have been added to the receipt line and footer to support the advanced auto-charges functionality.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Aşağıdaki giriş ögeleri giriş satırına ve altbilgisine gelişmiş otomatik masraflar işlevini desteklemek için eklenmiştir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source><bpt id="p1">**</bpt>Line Shipping Charges<ept id="p1">**</ept> – This line-level element can be used to recap specific charges codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Satır Sevkiyat Masrafları<ept id="p1">**</ept> - Bu satır düzeyi öğesi, satış satırına uygulanan belirli masraf kodlarını özetlemek için kullanılabilir.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Only charges codes that have been flagged as <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> charges on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page will be displayed here.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Yalnızca <bpt id="p2">**</bpt>Masraf kodları<ept id="p2">**</ept> sayfasındaki <bpt id="p1">**</bpt>Sevkiyat<ept id="p1">**</ept> masrafı olarak işaretlenmiş masraf kodları burada görüntülenir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source><bpt id="p1">**</bpt>Line Other Charges<ept id="p1">**</ept> – This line-level element can be used to recap any non-shipping specific charge codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Satır Diğer Masrafları<ept id="p1">**</ept> - Bu satır düzeyi öğesi, satış satırına uygulanan sevkiyatla ilgili olmayan belirli masraf kodlarını özetlemek için kullanılabilir.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>These are charges codes where the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page has not been enabled.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Bunlar, <bpt id="p2">**</bpt>Masraf kodlar<ept id="p2">**</ept> sayfasındaki <bpt id="p1">**</bpt>Sevkiyat<ept id="p1">**</ept> bayrağının etkinleştirilmediği masraf kodlarıdır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source><bpt id="p1">**</bpt>Order Shipping Charges Details<ept id="p1">**</ept> – This footer-level element displays the descriptions of the charge codes applied to the order that have been flagged as <bpt id="p2">**</bpt>Shipping<ept id="p2">**</ept> charges on the <bpt id="p3">**</bpt>Charges code<ept id="p3">**</ept> setup page.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Sipariş Sevkiyat Masrafları Ayrıntısı<ept id="p1">**</ept> - Bu altbilgi düzeyi öğe, <bpt id="p3">**</bpt>Masraf kodları<ept id="p3">**</ept> kurulum sayfasında <bpt id="p2">**</bpt>Sevkiyat<ept id="p2">**</ept> masrafı olarak işaretlenmiş masraf kodlarının açıklamalarını gösterir.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source><bpt id="p1">**</bpt>Order Shipping Charges<ept id="p1">**</ept> – This footer-level element shows the dollar value of the shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Sipariş Sevkiyat Masrafları<ept id="p1">**</ept> - Bu altbilgi düzeyi öğe, sevkiyat ile ilişkili masrafların Dolar cinsinden değerini gösterir.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source><bpt id="p1">**</bpt>Order Other Charges Details<ept id="p1">**</ept> – This footer-level element displays the description of the charges codes applied to the order that have not been flagged as shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Sipariş Diğer Masrafları Ayrıntısı<ept id="p1">**</ept> - Bu altbilgi düzeyi öğe, Masraf kodları kurulum sayfasında Sevkiyat masrafı değil olarak işaretlenmiş masraf kodlarının açıklamalarını gösterir.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source><bpt id="p1">**</bpt>Order Other Charges<ept id="p1">**</ept> – This footer-level element displays the dollar value of the other charges that are not shipping-related.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Sipariş Diğer Masraflar<ept id="p1">**</ept> - Bu altbilgi düzeyi öğe, sevkiyat ile ilişkili olmayan diğer masrafların dolar değerini gösterir.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>It is recommended that the organization also add free text fields to the receipt footer, in order to define the areas where charges will be recapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kuruluşun giriş altbilgisine serbest metin alanları eklemesi de önerilir, bu sayede masrafların özetleneceği bölgeler tanımlanır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Preventing charges from being calculated until the POS order is completed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Masrafların, POS siparişi tamamlanmadan hesaplanmasını engellemek</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Some organizations may prefer to wait until the user has finished adding all of the sales lines to the POS transaction before calculating charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bazı kuruluşlar, masrafları hesaplamadan önce kullanıcının tüm satış satırlarını POS hareketine girmesini beklemeyi tercih etmektedirler.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>To prevent calculation of charges as items are added to the POS transaction, turn on the <bpt id="p1">**</bpt>Manual charge calculation<ept id="p1">**</ept> parameter in the <bpt id="p2">**</bpt>Functionality profile<ept id="p2">**</ept> used by the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Öğeler POS hareketine eklenirken masraf öğelerinin hesaplanmasını engellemek için <bpt id="p1">**</bpt>El ile masraf hesaplaması<ept id="p1">**</ept> parametresini mağaza tarafından kullanılan <bpt id="p2">**</bpt>İşlev profili<ept id="p2">**</ept> içinde kapatın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Enabling this parameter will require the POS user to use the <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation when they have completed adding the products to the POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu parametreyi etkinleştirmek, POS kullanıcısının <bpt id="p1">**</bpt>Toplamları hesapla<ept id="p1">**</ept> işlemini, ürünleri POS hareketine eklemeyi tamamladıklarında kullanmalarını gerektirmesine neden olur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>The <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation will then trigger the calculation of any auto charges for the order header or lines as applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Toplamları hesapla<ept id="p1">**</ept> işlemi, sipariş başlığı veya satırları için otomatik masrafların hesaplanmasını tetikleyecektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Charges override reports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Masraf geçersiz kılma raporları</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>If users manually override the calculated charges or add a manual charge to the transaction, this data will available for auditing in the <bpt id="p1">**</bpt>Charge Override History<ept id="p1">**</ept> report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanıcılar hesaplanan masrafları el ile geçersiz kılarlarsa veya bir el ile masrafı harekete eklerlerse, bu veri <bpt id="p1">**</bpt>Masraf Geçersiz Kılma Geçmişi<ept id="p1">**</ept> raporunda denetleme için kullanılabilir olur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The report can be accessed from <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge Override History<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu rapor <bpt id="p1">**</bpt>Perakende <ph id="ph1">\&gt;</ph> Sorgular ve raporlar <ph id="ph2">\&gt;</ph> Masraf Geçersiz Kılma Geçmişi<ept id="p1">**</ept> üzerinden erişilebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>It is important to note that the data needed for this report is imported from the channel database into HQ through the "P" distribution schedule jobs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu rapor için ihtiyaç duyulan verinin kanal veritabanından HQ'ya "P" dağıtım zamanlama işleri üzerinden içe aktarılması gerektiğini unutmayın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Therefore, information about overrides just performed in the POS may not be immediately available on this report until this job has uploaded the store transaction data into HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu nedenle, POS içinde gerçekleştirilen geçersiz kılma hakkındaki bilgiler, bu iş mağaza hareketini HQ'ya karşıya yükleyene kadar bu raporda derhal kullanılabilir olmayabilirler.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>