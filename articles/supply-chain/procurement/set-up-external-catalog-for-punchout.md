<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="set-up-external-catalog-for-punchout.md" target-language="tr-TR">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>set-up-external-catalog-for-punchout.474d96.39baa331120d765543c3cf662ce53d2bcfe404ab.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>39baa331120d765543c3cf662ce53d2bcfe404ab</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\supply-chain\procurement\set-up-external-catalog-for-punchout.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Set up an external catalog for PunchOut eProcurement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PunchOut eProcurement için harici katalog ayarlama</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the use of an  external catalog or punchout catalog to collect quote information from a vendor and add it to a requisition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu konu, bir satıcıdan teklif bilgileri toplamak ve bunu talebe eklemek için harici katalog veya punchout (çıkış) kataloğu kullanımını açıklar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Set up an external catalog for PunchOut eProcurement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PunchOut eProcurement için harici katalog ayarlama</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>By using the external catalog, you can ensure that the product and price information that you subsequently process in Dynamics 365 for Finance and Operations July 2017 is accurate and up to date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici katalog kullanarak, daha sonra Dynamics 365 for Finance and Operations Temmuz 2017'de işleyeceğiniz fiyat ve ürün bilgilerinin doğru ve güncel olmasını sağlayabilirsiniz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The requisition can then be approved and converted to a purchase order and an order can be placed at the vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Talep daha sonra onaylanıp bir satın alma siparişine dönüştürülebilir ve sipariş satıcıya yerleştirilebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When the external catalog is set up and an employee is preparing a requisition, there will be an option to redirect to an external site, the external catalog, and return the shopping basket that was created at the external site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici katalog ayarlandığında ve bir çalışan bir talep hazırladığında, harici siteye, harici kataloğa yönlendirme ve harici sitede oluşturulan alışveriş sepetine geri dönme seçeneği olacaktır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This communication is based on the cXML protocol and it has to be set up between the systems of the buying and the selling organization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu iletişim cXML protokolünü temel alır ve satınalma ve satış kuruluşunun sistemleri arasında ayarlanmalıdır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To set up the communication, your vendor has to provide pieces of information for you to use in the configuraiton of the external catalog such as Identity, domain of the buyers company, for example, "DUNS" and "DUNS number", credentials, and the URL to reach the vendors catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İletişimi kurmak için, satıcınızın kimlik, satınalıcı şirket etki alanı (örneğin "DUNS" veya "DUNS numarası"), kullanıcı kimlik bilgileri ve satıcı kataloglarına erişmek için URL gibi bazı bilgileri harici katalog yapılandırmasında kullanmanız için size vermesi gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Setting up an external catalog</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici bir katalog ayarlama</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The external catalog should enable an employee who enters a purchase requisition to be redirected to an external site to select products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici katalog satınalma talebini giren çalışanın ürünleri seçmek için harici siteye yönlendirilmesini sağlamalıdır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The products that the employee selects from the external catalog are returned to Dynamics 365 for Finance and Operations with up-to-date price information and from here, they can be added to the purchase requisition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Çalışanın harici katalogdan seçtiği ürünler güncelleştirilmiş fiyat bilgileriyle birlikte Dynamics 365 for Finance and Operations'a döndürülür ve buradan satınalma talebine eklenebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The intention is not to enable employees to place an order on the external site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Amaç çalışanın harici siteye bir sipariş vermesini sağlamak değildir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>When setting up the external catalog, you need to make sure that the purpose of the site that can be accessed by the external catalog is to collect quote information and not to place a real order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici kataloğu ayarlarken, harici katalog tarafından erişilen sitenin amacının gerçek bir sipariş yerleştirmek değil teklif bilgilerini toplamak olduğundan emin olmanız gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>To set up an external vendor catalog, complete the following tasks:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici bir satıcı kataloğu ayarlamak için, aşağıdaki görevleri tamamlamanız gerekir:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Set up a procurement category hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bir tedarik kategori hiyerarşisi ayarlayın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For more information, see <bpt id="p1">[</bpt>Set up policies for procurement category hierarchies<ept id="p1">](tasks/set-up-policies-procurement-category-hierarchies.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Daha fazla bilgi için bkz. <bpt id="p1">[</bpt>Tedarik kategorisi hiyerarşileri için ilkeleri ayarlama<ept id="p1">](tasks/set-up-policies-procurement-category-hierarchies.md)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Register the vendor in Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satıcıyı Finance and Operations'a kaydedin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Before you can set up configurations to access an external vendor’s catalog, you must set up the vendor and the vendor contact in Microsoft Dynamics 365.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici satıcı kataloğuna erişmek için yapılandırmalarını ayarlamadan önce Microsoft Dynamics 365'te satıcıyı ve satıcı ilgili kişisini ayarlamanız gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The external catalog’s vendor must also be added to the selected procurement category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici kataloğun satıcısı seçilen tedarik kategorisine de eklenmelidir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For more information about registering vendors in Microsoft Dynamics 365, see <bpt id="p1">[</bpt>Manage vendor collaboration users<ept id="p1">](manage-vendor-collaboration-users.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satıcıları Microsoft Dynamics 365'te kaydetme hakkında daha fazla bilgi için bkz. <bpt id="p1">[</bpt>Satıcı iş birliği kullanıcılarını yönetme<ept id="p1">](manage-vendor-collaboration-users.md)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>For information about how to assign vendors to a procurement category, see <bpt id="p1">[</bpt>Approve vendors for specific procurement categories<ept id="p1">](tasks/approve-vendors-specific-procurement-categories.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satıcıları bir tedarik kategorisine atama konusunda bilgi için bkz. <bpt id="p1">[</bpt>Belirli tedarik kategorileri için satıcıları onaylama<ept id="p1">](tasks/approve-vendors-specific-procurement-categories.md)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Make sure that the units of measure and the currency that the vendor uses are set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satıcının kullandığı para birimi ve ölçü birimlerinin ayarlandığından emin olun.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>For information about how to create a unit of measure, see <bpt id="p1">[</bpt>Manage units of measure<ept id="p1">](../pim/tasks/manage-unit-measure.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bir ölçü birimi oluşturma hakkında bilgi için bkz. <bpt id="p1">[</bpt>Ölçü birimleri yönetme<ept id="p1">](../pim/tasks/manage-unit-measure.md)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Configure the external vendor catalog by using the requirements for your vendor’s external catalog site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici satıcı kataloğunu satıcınızın harici katalog sitesi gereksinimlerini kullanarak yapılandırın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For more details about this task, see <bpt id="p1">[</bpt>Configure the external vendor catalog<ept id="p1">](#configure-the-external-vendor-catalog)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu görev hakkında daha fazla bilgi için bkz. <bpt id="p1">[</bpt>Harici satıcı kataloğu yapılandırma<ept id="p1">](#configure-the-external-vendor-catalog)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Test the vendor’s external catalog configurations to verify that the settings are valid and that you can access the vendor’s external catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ayarlarının geçerli olduğunu ve satıcının harici kataloğuna erişebildiğinizi doğrulamak için satıcının harici katalog yapılandırmalarını test edin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Use the <bpt id="p1">**</bpt>Validate settings<ept id="p1">**</ept> action to validate the request setup message that you’ve defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tanımladığınız talep kurulumu iletisini doğrulamak için <bpt id="p1">**</bpt>Ayarları doğrula<ept id="p1">**</ept> eylemini kullanın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>This message should cause the vendors external catalog site to be opened in a browser window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu ileti satıcının harici katalog sitesinin bir tarayıcı penceresinde açılmasına neden olmalıdır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>During validation, you can’t order items and services from the vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Doğrulama sırasında satıcıdan ürün veya hizmet sipariş edemezsiniz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>To order items and services, you must access the vendor’s catalog from a purchase requisition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Madde veya hizmet sipariş etmek için satıcının kataloğuna bir satınalma talebinden erişmeniz gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Activate the external catalog by using the <bpt id="p1">**</bpt>Activate catalog<ept id="p1">**</ept> button on the <bpt id="p2">**</bpt>External catalogs<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici kataloğu <bpt id="p2">**</bpt>Harici kataloglar<ept id="p2">**</ept> sayfasındaki <bpt id="p1">**</bpt>Kataloğu etkinleştir<ept id="p1">**</ept> düğmesini kullanarak etkinleştirin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The external catalog must be activated before employees can use it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Çalışanların kullanabilmesi için harici kataloğun etkinleştirilmesi gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>You can inactivate the external catalog at any time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Herhangi bir zamanda harici kataloğu devre dışı bırakabilirsiniz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Configure the external vendor catalog</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici satıcı kataloğunu yapılandırma</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>This section gives more details about task 4 in the preceding section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu bölüm önceki bölümdeki görev 4 hakkında daha fazla ayrıntı içerir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Enter a name and description for the vendor’s external catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satıcının harici kataloğu için bir ad ve açıklama girin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The name that you enter will appear on the cart that represents the external catalog that is shown to employees who creates a requisition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Girdiğiniz ad, bir talep oluşturan çalışanlara gösterilen harici kataloğu temsil eden alışveriş sepetinde görünecektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Employees can click on the cart to open the catalog on the vendor’s external catalog site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Çalışanlar satıcının harici katalog sitesindeki kataloğu açmak için sepete tıklayabilirler.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Add an image by using the<bpt id="p1"> **</bpt>External catalog image<ept id="p1">**</ept> action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1"> **</bpt>Harici katalog görüntüsü<ept id="p1">**</ept> eylemini kullanarak bir resim ekleyin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>The image will appear on the cart that represents the external catalog that is shown to employees who create a requisition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Resim, bir talep oluşturan çalışanlara gösterilen harici kataloğu temsil eden alışveriş sepetinde görünecektir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Note that the image’s width and height must be equal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Resmin genişliğinin ve yüksekliğinin eşit olması gerektiğini unutmayın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Otherwise the image won’t be displayed correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aksi halde resim düzgün görüntülenmez.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Select whether the vendor’s external catalog website should appear in the same browser window as the one where the employee has created the requisition, or if it should open in a new window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satıcının harici katalog web sitesinin çalışanın talebi oluşturduğu tarayıcı penceresinde mi görüntüleneceğini yoksa yeni bir pencerede mi açılacağını belirleyin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Select the vendor for the catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Katalog için satıcıyı seçin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In the <bpt id="p1">**</bpt>Legal entities<ept id="p1">**</ept> list, there is a row for each legal entity where the vendor is set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Tüzel kişilikler<ept id="p1">**</ept> listesinde, satıcının ayarlandığı her tüzel kişilik için bir satır bulunur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To allow users to request products directly from the vendor’s catalog in some legal entities but not others, you can use the <bpt id="p1">**</bpt>Prevent access<ept id="p1">**</ept> or <bpt id="p2">**</bpt>Allow access<ept id="p2">**</ept> button for each legal entity where you want the catalog to be or not to be available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kullanıcıların nazı tüzel kişiliklerde ürünleri doğrudan satıcının kataloğundan talep etmelerine olanak tanımak ancak bazı tüzel kişiliklerde buna izin vermemek üzere, kataloğun kullanılabilir veya kullanılamaz olmasını istediğiniz her tüzel kişilik için <bpt id="p1">**</bpt>Erişimi engelle<ept id="p1">**</ept> veya <bpt id="p2">**</bpt>Erişime izin ver<ept id="p2">**</ept> düğmesini kullanılabilirsiniz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In the <bpt id="p1">**</bpt>Default expiration (Days)<ept id="p1">**</ept> field, enter the number of days that a quotation received from the external catalog is valid and can be used to purchase from the external vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Varsayılan süre sonu (Gün)<ept id="p1">**</ept> alanında, harici katalogdan alınan bir teklifin geçerli olacağı ve harici satıcıdan satınalmak için kullanılabileceği gün sayısını girin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>When a quotation is created and retrieved from the vendor’s external catalog site, the quotation is valid as of the current system date and remains valid for the number of days that you enter in this field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bir teklif oluşturulduğunda ve satıcının harici katalog sitesinden alındığında, teklif geçerli sistem tarihi itibarıyla geçerli olur bu alana girdiğiniz gün sayısı boyunca geçerli kalır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Click the <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> button to start mapping the procurement categories to the external catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tedarik kategorilerini harici katalogla eşleştirmek için <bpt id="p1">**</bpt>Ekle<ept id="p1">**</ept> düğmesini tıklayın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source> Then, in the Category name list, select a category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"> Ardından Kategori adı listesinden bir kategori seçin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The list of categories is a superset of procurement categories that the vendor has been mapped to in all the legal entities that are set up for the vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kategori listesi, satıcının satıcı için ayarlanan tüm tüzel kişiliklerde eşlendiği bir tedarik kategorileri üst kümesidir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Procurement policies are used to allow or restrict access to categories for the buying legal entity or receiving operating unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tedarik ilkeleri, satın alan bir tüzel kişilik veya alan işletme birimi için kategorilere erişim izni vermek veya erişimi engellemek için kullanılır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source> Punchout to an external catalog requires that access be allowed to at least one of the procurement categories that is mapped to the catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"> Harici bir kataloğa çıkış, erişime katalogla eşlenen en az bir tedarik kategorisi için izin verilmiş olmasını gerektirir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Set up the cXML setup request message that will be sent to the vendor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satıcıya gönderilecek cXML kurulum talebi iletisini ayarlayın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The automatically generated message format is the minimal template that is required in order to start a session.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Otomatik olarak oluşturulan ileti biçimi, bir oturumu başlatmak için gerekli olan minimum şablondur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Fill in values for the tags.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Etiketler için değerleri girin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>At any time, you can reload the system-generated message template by clicking <bpt id="p1">**</bpt>Restore message format<ept id="p1">**</ept>.<ph id="ph1"> </ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İstediğiniz zaman, sistem tarafından oluşturulan ileti şablonunu <bpt id="p1">**</bpt>İleti biçimi geri yükle<ept id="p1">**</ept><ph id="ph1"> </ph> üzerine tıklayarak yeniden yükleyebilirsiniz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Note that if you restore the message format, the current message will be replaced by the automatically generated message format, which has empty tags.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İleti biçimini geri yüklerseniz, geçerli iletinin otomatik olarak oluşturulan ve etiketleri boş olan mesaj biçimiyle değiştirileceğini unutmayın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>cXML setup message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">cXML kurulumu iletisi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Below you can find a description of the tags that are included in the template:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aşağıda şablonda bulunan etiketlerin açıklamasını bulabilirsiniz:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Alan</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Açıklama</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>&lt; Header &gt;&lt; From &gt;&lt; Credential domain=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; From &gt;&lt; Credential domain=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The domain of the buyer’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satın alıcı şirketinin etki alanı.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>&lt; Header &gt;&lt; From &gt;&lt; Credential&gt;&lt; Identity &gt;&lt; /Identity &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; From &gt;&lt; Credential&gt;&lt; Identity &gt;&lt; /Identity &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The identity of the buyer’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satın alıcı şirketinin kimliği.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>&lt; Header &gt;&lt; To &gt;&lt; Credential domain=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; To &gt;&lt; Credential domain=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The domain of the vendor’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satıcı şirketinin etki alanı.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>&lt; Header &gt;&lt; To &gt;&lt; Credential&gt;&lt; Identity &gt;&lt; /Identity&gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; To &gt;&lt; Credential&gt;&lt; Identity &gt;&lt; /Identity&gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The identity of the vendor’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satıcı şirketinin kimliği.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>&lt; Header &gt;&lt; Sender &gt;&lt; Credential domain=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; Sender &gt;&lt; Credential domain=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The domain of the buyer’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satın alıcı şirketinin etki alanı.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>&lt; Header &gt;&lt; Sender &gt;&lt; Credential &gt;&lt; Identity &gt;&lt; /Identity&gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; Sender &gt;&lt; Credential &gt;&lt; Identity &gt;&lt; /Identity&gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>The identity of the buyer’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satın alıcı şirketinin kimliği.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>&lt; Header &gt;&lt; Sender &gt;&lt; Credential &gt;&lt; SharedSecret &gt;&lt; /SharedSecret &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Header &gt;&lt; Sender &gt;&lt; Credential &gt;&lt; SharedSecret &gt;&lt; /SharedSecret &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The shared secret for the buyer’s company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Alıcının şirketi için paylaşılan gizli kod.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>&lt; Request deploymentMode=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Request deploymentMode=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The test or production deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Test veya üretim dağıtımı.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>&lt; Request &gt;&lt; PunchOutSetupRequest &gt;&lt; SupplierSetup &gt;&lt; URL &gt;&lt; /URL&gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; Request &gt;&lt; PunchOutSetupRequest &gt;&lt; SupplierSetup &gt;&lt; URL &gt;&lt; /URL&gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>The URL of the vendor’s punchout endpoint.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satıcının çıkış uç noktası URL'si.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Extrinsic elements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İkincil öğeler</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>An extrinsic element is additional information, such as a user name that is based on a user that punches out. The extrinsic element is set when the punchout occurs and it can be sent in the request setup message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İkincil öğe, çıkış yapan kullanıcının adına dayanan kullanıcı adı gibi bir ek bilgidir. İkincil öğe, çıkış yapma gerçekleştiğinde ayarlanır ve talep kurulum iletisinde gönderilebilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Your vendor could have a requirement for receiving an extrinsic element in the setup request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Satıcınızın kurulum isteğinde bir ikincil öğe almak gibi bir gereksinimi olabilir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>In that case, you should add the extrinsic element to the list of extrinsic elements in the <bpt id="p1">**</bpt>Message format<ept id="p1">**</ept> section of the <bpt id="p2">**</bpt>External catalog<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu durumda, <bpt id="p2">**</bpt>Harici katalog<ept id="p2">**</ept> sayfasının <bpt id="p1">**</bpt>İleti biçimi<ept id="p1">**</ept> bölümündeki ikincil öğeler listesine ikincil öğe eklemeniz gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Specify a name for the extrinsic element that the vendor can recognize and map it to a value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İkincil öğe için satıcının tanıyabileceği ve bir değerle eşleyebileceği için bir ad belirtin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>The options for values are: User name, User email, or Random value.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Değerler için seçenekler şunlardır: Kullanıcı adı, Kullanıcı e-postası veya Rasgele değer.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>For more information about the cXML protocol, see the <bpt id="p1">[</bpt>cXML.org website<ept id="p1">](http://cxml.org/)</ept>.</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match">CXML protokolü hakkında daha fazla bilgi için bkz: <bpt id="p1">[</bpt>cXML.org websitesi<ept id="p1">](http://cxml.org/)</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Post back message</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Geri gönderme iletisi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>The post back message is the message that is received from the vendor when the user checks out from the external site and returns to Finance and Operations.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Geri gönderme iletisi, kullanıcı harici siteden çıkış yapıp Finance and Operations'a döndüğünde satıcı tarafından gönderilen iletidir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Post back messages can’t be configured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Geri gönderme iletileri yapılandırılamaz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>The messages are based on the cXML protocol definition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İletiler cXML protokolü tanımını temel alır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source> Here is the information that can be part of the post back message that is received on a requisition line:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"> Bir talep satırında alınan geri gönderme iletisinin parçası olabilecek bilgiler aşağıda verilmektedir:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Message received from vendor</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">İleti satıcıdan alındı</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Copied to requisition line in Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations'da istek satırına kopyalandı</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>&lt; ItemIn quantity=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemIn quantity=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Quantity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Miktar</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>&lt; ItemIn&gt;&lt; ItemID &gt;&lt; SupplierPartID &gt;&lt; /SupplierPartID &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemIn&gt;&lt; ItemID &gt;&lt; SupplierPartID &gt;&lt; /SupplierPartID &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>External item ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici madde kodu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>&lt; ItemDetail&gt;&lt; UnitPrice &gt;&lt; Money currency=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail&gt;&lt; UnitPrice &gt;&lt; Money currency=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Currency</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Para birimi</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>&lt; ItemDetail &gt;&lt; UnitPrice &gt;&lt; Money &gt;&lt; /Money &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; UnitPrice &gt;&lt; Money &gt;&lt; /Money &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Unit price</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Birim fiyatı</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>&lt; ItemDetail &gt;&lt; Description ShortName=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; Description ShortName=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Product name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ürün adı</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>&lt; ItemDetail &gt;&lt; Description &gt;&lt; /Description &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; Description &gt;&lt; /Description &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Included in item description; Product name if ShortName is not specified.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Madde açıklamasına dahil edilir; ShortName belirtilmediyse Ürün adı.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>&lt; ItemDetail &gt;&lt; UnitOfMeasure &gt;&lt; /UnitOfMeasure &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; UnitOfMeasure &gt;&lt; /UnitOfMeasure &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Unit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Birim</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>&lt; ItemDetail &gt;&lt; Classification &gt;&lt; /Classification &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; Classification &gt;&lt; /Classification &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Included in item description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Madde açıklamasına dahil edilir</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>&lt; ItemDetail &gt;&lt; Classification domain=”” &gt;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">&lt; ItemDetail &gt;&lt; Classification domain=”” &gt;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Included in item description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Madde açıklamasına dahil edilir</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Delete an external catalog</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici bir kataloğu silme</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Delete an external catalog with the Delete action on the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici bir kataloğu sayfadaki Silme eylemiyle silin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>If a product from the external vendor catalog has been requested, the external vendor catalog cannot be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici satıcı kataloğundaki bir ürünün istenmiş olması durumunda, harici satıcı kataloğu silinemez.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Instead, the status of the external vendor catalog is set to inactive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bunun yerine, harici satıcı kataloğu durumu etkin değil olarak ayarlanır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>If you want to remove access to the external vendor’s catalog site, but not delete it, change the external catalog status to Inactive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Harici satıcı kataloğu sitesine erişimi kaldırmak istiyor ancak harici kataloğu silmek istemiyorsanız, harici katalog durumunu etkin değil olarak değiştirin.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>