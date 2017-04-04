---
title: "Mobil Fatura statü değerlerini"
description: "Mobil deneyimlerini tasarım iş kullanıcısı Microsoft Dynamics 365 işlemleri için mobil yetenekleri sağlar. Bunlar istediğiniz gibi Gelişmiş senaryolar için platform de yapalım geliştiriciler yeteneklerini genişletir. Bazı yeni kavramları mobile hakkında bilgi edinmek için en etkili yolu, bir kaç senaryo tasarlama işlemi boyunca tıklatmaktır. Bu konu, Satıcı Fatura statü değerlerini cep kullanım örneği olarak yararlanarak mobil senaryoları tasarlamak için pratik bir yaklaşım sağlamak için hazırlanmıştır. Bu konuda, yardımcı diğer çeşidi senaryoları tasarlamak ve satıcı faturaları için ilişkili olmayan diğer senaryolar için de uygulanabilir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 30229c0d24aed0bd927993b9af76b32d9bb073ee
ms.lasthandoff: 03/31/2017


---

# <a name="mobile-invoice-approvals"></a>Mobil Fatura statü değerlerini

Mobil deneyimlerini tasarım iş kullanıcısı Microsoft Dynamics 365 işlemleri için mobil yetenekleri sağlar. Bunlar istediğiniz gibi Gelişmiş senaryolar için platform de yapalım geliştiriciler yeteneklerini genişletir. Bazı yeni kavramları mobile hakkında bilgi edinmek için en etkili yolu, bir kaç senaryo tasarlama işlemi boyunca tıklatmaktır. Bu konu, Satıcı Fatura statü değerlerini cep kullanım örneği olarak yararlanarak mobil senaryoları tasarlamak için pratik bir yaklaşım sağlamak için hazırlanmıştır. Bu konuda, yardımcı diğer çeşidi senaryoları tasarlamak ve satıcı faturaları için ilişkili olmayan diğer senaryolar için de uygulanabilir.

<a name="prerequisites"></a>Önkoşullar
-------------

| Önkoşul                                                                                            | Açıklama                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Önceden okuma mobil el kitabı                                                                                |(/ dynamics365/işlemleri/dev-ITPro/mobil-apps / mobile-platform.md)                                                                                                  |
| Dynamics 365 işlemleri için                                                                             | Bir Microsoft Dynamics 365 işlemleri için 1611 sürümde ortamı ve işlemleri platform Microsoft Dynamics 3 (Kasım 2016) güncelleştirmesi                   |
| KB 3204341 düzeltmeyi yükleyin.                                                                              | Görev Kaydedici yanlışlıkla iki Kapat komutu bu işlem platform Güncelleştirmesi (güncelleştirme Kasım 2016) 3 Dynamics 365 içinde bulunmaktadır açılan iletişim kutuları için kaydedebilirsiniz |
| KB 3207800 düzeltmeyi yükleyin.                                                                              | Bu düzeltme ekleri bu Dynamics 365 içinde işlem platform Güncelleştirmesi (güncelleştirme Kasım 2016) 3 dahil mobil istemci üzerinde görüntülenmek üzere etkinleştirir.           |
| KB 3208224 düzeltmeyi yükleyin.                                                                              | Bu Microsoft Dynamics AX uygulama 7.0.1 (Mayıs 2016) dahil mobil satıcı fatura onayı uygulaması için uygulama kodu.                          |
| Bir Android, IOS ya da mobil uygulama işlemleri için Dynamics 365 için yüklü olan bir Windows aygıtı | App uygun app store içinde arayın.                                                                                                                     |

## <a name="introduction"></a>Giriş
Satıcı faturaları için mobil onayları "Önkoşullar" bölümünde açıklanan üç düzeltmeleri gerekir. Bu düzeltmeler için Fatura statü değerlerini çalışma sağlaması gerekmez. Ne öğrenmek için bir çalışma alanı bağlamında mobil, Okuma "Önkoşullar" bölümünde açıklanan mobil el kitabı. Fatura onaylarını çalışma tasarlanması gerekir. 

Her Kuruluş orchestrates ve satıcı faturaları için kendi iş süreci farklı tanımlar. Bir mobil deneyimi için Satıcı Fatura statü değerlerini tasarlamadan önce iş süreci aşağıdaki yönlerini düşünmelisiniz. Bu aygıt üzerindeki kullanıcı deneyimini en iyi duruma getirmek mümkün olduğunca çok veri noktası kullanmak için olur.

