---
title: PunchOut e-procurement için harici katalog ayarlama
description: Bu konu, bir satıcıdan teklif bilgileri toplamak ve bunu talebe eklemek için harici katalog veya PunchOut (çıkış) kataloğu kullanımını açıklar.
author: RichardLuan
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchVendorPortalRequests, CatExternalCatalogConfiguration, CatCXMLCartLogList
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f6e551f9d3d181674595e945bf1fb4c62a70ed5
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016389"
---
# <a name="set-up-an-external-catalog-for-punchout-e-procurement"></a>PunchOut e-procurement için harici katalog ayarlama

[!include [banner](../includes/banner.md)]

Harici katalog kullanarak, daha sonra Supply Chain Management'ta işleyeceğiniz fiyat ve ürün bilgilerinin doğru ve güncel olmasını sağlayabilirsiniz. Talep daha sonra onaylanıp bir satın alma siparişine dönüştürülebilir ve sipariş satıcıya yerleştirilebilir.

Harici katalog ayarlandığında ve bir çalışan bir talep hazırladığında, harici siteye, harici kataloğa yönlendirme ve harici sitede oluşturulan alışveriş sepetine geri dönme seçeneği olacaktır. Bu iletişim cXML protokolünü temel alır ve satınalma ve satış kuruluşunun sistemleri arasında ayarlanmalıdır.

İletişimi kurmak için, satıcınızın kimlik, satınalıcı şirket etki alanı (örneğin "DUNS" veya "DUNS numarası"), kullanıcı kimlik bilgileri ve satıcı kataloglarına erişmek için URL gibi bazı bilgileri harici katalog yapılandırmasında kullanmanız için size vermesi gerekir.

## <a name="setting-up-an-external-catalog"></a>Harici bir katalog ayarlama

Harici katalog satınalma talebini giren çalışanın ürünleri seçmek için harici siteye yönlendirilmesini sağlamalıdır. Çalışanın harici katalogdan seçtiği ürünler güncelleştirilmiş fiyat bilgileriyle birlikte döndürülür ve buradan satınalma talebine eklenebilir. Amaç çalışanın harici siteye bir sipariş vermesini sağlamak değildir. Harici kataloğu ayarlarken, harici katalog tarafından erişilen sitenin amacının gerçek bir sipariş yerleştirmek değil teklif bilgilerini toplamak olduğundan emin olmanız gerekir.

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>Harici bir satıcı kataloğu ayarlamak için, aşağıdaki görevleri tamamlamanız gerekir:

1. Bir tedarik kategori hiyerarşisi ayarlayın. Daha fazla bilgi için bkz. [Tedarik kategorisi hiyerarşileri için ilkeleri ayarlama](tasks/set-up-policies-procurement-category-hierarchies.md).
2. Satıcıyı Supply Chain Management'a kaydedin. Harici satıcı kataloğuna erişmek için yapılandırmalarını ayarlamadan önce Microsoft Dynamics 365'te satıcıyı ve satıcı ilgili kişisini ayarlamanız gerekir. Harici kataloğun satıcısı seçilen tedarik kategorisine de eklenmelidir. Satıcıları kaydetme hakkında daha fazla bilgi için bkz. [Satıcı iş birliği kullanıcılarını yönetme](manage-vendor-collaboration-users.md). Satıcıları bir tedarik kategorisine atama konusunda bilgi için bkz. [Belirli tedarik kategorileri için satıcıları onaylama](tasks/approve-vendors-specific-procurement-categories.md).
3. Satıcının kullandığı para birimi ve ölçü birimlerinin ayarlandığından emin olun. Bir ölçü birimi oluşturma hakkında bilgi için bkz. [Ölçü birimi yönetme](../pim/tasks/manage-unit-measure.md).
4. Harici satıcı kataloğunu satıcınızın harici katalog sitesi gereksinimlerini kullanarak yapılandırın. Bu görev hakkında daha fazla bilgi için bkz. [Harici satıcı kataloğu yapılandırma](#configure-the-external-vendor-catalog).
5. Ayarlarının geçerli olduğunu ve satıcının harici kataloğuna erişebildiğinizi doğrulamak için satıcının harici katalog yapılandırmalarını test edin. Tanımladığınız talep kurulumu iletisini doğrulamak için **Ayarları doğrula** eylemini kullanın. Bu ileti satıcının harici katalog sitesinin bir tarayıcı penceresinde açılmasına neden olmalıdır. Doğrulama sırasında satıcıdan ürün veya hizmet sipariş edemezsiniz. Malzeme veya hizmet sipariş etmek için satıcının kataloğuna bir satınalma talebinden erişmeniz gerekir.
6. Harici kataloğu **Harici kataloglar** sayfasındaki **Kataloğu etkinleştir** düğmesini kullanarak etkinleştirin. Çalışanların kullanabilmesi için harici kataloğun etkinleştirilmesi gerekir. Herhangi bir zamanda harici kataloğu devre dışı bırakabilirsiniz.


## <a name="configure-the-external-vendor-catalog"></a>Harici satıcı kataloğunu yapılandırma

Bu bölüm önceki bölümdeki görev 4 hakkında daha fazla ayrıntı içerir.

1. Satıcının harici kataloğu için bir ad ve açıklama girin. Girdiğiniz ad, bir talep oluşturan çalışanlara gösterilen harici kataloğu temsil eden alışveriş sepetinde görünecektir. Çalışanlar satıcının harici katalog sitesindeki kataloğu açmak için sepete tıklayabilirler.
2. **Harici katalog görüntüsü** eylemini kullanarak bir resim ekleyin. Resim, bir talep oluşturan çalışanlara gösterilen harici kataloğu temsil eden alışveriş sepetinde görünecektir. Resmin genişliğinin ve yüksekliğinin eşit olması gerektiğini unutmayın. Aksi halde resim düzgün görüntülenmez.
3. Satıcının harici katalog web sitesinin çalışanın talebi oluşturduğu tarayıcı penceresinde mi görüntüleneceğini yoksa yeni bir pencerede mi açılacağını belirleyin.
4. Katalog için satıcıyı seçin. **Tüzel kişilikler** listesinde, satıcının ayarlandığı her tüzel kişilik için bir satır bulunur. Kullanıcıların bazı tüzel kişiliklerde ürünleri doğrudan satıcının kataloğundan talep etmelerine olanak tanımak ancak bazı tüzel kişiliklerde buna izin vermemek üzere, kataloğun kullanılabilir veya kullanılamaz olmasını istediğiniz her tüzel kişilik için **Erişimi engelle** veya **Erişime izin ver** düğmesini kullanılabilirsiniz.
5. **Varsayılan süre sonu (Gün)** alanında, harici katalogdan alınan bir teklifin geçerli olacağı ve harici satıcıdan satınalmak için kullanılabileceği gün sayısını girin. Bir teklif oluşturulduğunda ve satıcının harici katalog sitesinden alındığında, teklif geçerli sistem tarihi itibarıyla geçerli olur bu alana girdiğiniz gün sayısı boyunca geçerli kalır.
6. Tedarik kategorilerini harici katalogla eşleştirmek için **Ekle** düğmesini tıklayın. Ardından Kategori adı listesinden bir kategori seçin. Kategori listesi, satıcının satıcı için ayarlanan tüm tüzel kişiliklerde eşlendiği bir tedarik kategorileri üst kümesidir.

    > [!NOTE]
    > Tedarik ilkeleri, satın alan bir tüzel kişilik veya alan işletme birimi için kategorilere erişim izni vermek veya erişimi engellemek için kullanılır. Harici bir kataloğa çıkış, erişime katalogla eşlenen en az bir tedarik kategorisi için izin verilmiş olmasını gerektirir.

7. Satıcıya gönderilecek cXML kurulum talebi iletisini ayarlayın. Otomatik olarak oluşturulan ileti biçimi, bir oturumu başlatmak için gerekli olan minimum şablondur. Etiketler için değerleri girin.

İstediğiniz zaman, sistem tarafından oluşturulan ileti şablonunu **İleti biçimini geri yükle**'ye tıklayarak yeniden yükleyebilirsiniz. İleti biçimini geri yüklerseniz, geçerli iletinin otomatik olarak oluşturulan ve etiketleri boş olan mesaj biçimiyle değiştirileceğini unutmayın.

### <a name="cxml-setup-message"></a>cXML kurulumu iletisi
Aşağıda şablonda bulunan etiketlerin açıklamasını bulabilirsiniz:

| Alan | Açıklama | 
|---------|---------|
|< Header >< From >< Credential domain=”” >|Satın alıcı şirketinin etki alanı.|
|< Header >< From >< Credential>< Identity >< /Identity > | Satın alıcı şirketinin kimliği.|
|< Header >< To >< Credential domain=”” > | Satıcı şirketinin etki alanı.|
|< Header >< To >< Credential>< Identity >< /Identity> | Satıcı şirketinin kimliği.|
|< Header >< Sender >< Credential domain=”” > | Satın alıcı şirketinin etki alanı.|
|< Header >< Sender >< Credential >< Identity >< /Identity> | Satın alıcı şirketinin kimliği.|
|< Header >< Sender >< Credential >< SharedSecret >< /SharedSecret >|Alıcının şirketi için paylaşılan gizli kod.|
|< Request deploymentMode=”” >|Test veya üretim dağıtımı.|
|< Request >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|Satıcının PunchOut uç noktası URL'si.|

### <a name="extrinsic-elements"></a>İkincil öğeler

İkincil öğe, çıkış yapan kullanıcının adına dayanan kullanıcı adı gibi bir ek bilgidir. İkincil öğe, PunchOut işlemi gerçekleştiğinde ayarlanır ve talep kurulum iletisinde gönderilebilir.
Satıcınızın kurulum isteğinde bir ikincil öğe almak gibi bir gereksinimi olabilir. Bu durumda, **Harici katalog** sayfasının **İleti biçimi** bölümündeki ikincil öğeler listesine ikincil öğe eklemeniz gerekir.
İkincil öğe için satıcının tanıyabileceği ve bir değerle eşleyebileceği için bir ad belirtin. Değerler için seçenekler şunlardır: Kullanıcı adı, Kullanıcı e-postası veya Rasgele değer.
CXML protokolü hakkında daha fazla bilgi için bkz: [cXML.org websitesi](http://cxml.org/).

## <a name="post-back-message"></a>Geri gönderme iletisi
Geri gönderme iletisi, kullanıcı harici siteden çıkış yapıp Supply Chain Management'a döndüğünde satıcı tarafından gönderilen iletidir. Geri gönderme iletileri yapılandırılamaz. İletiler cXML protokolü tanımını temel alır. Bir talep satırında alınan geri gönderme iletisinin parçası olabilecek bilgiler aşağıda verilmektedir.

| İleti satıcıdan alındı | Talep satırına kopyalandı|
|------------------------------|----------------------------------------------------------|
|< ItemIn quantity=”” > |Miktar|
|< ItemIn>< ItemID >< SupplierPartID >< /SupplierPartID >|Harici madde kodu|
|< ItemDetail>< UnitPrice >< Money currency=”” >| Para birimi|
|< ItemDetail >< UnitPrice >< Money >< /Money >| Birim fiyatı|
|< ItemDetail >< Description ShortName=”” >|Ürün adı|
|< ItemDetail >< Description >< /Description >|Madde açıklamasına dahil edilir; ShortName belirtilmediyse Ürün adı.|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|Birim|
|< ItemDetail >< Classification >< /Classification >|Madde açıklamasına dahil edilir|
|< ItemDetail >< Classification domain=”” >|Madde açıklamasına dahil edilir|

## <a name="delete-an-external-catalog"></a>Harici bir kataloğu silme
Harici bir kataloğu sayfadaki Silme eylemiyle silin.

Harici satıcı kataloğundaki bir ürünün istenmiş olması durumunda, harici satıcı kataloğu silinemez. Bunun yerine, harici satıcı kataloğu durumu etkin değil olarak ayarlanır. Harici satıcı kataloğu sitesine erişimi kaldırmak istiyor ancak harici kataloğu silmek istemiyorsanız, harici katalog durumunu etkin değil olarak değiştirin.

## <a name="additional-resources"></a>Ek kaynaklar

- [CXML geliştirmeleri satın alma](purchasing-cxml-enhancements.md)
- [PunchOut e-procurement için harici katalogları kullanma](use-external-catalogs-for-punchout.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]