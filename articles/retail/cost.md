<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="cost.md" target-language="tr-TR">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>cost.4e88df.80e7a033467c3d94d55f06daa05f99bd27e19a29.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>80e7a033467c3d94d55f06daa05f99bd27e19a29</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\cost.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Cost configuration for distributed order management (DOM)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dağıtılmış sipariş yönetimi (DOM) için maliyet yapılandırması</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes cost configuration for the distributed order management (DOM) functionality in Microsoft Dynamics 365 for Retail.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Bu konuda, Microsoft Dynamics 365 for Retail'deki dağıtılmış sipariş yönetimi (DOM) işlevi için maliyet yapılandırması açıklanmaktadır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Cost configuration for distributed order management (DOM)</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Dağıtılmış sipariş yönetimi (DOM) için maliyet yapılandırması</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kuruluşlar, bir siparişin karşılanması gereken en iyi konumu belirlemek için birden fazla maliyet bileşenini dikkate alır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Some of these cost components are shipping cost, handling cost, and packaging cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bu maliyet bileşenlerinden bazıları sevkiyat maliyeti, işleme maliyeti ve ambalaj maliyetidir.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>A combination of these costs is calculated to determine the fulfillment location.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bu maliyetlerin birleşimi, karşılama konumunun belirlenmesi için hesaplanır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When the first iteration of distributed order management (DOM) in Microsoft Dynamics 365 for Retail optimized the assignment of orders to fulfillment locations, it factored in distance only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Microsoft Dynamics 365 for Retail'de dağıtılmış sipariş yönetiminin (DOM) ilk yinelemesi siparişleri karşılama konumlarına atamayı en iyi duruma getirdiğinde, yalnızca mesafe dikkate alınıyordu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Although distance can be correlated with cost, it isn't the same as cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Mesafe maliyet ile ilişkili olabilmesine karşın maliyetle aynı değildir.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Örneğin, gece sevkiyatı yöntemi aynı mesafeye yapılan üç günlük veya yedi günlük sevkiyattan daha maliyetlidir.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Maliyet yapılandırması özelliği, perakendecilerin sipariş satırlarını karşılamak için en uygun konumu belirlemek üzere hesaplanacak ve dikkate alınacak ek maliyet bileşenlerini tanımlamasına ve yapılandırmasına olanak tanır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Maliyet bileşenleri yapılandırıldığında DOM çözücü siparişi karşılamak üzere en uygun konumu belirlemek için bu maliyet tanımlarını kullanır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>It doesn't consider the distance component as a cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Mesafe bileşenini maliyet olarak dikkate almaz.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Bununla birlikte, bileşenler yapılandırılmazsa DOM çözücü siparişi karşılamak üzere en uygun konumu belirlemek için mesafe bileşenini maliyet olarak kullanır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Set up cost components</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Maliyet bileşenlerini ayarlama</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Two major cost component types can be defined in the system: <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Other<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated">Sistemde iki ana maliyet bileşeni türü tanımlanabilir: <bpt id="p1">**</bpt>Sevkiyat<ept id="p1">**</ept> ve <bpt id="p2">**</bpt>Diğer<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Both cost component types support multiple calculation bases, as shown in the following table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Her iki maliyet bileşeni türü de aşağıdaki tabloda gösterildiği gibi çoklu hesaplama esaslarını destekler.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Cost component type</source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match">Maliyet bileşeni türü</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Calculation basis</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Hesaplama esası</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Shipping</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Sevkiyat</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Simple</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Basit</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Tiered</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Katmanlı</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Other</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Diğer</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Sales order</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Satış siparişi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Sales line</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Satış satırı</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Location</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Konum</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Shipping cost component type</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Sevkiyat maliyeti bileşeni türü</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and a calculation basis for shipping costs.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bu bölümde, <bpt id="p1">**</bpt>Sevkiyat<ept id="p1">**</ept> maliyeti bileşeni türü ve sevkiyat maliyetleri için hesaplama esası birleşiminin nasıl ayarlanacağı açıklanmaktadır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>It also explains how the DOM solver uses each combination.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ayrıca, DOM çözücünün her bir birleşimi nasıl kullandığı da açıklanmaktadır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Cost component type = Shipping and Calculation basis = Simple</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Maliyet bileşeni türü = Sevkiyat ve Hesaplama esası = Basit</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Simple<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Sevkiyat<ept id="p1">**</ept> maliyeti bileşeni türü ve <bpt id="p2">**</bpt>Basit<ept id="p2">**</ept> hesaplama esası birlikte kullanılırsa bir teslimat şekline ait sevkiyat maliyeti, sabit maliyeti veya mesafeyi temel alır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must set up the following fields for this combination:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bu birleşim için aşağıdaki alanları ayarlamanız gerekir:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Maliyet faktörü<ept id="p1">**</ept>: Maliyet faktörü için benzersiz bir tanımlayıcı girin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source><target logoport:matchpercent="78" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Açıklama<ept id="p1">**</ept>: Maliyet faktörünün adını ve açıklamasını girin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Başlangıç tarihi<ept id="p1">**</ept> ve <bpt id="p2">**</bpt>Bitiş tarihi<ept id="p2">**</ept>: Bu alanları, maliyet faktörünü belirli bir tarih aralığı için sınırlandırmak amacıyla kullanabilirsiniz.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bu alanları boş bırakırsanız maliyet faktörü belirsiz bir dönem için geçerli olur.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Etkin<ept id="p1">**</ept>: Maliyet faktörünün etkin olup olmadığını gösterir.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">DOM yalnızca karşılama profiliyle ilişkili olan etkin maliyet faktörlerini dikkate alır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Şirket<ept id="p1">**</ept>: Maliyet faktörünün yapılandırıldığı tüzel kişiliği belirtin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>All lines of the calculation criteria must be for the same legal entity.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Hesaplama ölçütlerinin tüm satırları aynı tüzel kişilik için olmalıdır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Teslimat şekilleri<ept id="p1">**</ept>: Maliyetin yapılandırıldığı teslimat şekillerini belirtin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Hesaplama türü<ept id="p1">**</ept>: Maliyetin belirli bir teslimat şekli için nasıl hesaplanacağını belirtin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Two calculation types are supported:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">İki hesaplama türü desteklenir:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Sabit<ept id="p1">**</ept>: Teslimat şekli olarak düz maliyet kullanılır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bu hesaplama türünü seçerseniz <bpt id="p1">**</bpt>Maliyet<ept id="p1">**</ept> alanı düz maliyeti tanımlar.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Per-distance unit<ept id="p1">**</ept> – The cost for the mode of delivery is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Mesafe başına birim<ept id="p1">**</ept>: Teslimat şeklinin maliyeti, <bpt id="p2">**</bpt>Maliyet<ept id="p2">**</ept> alanında belirtilen maliyet değeri ile teslimat adresi ve konumlar arasındaki mesafe çarpılarak hesaplanır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Maliyet<ept id="p1">**</ept>: Teslimat şeklinin maliyetini hesaplamak için <bpt id="p2">**</bpt>Hesaplama türü<ept id="p2">**</ept> alanıyla birlikte kullanılan maliyet değerini belirtin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Cost component type = Shipping and Calculation basis = Tiered</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Maliyet bileşeni türü = Sevkiyat ve Hesaplama esası = Katmanlı</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Tiered<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="95" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Sevkiyat<ept id="p1">**</ept> maliyeti bileşeni türü ve <bpt id="p2">**</bpt>Katmanlı<ept id="p2">**</ept> hesaplama esası birlikte kullanılırsa bir teslimat şekline ait sevkiyat maliyeti, sabit maliyeti veya mesafeyi temel alır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>However, in this combination, the distance is based on a tiered range of distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ancak bu birleşimde, mesafe katmanlı bir mesafe aralığını temel alır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Bu birleşim için aşağıdaki alanları ayarlamanız gerekir:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Maliyet faktörü<ept id="p1">**</ept>: Maliyet faktörü için benzersiz bir tanımlayıcı girin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Açıklama<ept id="p1">**</ept>: Maliyet faktörünün adını ve açıklamasını girin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>Default cost<ept id="p1">**</ept> – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Varsayılan maliyet<ept id="p1">**</ept>: Teslimat adresi ile konum arasındaki mesafe teslimat şekline ilişkin katmanlı mesafelerden herhangi birine denk düşmezse, teslimat şekli için kullanılacak maliyeti belirtin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Başlangıç tarihi<ept id="p1">**</ept> ve <bpt id="p2">**</bpt>Bitiş tarihi<ept id="p2">**</ept>: Bu alanları, maliyet faktörünü belirli bir tarih aralığı için sınırlandırmak amacıyla kullanabilirsiniz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Bu alanları boş bırakırsanız maliyet faktörü belirsiz bir dönem için geçerli olur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Etkin<ept id="p1">**</ept>: Maliyet faktörünün etkin olup olmadığını gösterir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM yalnızca karşılama profiliyle ilişkili olan etkin maliyet faktörlerini dikkate alır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Şirket<ept id="p1">**</ept>: Maliyet faktörünün yapılandırıldığı tüzel kişiliği belirtin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>All lines of the calculation criteria must be for the same legal entity.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Hesaplama ölçütlerinin tüm satırları aynı tüzel kişilik için olmalıdır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Teslimat şekilleri<ept id="p1">**</ept>: Maliyetin yapılandırıldığı teslimat şekillerini belirtin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>Distance type<ept id="p1">**</ept> – Specify whether the tiered distance definition is an aerial distance or a road distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Mesafe türü<ept id="p1">**</ept>: Katmanlı mesafe tanımının bir havayolu mesafesi mi yoksa karayolu mesafesi mi olduğunu belirtin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>Distance units<ept id="p1">**</ept> – Specify the unit that the tiered distance is measured in.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Mesafe birimleri<ept id="p1">**</ept>: Katmanlı mesafenin ölçüldüğü birimi belirtin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Distance from<ept id="p1">**</ept> – Specify the start range for the tiered distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Başlangıçtan mesafe<ept id="p1">**</ept>: Katmanlı mesafe için başlangıç aralığını belirtin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>Distance to<ept id="p1">**</ept> – Specify the end range for the tiered distance.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Bitişe mesafe<ept id="p1">**</ept>: Katmanlı mesafe için bitiş aralığını belirtin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Hesaplama türü<ept id="p1">**</ept>: Maliyetin belirli bir teslimat şekli ve katmanlı mesafe için nasıl hesaplanacağını belirtin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Two calculation types are supported:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">İki hesaplama türü desteklenir:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Sabit<ept id="p1">**</ept>: Teslimat şekli olarak düz maliyet kullanılır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Bu hesaplama türünü seçerseniz <bpt id="p1">**</bpt>Maliyet<ept id="p1">**</ept> alanı düz maliyeti tanımlar.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Per distance unit<ept id="p1">**</ept> – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Mesafe başına birim<ept id="p1">**</ept>: Teslimat şeklinin ve katmanlı mesafenin maliyeti, <bpt id="p2">**</bpt>Maliyet<ept id="p2">**</ept> alanında belirtilen maliyet değeri ile teslimat adresi ve konumlar arasındaki mesafe çarpılarak hesaplanır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Maliyet<ept id="p1">**</ept>: Teslimat şeklinin maliyetini hesaplamak için <bpt id="p2">**</bpt>Hesaplama türü<ept id="p2">**</ept> alanıyla birlikte kullanılan maliyet değerini belirtin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>When you define tiered distances, the system validates that there are no missing or overlapping distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Katmanlı mesafeler tanımladığınızda, sistem eksik veya çakışan mesafeler olmadığını doğrular.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The distance type that is used for a mode of delivery must be the same across all the tiered distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bir teslimat şekli için kullanılan mesafe türü, tüm katmanlı mesafelerde aynı olmalıdır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Other cost component type</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Diğer maliyet bileşeni türü</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and an other cost type for non-shipping costs.</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match">Bu bölümde, <bpt id="p1">**</bpt>Diğer<ept id="p1">**</ept> maliyeti bileşeni türü ve sevkiyat dışı maliyetler için diğer maliyet türü birleşiminin nasıl ayarlanacağı açıklanmaktadır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>It also explains how the DOM solver uses each combination.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Ayrıca, DOM çözücünün her bir birleşimi nasıl kullandığı da açıklanmaktadır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Cost component type = Other and Other cost type = Sales order</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Maliyet bileşeni türü = Diğer ve Diğer maliyet türü = Satış siparişi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales order<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order level.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Diğer<ept id="p1">**</ept> maliyet bileşeni türü ile <bpt id="p2">**</bpt>Satış siparişi<ept id="p2">**</ept> diğer maliyet türü satış siparişi düzeyindeki sevkiyat dışı maliyetlerin tanımlanması için kullanılır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Bu birleşim için aşağıdaki alanları ayarlamanız gerekir:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Maliyet faktörü<ept id="p1">**</ept>: Maliyet faktörü için benzersiz bir tanımlayıcı girin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Açıklama<ept id="p1">**</ept>: Maliyet faktörünün adını ve açıklamasını girin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Başlangıç tarihi<ept id="p1">**</ept> ve <bpt id="p2">**</bpt>Bitiş tarihi<ept id="p2">**</ept>: Bu alanları, maliyet faktörünü belirli bir tarih aralığı için sınırlandırmak amacıyla kullanabilirsiniz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Bu alanları boş bırakırsanız maliyet faktörü belirsiz bir dönem için geçerli olur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Etkin<ept id="p1">**</ept>: Maliyet faktörünün etkin olup olmadığını gösterir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM yalnızca karşılama profiliyle ilişkili olan etkin maliyet faktörlerini dikkate alır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Maliyet<ept id="p1">**</ept>: Satış siparişi düzeyinde sevkiyat dışı bir maliyetin maliyet değerini belirtin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Cost component type = Other and Other cost type = Sales line</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Maliyet bileşeni türü = Diğer ve Diğer maliyet türü = Satış satırı</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales line<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order line level.</source><target logoport:matchpercent="93" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Diğer<ept id="p1">**</ept> maliyet bileşeni türü ile <bpt id="p2">**</bpt>Satış satırı<ept id="p2">**</ept> diğer maliyet türü satış satırı düzeyindeki sevkiyat dışı maliyetlerin tanımlanması için kullanılır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Bu birleşim için aşağıdaki alanları ayarlamanız gerekir:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Maliyet faktörü<ept id="p1">**</ept>: Maliyet faktörü için benzersiz bir tanımlayıcı girin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Açıklama<ept id="p1">**</ept>: Maliyet faktörünün adını ve açıklamasını girin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Başlangıç tarihi<ept id="p1">**</ept> ve <bpt id="p2">**</bpt>Bitiş tarihi<ept id="p2">**</ept>: Bu alanları, maliyet faktörünü belirli bir tarih aralığı için sınırlandırmak amacıyla kullanabilirsiniz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Bu alanları boş bırakırsanız maliyet faktörü belirsiz bir dönem için geçerli olur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Etkin<ept id="p1">**</ept>: Maliyet faktörünün etkin olup olmadığını gösterir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM yalnızca karşılama profiliyle ilişkili olan etkin maliyet faktörlerini dikkate alır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order line level.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Maliyet<ept id="p1">**</ept>: Satış satırı düzeyinde sevkiyat dışı bir maliyetin maliyet değerini belirtin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Cost component type = Other and Other cost type = Location</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Maliyet bileşeni türü = Diğer ve Diğer maliyet türü = Konum</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Location<ept id="p2">**</ept> other cost type is used to define non-shipping costs for a group of locations or an individual location.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Diğer<ept id="p1">**</ept> maliyet bileşeni türü ile <bpt id="p2">**</bpt>Konum<ept id="p2">**</ept> diğer maliyet türünün birleşimi, bir konum grubu veya tek bir konum için sevkiyat dışı maliyetleri tanımlamak amacıyla kullanılır.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Bu birleşim için aşağıdaki alanları ayarlamanız gerekir:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Maliyet faktörü<ept id="p1">**</ept>: Maliyet faktörü için benzersiz bir tanımlayıcı girin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Açıklama<ept id="p1">**</ept>: Maliyet faktörünün adını ve açıklamasını girin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Başlangıç tarihi<ept id="p1">**</ept> ve <bpt id="p2">**</bpt>Bitiş tarihi<ept id="p2">**</ept>: Bu alanları, maliyet faktörünü belirli bir tarih aralığı için sınırlandırmak amacıyla kullanabilirsiniz.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Bu alanları boş bırakırsanız maliyet faktörü belirsiz bir dönem için geçerli olur.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Etkin<ept id="p1">**</ept>: Maliyet faktörünün etkin olup olmadığını gösterir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM yalnızca karşılama profiliyle ilişkili olan etkin maliyet faktörlerini dikkate alır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">**</bpt>Fulfillment group<ept id="p1">**</ept> – Specify the group of locations that the non-shipping cost is defined for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Karşılama grubu<ept id="p1">**</ept>: Sevkiyat dışı maliyetin tanımlandığı konum gruplarını belirtin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">**</bpt>Fulfillment location<ept id="p1">**</ept> – Specify the location that the non-shipping cost is defined for.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Karşılama konumu<ept id="p1">**</ept>: Sevkiyat dışı maliyetin tanımlandığı konumu belirtin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Konum tabanlı hesaplama ölçütleri için aynı satırda bir karşılama grubu ve karşılama konumu belirtemezsiniz.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Maliyet<ept id="p1">**</ept>: Karşılama grubu düzeyi veya karşılama konumu düzeyinde sevkiyat dışı maliyetin maliyet değerini belirtin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">DOM'ın çalıştırıldığında bu maliyetleri dikkate alması için maliyet faktörünü ilgili karşılama profiline eklemeniz gerekir.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>