-   Hangi alanların faturası başlığından kullanıcı mobil deneyimi ve hangi sırayla görmek istersiniz?
-   Hangi alanların faturası satırlarından kullanıcı mobil deneyimi ve hangi sırayla görmek istersiniz?
-   Kaç tane fatura satırları faturada var mı? Burada 80-20 kuralı uygulamak ve yüzde 80'i için en iyi duruma getirme.
-   Kullanıcılar (fatura kodlama) hesap dağıtımları mobil aygıtta incelemeleri sırasında görmek istersiniz? Bu soruya yanıt Evet ise, aşağıdaki soruları göz önünde bulundurun:
    -   Kaç tane hesap dağıtımları (Genişletilmiş Fiyat, satış vergisi, giderleri, bölmeleri vb.) için bir fatura satırı vardır? Yine, 80-20 kuralı uygulayın.
    -   Faturaları fatura başlığındaki hesap dağıtımları gerekir mi? Öyleyse, bu hesap dağıtımları aygıtta kullanılabilir olması gerekir?

> [!NOTE]
> Çünkü bu işlevsellik şu anda mobil senaryoları için desteklenmez bu konuda hesap dağıtımları düzenlemek nasıl açıklamak değil.

-   Kullanıcılar aygıtta fatura için ekleri görmek istersiniz?

Fatura statü değerlerini için mobil deneyimi tasarımı, bu sorulara bağlı olarak farklılık gösterir. İş süreci üzerinde bir kuruluştaki mobil kullanıcı deneyimini en iyi duruma getirme amacı olduğunu. Bu konuda geri kalanı içinde biz yukarıdaki soruların farklı temel alan iki senaryo çeşitlemeleri bakmak. 

Mobil Tasarımcı ile çalışırken bir genel bir yönerge olarak, 'güncelleştirmeleri kaybolmasını önlemek için değişiklikleri yayımlamak ' olduğundan emin olun.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Basit fatura onayı senaryo için Contoso tasarlama
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Senaryo özniteliği</th>
<th>Yanıt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hangi alanların faturası başlığından kullanıcı mobil deneyimi ve hangi sırayla görmek istersiniz?</td>
<td><ol>
<li>Satıcı adı</li>
<li>Fatura toplamı</li>
<li>Fatura hesabı</li>
<li>Fatura numarası</li>
<li>Fatura tarihi</li>
<li>Fatura açıklaması</li>
<li>Vade tarihi</li>
<li>Fatura para birimi</li>
</ol></td>
</tr>
<tr class="even">
<td>Hangi alanların faturası satırlarından kullanıcı mobil deneyimi ve hangi sırayla görmek istersiniz?</td>
<td><ol>
<li>Tedarik kategorisi</li>
<li>Miktar</li>
<li>Birim fiyatı</li>
<li>Satır net tutarı</li>
<li>Vergi beyan tutarı</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kaç tane fatura satırları faturada var mı? Burada 80-20 kuralı uygulamak ve yüzde 80'i için en iyi duruma getirme.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Kullanıcılar (fatura kodlama) hesap dağıtımları mobil aygıtta incelemeleri sırasında görmek istersiniz?</td>
<td>Evet</td>
</tr>
<tr class="odd">
<td>Kaç tane hesap dağıtımları (Genişletilmiş Fiyat, satış vergisi, giderleri vb.) için bir fatura satırı vardır? Yine, 80-20 kuralı uygulayın.</td>
<td>Genişletilmiş Fiyat: 2 satış vergisi: 0 giderler: 0</td>
</tr>
<tr class="even">
<td>Faturaları fatura başlığındaki hesap dağıtımları gerekir mi? Öyleyse, bu hesap dağıtımları aygıtta kullanılabilir olması gerekir?</td>
<td>Kullanılmıyor</td>
</tr>
<tr class="odd">
<td>Kullanıcılar aygıtta fatura için ekleri görmek istersiniz?</td>
<td>Evet</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Çalışma alanı oluşturma

1.  Bir tarayıcı Dynamics 365 işlemleri için açın ve oturum açın.
2.  Oturum açtığınız sonra append **& modu mobil =** için aşağıdaki örnek ve yenileme sayfa içinde gösterildiği gibi URL: https://&lt;yoururl&gt;/? cmp = usmf & mi DefaultDashboard =**& modu mobil =**
3.  ' I **ayarları** (dişli) düğmesini tıklatın ve sayfanın sağında üst **mobil uygulama**. Mobil Uygulama Tasarımcısı yalnızca Kaydedici görünüyor görev olarak görünmesi gerekir.
4.  ' I **Ekle** yeni bir çalışma alanı oluşturmak için. Bu örnek için çalışma alanı adı **benim onayları**.
5.  Açıklama girin.
6.  Çalışma alanı rengini seçin. Çalışma alanı renk stilinin bu çalışma alanı için mobil deneyimi için kullanılır.
7.  Çalışma alanı için bir simge seçin.
8.  ' I **bitti**
9.  ' I **çalışma yayımlamak** değişiklikleri kaydetmek için

### <a name="vendor-invoices-assigned-to-me"></a>Bana atanan satıcı faturaları

Tasarım ilk mobil sayfa incelemesi kullanıcıya atanan fatura listesidir. Bu mobil sayfa tasarlamak için kullanın **VendMobileInvoiceAssignedToMeListPage** işlemleri için Dynamics 365 sayfasında. Bu yordamı tamamlamadan önce en az bir satıcı faturası için gözden geçirilmek üzere atanır emin olun ve fatura satırında iki dağıtımlar vardır. Bu kurulum bu senaryo için gereksinimleri karşılar.

1.  URL işlemleri için Dynamics 365 içinde ile menü öğesinin adını değiştirmek **VendMobileInvoiceAssignedToMeListPage** mobil sürümünü açmak için **Bana atanan satıcı faturaları bekleyen** listesi sayfası, **Borç hesapları** modülü. Sisteminizde atadığınız Fatura sayısına bağlı olarak, bu faturaları bu sayfayı gösterir. Belirli bir faturada bulmak için sol tarafta filtre kullanabilirsiniz. Ancak, biz Bu örnek için belirli bir faturaya gerektirmez. Biz yalnızca size atanan bazı mobil sayfa tasarlamanıza olanak tanımak için gittiği faturasının gerektirir. Kullanılabilir yeni sayfalar özellikle mobil senaryoları için satıcı faturası geliştirmek için tasarlanmıştır. Bu nedenle, bu sayfalar kullanmanız gerekir. Aşağıdaki URL'yi URL benzer olmalıdır ve resimde gösterilen sayfa girdiğiniz sonra görünmelidir: https://&lt;yourURL&gt;/? cmp = usmf & mi =**VendMobileInvoiceAssignedToMeListPage**& modu mobil = [![Bana atanan satıcı faturaları bekleyen sayfa](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  ' I **ayarları** (dişli) düğmesini tıklatın ve sayfanın sağında üst **mobil app**
3.  Çalışma alanınızı seçin ve **Düzenle**
4.  ' I **Ekle sayfasını** ilk mobil sayfa oluşturmak için.
5.  Gibi bir ad girin **benim satıcı faturaları**ve bir açıklama, aþaðýdaki gibi **bana gözden geçirilmek üzere atanan satıcı faturaları**.
6.  Click **Done**.
7.  Mobil tasarımcısında, üzerinde **alan** sekmesini tıklatın, **alanları seçin**. Sütunlar listesi sayfasında aşağıda benzer olmalıdır. [![Bekleyen satıcı faturalarına sütunları sayfa bana atanmış](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Mobil sayfasında kullanıcılara gösterilecek listesi sayfasından gerekli sütunları ekleyin. İçine eklediğiniz alanlar son kullanıcıya görüntülenecek olan sipariş sırasıdır. Tüm alanları yeniden seçerek sıralama alanlarını değiştirmek için tek yolu olacaktır. Bu senaryo için gereksinimleri bağlı olarak, aşağıdaki sekiz alanlar gereklidir. Ancak, bazı kullanıcılar mobil aygıtta sağlamak için çok fazla bilgi sekiz alanları düşünebilirsiniz. Bu nedenle, mobil liste görünümünde yalnızca en önemli alanları göstereceğiz. Geri kalan alanlar, biz daha sonra tasarlayacaksınız Ayrıntılar görünümünde görüntülenir. Şu an için biz aşağıdaki alanları ekleyin. Artı işaretini tıklatın (**+**) mobil sayfaya eklemek için bu sütunlarda.
    1.  Satıcı adı
    2.  Fatura toplamı
    3.  Fatura hesabı
    4.  Fatura numarası
    5.  Fatura tarihi

    Alan eklendikten sonra mobil sayfada aşağıda benzer olmalıdır. [![Alan eklendikten sonra sayfa](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  İş akışı eylemleri daha sonra etkinleştirmek üzere, aşağıdaki sütunları şimdi de eklemeniz gerekir.
    1.  Görev tamamlanamıyor Göster
    2.  Görev için Temsilci Seç Göster
    3.  Geri çekme görevini göster
    4.  Red görevini göster
    5.  İsteğin tamamlanması görevini göster
    6.  Yeniden gönderme işlemi görevini göster

10. ' I **yapılan** düzenleme modundan çıkmak için.
11. ' I **geri** ve sonra **yapılan** çalışma çıkmak için
12. ' I **çalışma yayımlamak** işinizi kaydetmek için.
13. Etkinleştirme **görüntü Fatura toplam satıcı faturaları listesi** Borç hesapları parametreleri formundaki altında nda **fatura**. Bu parametre yalnızca etkinleştirerek, fatura toplamları bekleyen satıcı faturaları Listesi sayfasında görüntülenecek hesaplanır, unutmayın. Bu, önceden gerekli düzeltme 3208224 bir parçası olarak yeni bir yetenektir.

### <a name="vendor-invoice-details"></a>Satıcı Fatura Ayrıntıları

Fatura Ayrıntıları sayfasında Mobile tasarlamak için kullanın **VendMobileInvoiceHeaderDetails** işlemleri için Dynamics 365 sayfasında. Unutmayın, sisteminizde yüklü faturalar sayısına bağlı olarak, bu sayfanın eski fatura (ilk oluşturulan fatura) gösterir. Belirli bir faturada bulmak için sol tarafta filtre kullanabilirsiniz. Ancak, biz Bu örnek için belirli bir faturaya gerektirmez. Biz mobil sayfa tasarlayabilirsiniz, böylece biz sadece bazı fatura verileri gerektirir. [![İş akışı sayfası](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1.  İşlemleri URL için Dynamics 365 içinde Değiştir ile menü öğesinin adı **VendMobileInvoiceHeaderDetails** formunu açmak için
2.  Mobil Tasarımcısı'ndan açmak **ayarları** (dişli) düğmesi.
3.  ' I **düzenleme** çalışma alanında düzenleme modunda başlatmak için düğmeyi.
4.  Seçin ** benim satıcı faturaları ** daha önce oluşturduğunuz sayfa ve i **düzenleme**.
5.  Üzerinde **alan** sekmesini tıklatın, **ızgara** sütun başlığı.
6.  ' I **Özellikler**&gt;**Ekle sayfasını**. **Not:** tıklattığınızda **ızgara** başlık ve sayfa otomatik olarak kurulan ayrıntıları ile ilişkisi bir sayfa ekleyin.
7.  Bir sayfa başlığı girin **fatura ayrıntıları**ve bir açıklama, gibi **Fatura başlığı ve satır ayrıntıları görüntüle**.
8.  ' I **alanları seçin**. İçine eklediğiniz sırada alanları son kullanıcıya görüntülenecek olan sipariş olduğuna dikkat edin. Tüm alanları yeniden seçerek sıralama alanlarını değiştirmek için tek yolu olacaktır.
9.  Bu senaryo için gereksinimleri temel alarak başlığından aşağıdaki alanları ekleyin:
    1.  Satıcı adı
    2.  Fatura toplamı
    3.  Fatura hesabı
    4.  Fatura numarası
    5.  Fatura tarihi
    6.  Fatura açıklaması
    7.  Vade tarihi
    8.  Fatura para birimi

10. Gelen satır kılavuz sayfasında aşağıdaki alanları ekleyin:
    1.  Tedarik kategorisi
    2.  Miktar
    3.  Birim fiyatı
    4.  Satır net tutarı
    5.  Vergi beyan tutarı

11. Önceki iki adımı tüm alanları ekledikten sonra ' ı **yapılan**. Sayfa aşağıda benzer olmalıdır. [![Alan eklendikten sonra sayfa](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. ' I **yapılan** düzenleme modundan çıkmak için.
13. ' I **geri** ve sonra **yapılan** çalışma çıkmak için
14. ' I **çalışma yayımlamak** işinizi kaydetmek için

### <a name="workflow-actions"></a>İş akışı eylemleri

İş akışı eylemleri eklemek, **VendMobileInvoiceHeaderDetails** işlemleri için Dynamics 365 sayfasında. Bu sayfayı açmak için daha önce yaptığınız gibi menü öğesi URL adını değiştirin. Mobil Tasarımcısı'ndan sonra açmak **ayarları** (dişli) düğmesi. Ayrıntıları sayfasında iş akışı eylemlerini eklemek için aşağıdaki adımları izleyin.

1.  ' I **düzenleme** çalışma alanında düzenleme modunda başlatmak için düğmeyi.
2.  Seçin **fatura ayrıntıları** daha önce oluşturduğunuz sayfa ve i **düzenleme**.
3.  Üzerinde **Eylemler** sekmesini tıklatın, **eylem eklemek**.
4.  Gibi bir eylem başlığı girin **Onayla**ve bir açıklama, aþaðýdaki gibi **Onayla fatura**. Not eylem başlığı buraya girin mobil app kullanıcıya gösterilen eylem adı haline gelir.
5.  Click **Done**.
6.  ' I **alanları seçin**.
7.  İş akışı işlemi boyunca devam **VendMobileInvoiceHeaderDetails** sayfa ve kaydetmek istediğiniz eylemi tamamlayamıyor. Yorumlar alanına mobil deneyimi de dahil, bu işlem sırasında iş akışı yorumlar girmek emin olun.
8.  İş akışı eylemi çalıştırıldıktan sonra'ı **yapılan** alan seçmek görevi tamamlamak için.
9.  ' I **yapılan** düzenleme modundan çıkmak için.
10. ' I **geri** ve sonra **yapılan** çalışma çıkmak için
11. ' I **çalışma yayımlamak** işinizi kaydetmek için
12. 3-11 gerekli iş akışı eylemleri kaydetmek için adımları yineleyin. Size atanan iş akışı eylemleri için tasarlamak için uygulayacağınız size sağlamak için bir durumda olan faturaları için bir gereksinim olduğuna dikkat edin.
13. Not Defteri veya Microsoft Visual Studio açın ve aşağıdaki kodu yapıştırın. Dosyasını .js dosya olarak kaydedin. Bu kod iki şey gerçekleştirir:
    1.  Mobil Listesi sayfasında daha önce eklediğimiz ekstra iş akışı ile ilgili sütunları gizler. Böylece uygulama bağlamında bu bilgilere sahip ve sonraki adıma yapmak için bu sütunları eklediğimiz.
    2.  Bağlı olarak etkin olan iş akışı adımı, yalnızca bu eylemleri göstermek için mantık geçerlidir.

Sayfaları ve diğer denetimleri JS kodu adını aynı çalışma alanı'ndan, olmalıdır.

1.  Işlevi ana (metadataService, dataService, cacheService, $q) {dönmek {appInit: işlevi (appMetadata) {/ / metadataService.configureControl var, ancak görünmez olması gereken denetimleri gizleme ('My-satıcı-faturalar, 'ShowAccept' {Gizli: true}); metadataService.configureControl ('My-satıcı-faturalar, 'ShowApprove' {Gizli: true}); metadataService.configureControl ('My-satıcı-faturalar, 'ShowReject' {Gizli: true}); metadataService.configureControl ('My-satıcı-faturalar, 'ShowDelegate' {Gizli: true}); metadataService.configureControl ('My-satıcı-faturalar, 'ShowRequestChange' {Gizli: true}); metadataService.configureControl ('My-satıcı-faturalar, 'ShowRecall' {Gizli: true}); metadataService.configureControl ('My-satıcı-faturalar, 'ShowComplete' {Gizli: true}); metadataService.configureControl ('My-satıcı-faturalar, 'ShowResubmit' { Gizli: true}); }, pageInit: işlevi (pageMetadata, params) {ise (pageMetadata.Name == 'Fatura Ayrıntıları') {/ / Göster/Gizle iş akışı eylemleri iş akışında temel adım metadataService.configureAction ('Accept' {görünür: true}); metadataService.configureAction ('Onayla' {görünür: true}); metadataService.configureAction ('Reddet' {görünür: true}); metadataService.configureAction ('Temsilci' {görünür: true}); metadataService.configureAction (' isteği-Değiştir ', {görünür: true}); metadataService.configureAction ('Geri' {görünür: true}); metadataService.configureAction ('Tamamlandı' {görünür: true}); metadataService.configureAction ('Yeniden gönderme işlemi' {görünür: true});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  Kod dosyasını seçerek çalışma alanına karşıya **mantık** sekmesi
3.  ' I **yapılan** düzenleme modundan çıkmak için.
4.  ' I **geri** ve sonra **yapılan** çalışma çıkmak için
5.  ' I **çalışma yayımlamak** işinizi kaydetmek için

### <a name="vendor-invoice-attachments"></a>Satıcı Fatura ekleri

1.  ' I **ayarları** (dişli) düğmesini tıklatın ve sayfanın sağında üst **mobil app**
2.  ' I **düzenleme** çalışma alanında düzenleme modunda başlatmak için düğmeyi.
3.  Seçin ** fatura ayrıntıları ** daha önce oluşturduğunuz sayfa ve i **düzenleme**.
4.  Set **belge yönetimi** için seçenek **Evet** aşağıda gösterildiği gibi. **Not:** mobil aygıtta ekleri göstermek için hiçbir gereksinimleri varsa, bu seçeneği ayarlamak bırakın **No**, varsayılan ayarı olur.
5.  [![docmanagement](./media/docmanagement-216x300.png)](./media/docmanagement.png)
6.  ' I **yapılan** düzenleme modundan çıkmak için.
7.  ' I **geri** ve sonra **yapılan** çalışma çıkmak için
8.  ' I **çalışma yayımlamak** işinizi kaydetmek için

### <a name="vendor-invoice-line-distributions"></a>Satıcı fatura satırının dağıtımları

Yalnızca satır dağıtımları düzeyi olur ve fatura tek bir satırı her zaman olacaktır bu senaryo için gereksinimleri doğrulayın. Bu senaryoda, basit olduğundan, kullanıcı deneyimini mobil aygıttaki de kullanıcı birkaç düzeyleri dağıtımlarını görüntülemek için ayrıntıya sahip olmadığı kadar basit olmalıdır. Dynamics 365 işlemleri için satıcı faturaları fatura başlığındaki tüm dağıtımları gösteren seçeneği içerir. Bu deneyimi için mobil senaryo ne ihtiyacımız var. Bu nedenle, biz kullanır **VendMobileInvoiceAllDistributionTree** bu mobil senaryonun bir parçası tasarlamak için sayfa. 

> [!NOTE] 
> Gereksinimleri bilmek bize hangi belirli sayfa kullan ve biz senaryo tasarlarken tam olarak mobil kullanıcı deneyimini en iyi duruma getirme için karar yardımcı olur. Bu senaryo için gereksinimler farklılık gösterdiğinden İkinci senaryoda, farklı bir sayfaya dağıtımları göstermek için kullanacağız.

1.  URL'de, daha önce yaptığınız gibi menü öğesinin adını değiştirin. Aşağıdaki resimde görüntülenen sayfa benzemelidir. [![Tüm dağıtımlar sayfa](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Mobil Tasarımcısı'ndan açmak **ayarları** (dişli) düğmesi.
3.  ' I **düzenleme** çalışma alanında düzenleme modunda başlatmak için düğmeyi. **Not:** iki yeni sayfalar otomatik olarak oluşturulduğunu görürsünüz. Önceki bölümde belge yönetimi açık olduğundan, sistem bu sayfalar oluşturur. Bu yeni sayfalar sayabilirsiniz.
4.  ' I **Ekle sayfasını**.
5.  Bir sayfa başlığı girin **görünüm hesap**ve bir açıklama, gibi **görünüm hesap fatura için**.
6.  Click **Done**.
7.  Üzerinde **alan** sekmesini tıklatın, **alanları seçin**, dağıtımları sayfasından aşağıdaki alanları seçin ve sonra tıklatın **yapılan**:
    1.  Tutar
    2.  Para Birimi
    3.  Genel muhasebe hesabı

> [!NOTE] 
> Seçeneğini belirlemediğim **açıklama** dağıtımları kılavuz sütun olduğundan bu senaryo için gereksinimleri Genişletilmiş Fiyat için dağıtımları olacaktır sadece tutar olduğunu doğruladı. Bu nedenle, kullanıcı, dağıtım için tutar türünü belirlemek için başka bir alan istemeyecektir. Ancak, senaryoda İleri, biz **olur** bu senaryo için gereksinimleri diğer tutar türleri (örneğin, satış vergisi) dağıtımları olduğunu belirtmek için bu bilgileri kullanın.
8.  ' I **yapılan** düzenleme modundan çıkmak için.
9.  ' I **geri** ve sonra **yapılan** çalışma çıkmak için
10. ' I **çalışma yayımlamak** işinizi kaydetmek için

**Not:****görünüm hesap** mobil sayfada değil şu anda bağlı herhangi şimdiye tasarladığımız mobil sayfalar. Kullanıcı gitmek mümkün olmayacaktır çünkü **görünüm hesap** gelen sayfa **fatura ayrıntıları** sayfa mobil aygıtta gezinmesinden sağladığımız gerekir **fatura ayrıntıları** sayfasına **görünüm hesap** sayfa. Biz bu gezinti JavaScript aracılığıyla ek mantık kullanarak oluşturun.

1.  Daha önce oluşturduğunuz .js dosyasını açın ve aşağıdaki kodda vurgulanan satırlar ekleyin. Bu kod iki şey gerçekleştirir:
    1.  Kullanıcılar doğrudan çalışma alanına gidemiyor garanti yardımcı **görünüm hesap** sayfa.
    2.  Gezinti denetimden kuran **fatura ayrıntıları** sayfasına **görünüm hesap** sayfa.

> [!NOTE] 
> Sayfaları ve diğer denetimleri JS kod adı çalışma alanından aynı olması gerekir.

1.  Işlevi ana (metadataService, dataService, cacheService, $q) {dönmek {appInit: işlevi (appMetadata) {/ / metadataService.configureControl var, ancak görünmez olması gereken denetimleri gizleme ('My-satıcı-faturalar, 'ShowAccept' {Gizli: true}); metadataService.configureControl ('My-satıcı-faturalar, 'ShowApprove' {Gizli: true}); metadataService.configureControl ('My-satıcı-faturalar, 'ShowReject' {Gizli: true}); metadataService.configureControl ('My-satıcı-faturalar, 'ShowDelegate' {Gizli: true}); metadataService.configureControl ('My-satıcı-faturalar, 'ShowRequestChange' {Gizli: true}); metadataService.configureControl ('My-satıcı-faturalar, 'ShowRecall' {Gizli: true}); metadataService.configureControl ('My-satıcı-faturalar, 'ShowComplete' {Gizli: true}); metadataService.configureControl ('My-satıcı-faturalar, 'ShowResubmit' { Gizli: true}); Sayfalar için Gezinti metadataService.hideNavigation('View-accounting') kök uygulanamaz Gizle; Hesap metadataService.addLink görüntülemek için bağlantıyı (' fatura ayrıntıları, ' görünüm hesap ', ' görünüm hesap nav denetim ', 'Görünüm hesap', true); }, pageInit: işlevi (pageMetadata, params) {ise (pageMetadata.Name == 'Fatura Ayrıntıları') {/ / Göster/Gizle iş akışı eylemleri iş akışında temel adım metadataService.configureAction ('Accept' {görünür: true}); metadataService.configureAction ('Onayla' {görünür: true}); metadataService.configureAction ('Reddet' {görünür: true}); metadataService.configureAction ('Temsilci' {görünür: true}); metadataService.configureAction (' isteği-Değiştir ', {görünür: true}); metadataService.configureAction ('Geri' {görünür: true}); metadataService.configureAction ('Tamamlandı' {görünür: true}); metadataService.configureAction ('Yeniden gönderme işlemi' {görünür: true});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  Kod dosyasını seçerek çalışma alanına karşıya **mantık** önceki kod yazmak için sekme
3.  ' I **yapılan** düzenleme modundan çıkmak için.
4.  ' I **geri** ve sonra **yapılan** çalışma çıkmak için
5.  ' I **çalışma yayımlamak** işinizi kaydetmek için

### <a name="validation"></a>Doğrulama

Mobil aygıtınızdan uygulamasını açın ve işlemleri örneği için Dynamics 365 bağlanın. Burada satıcı faturaları gözden geçirilmek üzere atanmış, şirkete oturumu açma emin olun. Aşağıdaki eylemleri gerçekleştirmeniz:

-   Bkz: **benim onayları** çalışma alanı.
-   Ayrıntısına **benim onayları** çalışma alanı ve bkz: **benim satıcı faturaları** sayfa.
-   Ayrıntısına **benim satıcı faturaları** sayfa ve size atanmış olan faturaların listesini görebilirsiniz.
-   Bir fatura ayrıntısına ve fatura Üstbilgi ayrıntılarını ve satır ayrıntıları görebilirsiniz.
-   Ayrıntıları sayfasında bağlantı eklere bakın ve eklerin listesine gidin ve ekleri görüntülemek için bu bağlantıyı kullanın.
-   Bağlantı ayrıntıları sayfasında ziyaret **hesap görüntülemek** sayfa ve dağıtımları sayfasına gidin ve dağıtımlarını görüntülemek için bu bağlantıyı kullanın.
-   Ayrıntıları sayfasında tıklatın **Eylemler**, alt menü ve iş akışı adımı için geçerli olan iş akışı eylemleri gerçekleştirin.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Karmaşık fatura onayı senaryo için Fabrikam tasarlama
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Senaryo özniteliği</th>
<th>Yanıt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hangi alanların faturası başlığından kullanıcı mobil deneyimi ve hangi sırayla görmek istersiniz?</td>
<td><ol>
<li>Satıcı adı</li>
<li>Fatura tutarı</li>
<li>Fatura hesabı</li>
<li>Fatura numarası</li>
<li>Fatura tarihi</li>
<li>Fatura açıklaması</li>
<li>Vade tarihi</li>
<li>Fatura para birimi</li>
</ol></td>
</tr>
<tr class="even">
<td>Hangi alanların faturası satırlarından kullanıcı mobil deneyimi ve hangi sırayla görmek istersiniz?</td>
<td><ol>
<li>Tedarik kategorisi</li>
<li>Miktar</li>
<li>Birim fiyatı</li>
<li>Satır net tutarı</li>
<li>Vergi beyan tutarı</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kaç tane fatura satırları faturada var mı? Burada 80-20 kuralı uygulamak ve yüzde 80'i için en iyi duruma getirme.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Kullanıcılar (fatura kodlama) hesap dağıtımları mobil aygıtta incelemeleri sırasında görmek istersiniz?</td>
<td>Evet</td>
</tr>
<tr class="odd">
<td>Kaç tane hesap dağıtımları (Genişletilmiş Fiyat, satış vergisi, giderleri vb.) için bir fatura satırı vardır? Yine, 80-20 kuralı uygulayın.</td>
<td>Genişletilmiş Fiyat: 2 satış vergisi: 2 ücretleri: 2</td>
</tr>
<tr class="even">
<td>Faturaları fatura başlığındaki hesap dağıtımları gerekir mi? Öyleyse, bu hesap dağıtımları aygıtta kullanılabilir olması gerekir?</td>
<td>Kullanılmıyor</td>
</tr>
<tr class="odd">
<td>Kullanıcılar aygıtta fatura için ekleri görmek istersiniz?</td>
<td>Evet</td>
</tr>
</tbody>
</table>

### <a name="exercise"></a>Alıştırma

Senaryo 1, Senaryo 2 gereksinimleri temel alarak aşağıdaki çeşitlemelerden yapılabilir. Bu bölümde, öğrenme amaçları için tamamlayabileceğiniz bir alıştırma olarak kullanın.

1.  Daha fazla fatura satırları Senaryo 2 beklenir çünkü tasarımı yapılan aşağıdaki değişiklikler mobil aygıt üzerindeki kullanıcı deneyimini en iyi duruma yardımcı olacaktır:
    1.  (Senaryo 1) olduğu gibi ayrıntıları sayfasında fatura satırları görüntülemek yerine, kullanıcılar, ayrı bir mobil sayfa satırlarını görüntülemek seçebilirsiniz.
    2.  Birden çok fatura satırı, bu senaryoda, beklenir çünkü **VendMobileInvoiceAllDistributionTree** (Senaryo 1) olduğu gibi cep dağıtımları sayfa tasarlamak için kullanılan sayfa, kullanıcının dağıtımları için satırları ilişkilendirmek kafa karıştırıcı olabilir. Bu nedenle, kullanın **VendMobileInvoiceLineDistributionTree** dağıtımları sayfa tasarlamak için sayfa.
    3.  İdeal olarak, bu senaryoda bir fatura satırı bağlamında dağıtımları gösterilmesi gerekir. Bu nedenle, kullanıcı dağıtımları sayfayı görmek için bir satıra inebilir emin olun. Senaryo 1 başlığı ve ayrıntıları sayfaları için yaptığınız gibi sayfa bağlantı yeteneği detaylandırma, kurmak için kullanın.

2.  Dağıtımları Senaryo 2'de (satış vergisi, giderleri vb.) birden fazla tutar türü beklendiği için seçtiğiniz tutar türü açıklamasını görüntülemek yararlı olacaktır. (Biz bu bilgiyi Senaryo 1 atlanmış.)

## <a name="conclusion"></a>Sonuç
Mobil platform ve uygulama yetenekleri bir kuruluştaki temel bir kullanıcı için optimize edilmiş mobil senaryoları tasarlamak sağlar. Bu konuda sağlanan örnekler temel alarak, belirli bir gereksinimi karşılamak farklı deneyimleri oluşturmak ve diğer çeşitlemelerdeki deneyin.


