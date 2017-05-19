---
title: "Mobil fatura onayları"
description: "Microsoft Dynamics 365 for Operations&quot;daki mobil yetenekler işletme kullanıcısının mobil deneyimleri tasarlamasına olanak tanır. Gelişmiş senaryolar için platform geliştiricilerin de yeteneklerini istedikleri gibi genişletmesine olanak tanır. Mobildeki yeni kavramlardan bazıları hakkında bilgi edinmek için en etkili yol, bir kaç senaryo tasarlama işleminde ilerlemektir. Bu konu, mobil için satıcı faturası onaylarını bir kullanım durumu olarak kullanarak mobil senaryolar tasarlamak amacıyla partik bir yaklaşım sunmak üzere hazırlanmıştır. Bu konu, senaryoların farklı çeşitlerini tasarlamanıza yardımcı olur ve satıcı faturalarıyla ilgili olmayan diğer senaryolara da uygulanablir."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 511dc31b96f2f5133dd0c22712d2c8d6f8746e8c
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="mobile-invoice-approvals"></a>Mobil fatura onayları

[!include[banner](../includes/banner.md)]


Microsoft Dynamics 365 for Operations'daki mobil yetenekler işletme kullanıcısının mobil deneyimleri tasarlamasına olanak tanır. Gelişmiş senaryolar için platform geliştiricilerin de yeteneklerini istedikleri gibi genişletmesine olanak tanır. Mobildeki yeni kavramlardan bazıları hakkında bilgi edinmek için en etkili yol, bir kaç senaryo tasarlama işleminde ilerlemektir. Bu konu, mobil için satıcı faturası onaylarını bir kullanım durumu olarak kullanarak mobil senaryolar tasarlamak amacıyla partik bir yaklaşım sunmak üzere hazırlanmıştır. Bu konu, senaryoların farklı çeşitlerini tasarlamanıza yardımcı olur ve satıcı faturalarıyla ilgili olmayan diğer senaryolara da uygulanablir.

<a name="prerequisites"></a>Önkoşullar
-------------

| Önkoşul                                                                                            | Açıklama                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mobil el kitabı ön okuma                                                                                |(/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform.md)                                                                                                  |
| Dynamics 365 for Operations                                                                             | Microsoft Dynamics 365 for Operations sürüm 1611 ve Microsoft Dynamics for Operations platform güncelleştirmesi 3 (Kasım 2016) güncelleştirmelerine sahip bir ortam                   |
| KB 3204341 numaralı düzeltmeyi yükleyin.                                                                              | Görev kaydedici Dynamics 365 for Operation platform güncelleştirmesi 3'te (Kasım 2016 güncellemesi) bulunan açılır iletişim kutusu için yanlışlıkla iki Kapat komutu kaydedebilir. |
| KB 3207800 numaralı düzeltmeyi yükleyin.                                                                              | Bu düzeltme eklerin Dynamics 365 for Operation platform güncelleştirmesi 3'te (güncelleştirme Kasım 2016) bulunan mobil istemci üzerinde görüntülenmesini sağlar.           |
| KB 3208224 numaralı düzeltmeyi yükleyin.                                                                              | Microsoft Dynamics AX uygulaması 7.0.1'e (Mayıs 2016) dahil edilen mobil satıcı faturası onayı uygulaması için uygulama kodu.                          |
| Dynamics 365 for Operations için mobil uygulama yüklenmiş olan bir Android, iOS veya Windows cihaz | Uygulamayı ilgili uygulama mağazasında arayın.                                                                                                                     |

## <a name="introduction"></a>Giriş
Satıcı faturaları için mobil onaylar "Önkoşullar" bölümünde açıklanan üç düzeltmenin olmasını gerektirir. Bu düzeltmeler fatura onayları için bir çalışma alanı sağlamaz. Mobil bağlamında çalışma alanının ne olduğunu öğrenmek için, "Önkoşullar" bölümünde belirtilen mobil el kitabını okuyun. Fatura onayları çalışma alanının tasarlanması gerekir. 

Her kuruluş satıcı faturaları için kendi iş sürecini farklı şekilde düzenler ve tanımlar. Satıcı fatura onayları için bir mobil deneyim tasarlamadan önce iş sürecinin aşağıdaki yönlerini göz önünde bulundurmanız gerekir. Fikir, cihaz üzerindeki kullanıcı deneyimini en iyi duruma getirmek için mümkün olduğunca çok veri noktası kullanmaktır.

-   Kullanıcı mobil deneyimde fatura başlığından hangi alanları ve hangi sırayla görmek ister?
-   Kullanıcı mobil deneyimde fatura satırlarından hangi alanları ve hangi sırayla görmek ister?
-   Faturada kaç adet fatura satırı var? Burada 80-20 kuralını uygulayın ve yüzde 80 için iyileştirme yapın.
-   Kullanıcılar incelemeler sırasında mobil cihazda muhasebe dağıtımlarını (fatura kodlama) görmek istiyor mu? Bu soruya yanıt Evet ise, aşağıdaki soruları göz önünde bulundurun:
    -   Bir fatura satırı için kaç tane hesap dağıtımı (genişletilmiş fiyat, satış vergisi, giderler, bölmeler vb.) vardır? Yine, 80-20 kuralını uygulayın.
    -   Faturaların fatura başlığında da hesap dağıtımları var mı? Öyleyse, bu hesap dağıtımlarının cihazda kullanılabilir olması gerekir mi?

> [!NOTE]
> Bu konuda hesap dağıtımlarının nasıl düzenleneceği açıklanmamaktadır çünkü bu işlevsellik şu anda mobil senaryolar için desteklenmez.

-   Kullanıcılar cihazda fatura için ekleri görmek ister mi?

Fatura onayları için mobil deneyimi tasarımı, bu sorulara bağlı olarak farklılık gösterir. Amaç, bir kuruluş içinde mobildeki iş süreci için kullanıcı deneyimini en iyi duruma getirmektir. Bu konunun devamında, yukarıdaki sorulara verilecek farklı yanıtları temel alan iki senaryo çeşidine bakacağız. 

Genel bir yönerge olarak, mobil tasarımcıyla çalışırken güncelleştirmelerin kaybolmasını önlemek için değişiklikleri "yayımlamadığınızdan' emin olun.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Contoso için basit bir fatura onayı senaryosu tasarlama
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
<td>Kullanıcı mobil deneyimde fatura başlığından hangi alanları ve hangi sırayla görmek ister?</td>
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
<td>Kullanıcı mobil deneyimde fatura satırlarından hangi alanları ve hangi sırayla görmek ister?</td>
<td><ol>
<li>Tedarik kategorisi</li>
<li>Miktar</li>
<li>Birim fiyatı</li>
<li>Satır net tutarı</li>
<li>Vergi beyan tutarı</li>
</ol></td>
</tr>
<tr class="odd">
<td>Faturada kaç adet fatura satırı var? Burada 80-20 kuralını uygulayın ve yüzde 80 için iyileştirme yapın.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Kullanıcılar incelemeler sırasında mobil cihazda muhasebe dağıtımlarını (fatura kodlama) görmek istiyor mu?</td>
<td>Evet</td>
</tr>
<tr class="odd">
<td>Bir fatura satırı için kaç tane hesap dağıtımı (genişletilmiş fiyat, satış vergisi, giderler, vb.) vardır? Yine, 80-20 kuralını uygulayın.</td>
<td>Genişletilmiş fiyat: 2 Satış vergisi: 0 Giderler: 0</td>
</tr>
<tr class="even">
<td>Faturaların fatura başlığında da hesap dağıtımları var mı? Öyleyse, bu hesap dağıtımlarının cihazda kullanılabilir olması gerekir mi?</td>
<td>Kullanılmıyor</td>
</tr>
<tr class="odd">
<td>Kullanıcılar cihazda fatura için ekleri görmek ister mi?</td>
<td>Evet</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Çalışma alanını oluştur

1.  Bir tarayıcıda Dynamics 365 for Operations'ı açın ve oturum açın.
2.  Oturum açtıktan sonra, URL'ye aşağıdaki örnekte gösterildiği gibi **&mode=mobile** ekleyin ve sayfayı yenileyin: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**
3.  Sayfanın sağ üst kısmındaki **Ayarlar** (dişli) düğmesine ve ardından **Mobil uygulama**'ya tıklayın. Mobil uygulama tasarımcısı Görev kaydedicinin göründüğü şekilde görünmelidir.
4.  Yeni bir çalışma alanı oluşturmak için **Ekle**'ye tıklayın. Bu örnek için çalışma alanı adı **Onaylarım**'dır.
5.  Açıklama girin.
6.  Çalışma alanı rengi seçin. Çalışma alanı rengi, bu çalışma alanı için mobil deneyimin genel tarzı olarak kullanılacaktır.
7.  Çalışma alanı için bir simge seçin.
8.  **Bitti**'ye tıklayın.
9.  Değişikliklerinizi kaydetmek için **Çalışma alanını yayımla**'ya tıklayın.

### <a name="vendor-invoices-assigned-to-me"></a>Bana atanan satıcı faturaları

İlk tasarlamanız gereken mobil sayfa incelenmek üzere kullanıcıya atılan faturaların listesi olmalıdır. Bu mobil sayfayı tasarlamak için Dynamics 365 for Operations'daki **VendMobileInvoiceAssignedToMeListPage** sayfasını kullanın. Bu yordamı tamamlamadan önce, en az bir satıcı faturasının gözden geçirilmek üzere size atandığından ve fatura satırında iki dağıtım olduğundan emin olun. Bu kurulum bu senaryo için gereksinimleri karşılar.

1.  **Borç hesapları** modülündeki **Bana atanmış bekleyen satıcı faturalarının** listesi sayfasının mobil  sürümünü açmak için Dynamics 365 for Operations URL'sinde menü öğesi adını **VendMobileInvoiceAssignedToMeListPage** olarak değiştirin. Sisteminizde size atanan fatura sayısına bağlı olarak, sayfa bu faturaları gösterir. Belirli bir faturayı bulmak için soldaki filtreyi kullanabilirsiniz. Ancak, bu örnek için bize belirli bir fatura gerekmiyor. Yalnızca mobil sayfanızı tasarlamanıza olanak tanıyacak size atanmış bazı faturalar olması gerekiyor. Kullanılabilir yeni sayfalar özellikle satıcı faturası için mobil senaryolar geliştirmek üzere tasarlanmıştır. Bu nedenle, bu sayfaları kullanmanız gerekir. URL aşağıdaki URL'ye benzer olmalıdır ve bunu girdikten sonra resimde gösterilen sayfada şu görünmelidir: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Bana atanmış bekleyen satıcı faturaları sayfası](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Sayfanın sağ üst kısmındaki **Ayarlar** (dişli) düğmesine ve ardından **Mobil uygulama**'ya tıklayın.
3.  Çalışma alanınızı seçin ve **Düzenle**'ye tıklayın.
4.  İlk mobil sayfayı oluşturmak için **Sayfa ekle**'ye tıklayın.
5.  **Satıcı faturalarım** gibi bir ad ve **Bana gözden geçirilmek üzere atanan satıcı faturaları** gibi bir açıklama girin.
6.  **Bitti**'ye tıklayın.
7.  Mobil tasarımcıda, **Alanlar** sekmesinde, **Alanları seç**'e tıklayın. Liste sayfasındaki sütunlar aşağıda gösterilene benzemelidir. [![Bana atanmış bekleyen satıcı faturaları sayfasındaki sütunlar](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Mobil sayfada kullanıcılara gösterilecek sütunları liste sayfasından ekleyin. Sütunları ekleme sıranız alanların son kullanıcıya gösterileceği sıradır. Alanların sıralamasını değiştirmenin tek yolu tüm alanları yeniden seçmektir. Bu senaryonun gereksinimlerine bağlı olarak, aşağıdaki sekiz alan gereklidir. Ancak, bazı kullanıcılar mobil cihazda sunmak için sekiz alanın çok fazla bilgi olduğunu düşünebilir. Bu nedenle, mobil liste görünümünde yalnızca en önemli alanları göstereceğiz. Geri kalan alanlar, daha sonra tasarlayacağımız ayrıntılar görünümünde gösterilecektir. Şu an için, aşağıdaki alanları ekleyeceğiz. Mobil sayfaya eklemek için bu sütunlardaki artı işaretini (**+**) tıklayın.
    1.  Satıcı adı
    2.  Fatura toplamı
    3.  Fatura hesabı
    4.  Fatura numarası
    5.  Fatura tarihi

    Alanlar eklendikten sonra, mobil sayfa aşağıdaki resme benzer olmalıdır. [![Alanlar eklendikten sonra sayfa](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  Daha sonra iş akışı eylemlerini etkinleştirebilmemiz için, şimdi aşağıdaki sütunları da eklemeniz gerekir.
    1.  Tamamlanan görevi göster
    2.  Göreve temsilci atamayı göster
    3.  Görevi geri çağırmayı göster
    4.  Görevi reddetmeyi göster
    5.  Talep tamamlama görevini göster
    6.  Yeniden gönderme görevini göster

10. Düzenleme modundan çıkmak için **Bitti**'ye tıklayın.
11. Çalışma alanından çıkmak için **Geri**'ye ve sonra **Bitti**'ye tıklayın.
12. Çalışmanızı kaydetmek için **Çalışma alanını yayımla**'ya tıklayın.
13. **Fatura** altından borç hesapları parametrelerindeki **Bekleyen satıcı faturaları listesinde fatura toplamını görüntüle**'yi etkinleştirin. Yalnızca bu parametre etkinleştirilerek, fatura toplamlarının bekleyen satıcı faturaları liste sayfasında gösterilmek üzere hesaplanacağını unutmayın. Bu, ön koşul olan 3208224 no'lu düzeltmenin bir parçası olan yeni bir yetenektir.

### <a name="vendor-invoice-details"></a>Satıcı faturası ayrıntıları

Mobil için fatura ayrıntıları sayfasını tasarlamak üzere Dynamics 365 for Operations'daki **VendMobileInvoiceHeaderDetails** sayfasını kullanın. Sisteminizdeki faturaların sayısına bağlı olarak, bu sayfanın en eski faturayı (ilk oluşturulan fatura) gösterdiğini unutmayın. Belirli bir faturayı bulmak için soldaki filtreyi kullanabilirsiniz. Ancak, bu örnek için bize belirli bir fatura gerekmiyor. Mobil sayfayı tasarlayabilmek için sadece bazı fatura verileri gereklidir. [![İş akışı sayfası](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1.  Dynamics 365 for Operations URL'sinde menü öğesinin adını **VendMobileInvoiceHeaderDetails** olarak değiştirerek formu açın.
2.  Mobil tasarımcıyı **Ayarlar** (dişli) düğmesinden açın.
3.  **Düzenle** düğmesine tıklayarak çalışma alanında düzenleme modunu başlatın.
4.  Daha önce oluşturduğunuz **Satıcı faturalarım** sayfasını seçin ve **Düzenle**'ye tıklayın.
5.  **Alanlar** ssekmesinde **Izgara** sütun başlığına tıklayın.
6.  **Özellikler** &gt; **Sayfa ekle**'ye tıklayın. **Not:** **Izgara** başlığına tıkladığınızde ve sayfa eklediğinizde, ayrıntılar sayfasıyla ilişki otomatik olarak kurulur.
7.  **Fatura ayrıntıları** gibi bir sayfa başlığı ve **Fatura başlığı ve satır ayrıntılarını görüntüle** gibi bir açıklama ekleyin.
8.  **Alanları seç**'e tıklayın. Ekleme sıranızın alanların son kullanıcıya gösterileceği sıra olduğunu unutmayın. Alanların sıralamasını değiştirmenin tek yolu tüm alanları yeniden seçmektir.
9.  Bu senaryonın gerekliliklerini temel alarak başlıktan aşağıdaki alanları ekleyin:
    1.  Satıcı adı
    2.  Fatura toplamı
    3.  Fatura hesabı
    4.  Fatura numarası
    5.  Fatura tarihi
    6.  Fatura açıklaması
    7.  Vade tarihi
    8.  Fatura para birimi

10. Sayfadaki satır kılavuzundan aşağıdaki alanları ekleyin:
    1.  Tedarik kategorisi
    2.  Miktar
    3.  Birim fiyatı
    4.  Satır net tutarı
    5.  Vergi beyan tutarı

11. Önceki iki adımda tüm alanları ekledikten sonra **Bitti**'yi tıklayın. Bu sayfa aşağıda gösterilene benzemelidir. [![Alanlar eklendikten sonra sayfa](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Düzenleme modundan çıkmak için **Bitti**'ye tıklayın.
13. Çalışma alanından çıkmak için **Geri**'ye ve sonra **Bitti**'ye tıklayın.
14. Çalışmanızı kaydetmek için **Çalışma alanını yayımla**'ya tıklayın

### <a name="workflow-actions"></a>İş akışı eylemleri

İş akışı eylemleri eklemek için Dynamics 365 for Operations'daki **VendMobileInvoiceHeaderDetails** sayfasını kullanın. Bu sayfayı açmak için daha önce yaptığınız gibi URL'deki menü öğesi adını değiştirin. Ardından mobil tasarımcıyı **Ayarlar** (dişli) düğmesinden açın. Ayrıntılar sayfasında iş akışı eylemlerini eklemek için aşağıdaki adımları izleyin.

1.  **Düzenle** düğmesine tıklayarak çalışma alanında düzenleme modunu başlatın.
2.  Daha önce oluşturduğunuz **Fatura ayrıntılarım** sayfasını seçin ve **Düzenle**'ye tıklayın.
3.  **Eylemler** sekmesinde **Eylem ekle** düğmesini tıklayın.
4.  **Onayla** gibi bir eylem başlığı ve **Faturayı onayla** gibi bir açıklama girin. Girdiğiniz eylem başlığının mobil uygulamada kullanıcıya gösterilen eylemin adı olacağını unutmayın.
5.  **Bitti**'ye tıklayın.
6.  **Alanları seç**'e tıklayın.
7.  **VendMobileInvoiceHeaderDetails** sayfasında iş akışı işleminde ilerleyin ve kaydetmek istediğiniz eylemi tamamlayın. Bu işlem sırasında iş akışı yorumları girdiğinizden emin olun, böylece mobil deneyime bir yorum alanı da eklenmiş olur.
8.  İş akışı eylemi çalıştırıldıktan sonra **Bitti**'ye tıklayarak Alan seç görevini tamamlayın.
9.  Düzenleme modundan çıkmak için **Bitti**'ye tıklayın.
10. Çalışma alanından çıkmak için **Geri**'ye ve sonra **Bitti**'ye tıklayın.
11. Çalışmanızı kaydetmek için **Çalışma alanını yayımla**'ya tıklayın
12. Gerekli tüm iş akışı eylemlerini kaydetmek için 3 ile 11 arası adımları yineleyin. Tasarım yapacağınız iş akışı eylemlerini kullanılabilir yapacak durumdaki faturaların size atanmasının gerekli olduğunu unutmayın.
13. Not Defteri'ni veya Microsoft Visual Studio'yu açın ve aşağıdaki kodu yapıştırın. Dosyayı .js dosyası olarak kaydedin. Bu kod iki şey gerçekleştirir:
    1.  Mobil listesi sayfasında daha önce eklediğimiz iş akışıyla ilgili ekstra sütunları gizler. Bu sütunları uygulamanın bağlan hakkında bilgisi olması ve bir sonraki adımın gerçekleştirilebilmesi için ekledik.
    2.  Etkin olan iş akışı adımını temel alarak , yalnızca bu eylemleri göstermek için mantık uygular.

Sayfaların ve JS kodundaki diğer denetimlerin adının çalışma alanındakiyle aynı olması gerektiğini unutmayın.

1.  function main(metadataService, dataService, cacheService, $q) {        return {            appInit: function (appMetadata) {                // Hide controls that need to be present, but not visible                metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });              metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });            metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });            },            pageInit: function (pageMetadata, params) {     if (pageMetadata.Name == 'Invoice-details') {                    // Show/hide workflow actions based on workflow step                    metadataService.configureAction('Accept', { visible: true });                    metadataService.configureAction('Approve', { visible: true });                    metadataService.configureAction('Reject', { visible: true });                    metadataService.configureAction('Delegate', { visible: true });                    metadataService.configureAction('Request-change', { visible: true });                    metadataService.configureAction('Recall', { visible: true });                    metadataService.configureAction('Complete', { visible: true });                    metadataService.configureAction('Resubmit', { visible: true });

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

2.  **Mantık** sekmesini seçerek kod dosyasını çalışma alanına yükleyin
3.  Düzenleme modundan çıkmak için **Bitti**'ye tıklayın.
4.  Çalışma alanından çıkmak için **Geri**'ye ve sonra **Bitti**'ye tıklayın.
5.  Çalışmanızı kaydetmek için **Çalışma alanını yayımla**'ya tıklayın

### <a name="vendor-invoice-attachments"></a>Satıcı faturası ekleri

1.  Sayfanın sağ üst kısmındaki **Ayarlar** (dişli) düğmesine ve ardından **Mobil uygulama**'ya tıklayın.
2.  **Düzenle** düğmesine tıklayarak çalışma alanında düzenleme modunu başlatın.
3.  Daha önce oluşturduğunuz **Fatura ayrıntıları** sayfasını seçin ve **Düzenle**'ye tıklayın.
4.  **Belge yönetimi** seçeneğini aşağıda gösterildiği gibi **Evet** olarak ayarlayın. **Not:** Mobil cihazda ekleri göstermek için hiçbir gereklilik yoksa, bu seçeneği varsayılan ayar olan **Hayır** olarak bırakabilirsiniz.
5.  [![docmanagement](./media/docmanagement-216x300.png)](./media/docmanagement.png)
6.  Düzenleme modundan çıkmak için **Bitti**'ye tıklayın.
7.  Çalışma alanından çıkmak için **Geri**'ye ve sonra **Bitti**'ye tıklayın.
8.  Çalışmanızı kaydetmek için **Çalışma alanını yayımla**'ya tıklayın

### <a name="vendor-invoice-line-distributions"></a>Satıcı faturası satırı dağıtımları

Bu senaryonun gereksinimleri yalnızca satır düzeyinde dağıtımlar olacağını ve bir faturada yalnızca bir satır bulunacağını onaylamaktadır. Bu senaryo basit olduğundan, mobil cihazdaki kullanıcı deneyimi de kullanıcının dağıtımları görüntülemek için birçok satırın ayrıntısına bakmasını gerektirmeyecek kadar basit olmalıdır. Dynamics 365 for Operations'daki satıcı faturaları, fatura başlığından tüm dağıtımları gösterme seçeneği içerir. Bu deneyim mobil senaryo için ihtiyacımız olan şeydir. Bu nedenle, mobil senaryonun bu bölümünü tasarlamak için **VendMobileInvoiceAllDistributionTree** sayfasını kullanacağız. 

> [!NOTE] 
> Gereksinimleri bilmek bize hangi belirli sayfayı kullanacağımıza ve senaryoyu tasarlarken tam olarak mobil deneyimi kullanıcı için ne kadar en iyi duruma getireceğimize karar vermede yardımcı olur. İkinci senaryoda, bu senaryo için gereksinimler farklılık gösterdiğinden dağıtımları göstermek için farklı bir sayfa kullanacağız.

1.  Daha önce yaptığınız gibi URL'deki menü öğesi adını değiştirin. Görüntülenen sayfa aşağıdaki resimde gösterilen sayfaya benzemelidir. [![Tüm dağıtımlar sayfası](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Mobil tasarımcıyı **Ayarlar** (dişli) düğmesinden açın.
3.  **Düzenle** düğmesine tıklayarak çalışma alanında düzenleme modunu başlatın. **Not:** İki yeni sayfanın otomatik olarak oluşturulduğunu görürsünüz. Önceki bölümde belge yönetimini açmış olduğunuzdan, sistem bu sayfaları oluşturur. Bu yeni sayfaları yok sayabilirsiniz.
4.  **Sayfa ekle**'ye tıklayın.
5.  **Muhasebeyi görüntüle** gibi bir sayfa başlığı ve **Fatura için muhasebeyi görüntüle** gibi bir açıklama girin.
6.  **Bitti**'ye tıklayın.
7.  **Alan** sekmesinde, **Alanları seçin**'e tıklayın, dağıtımlar sayfasından aşağıdaki alanları seçin ve sonra **Bitti**'ye tıklayın.
    1.  Tutar
    2.  Para Birimi
    3.  Genel muhasebe hesabı

> [!NOTE] 
> Dağıtım ızgarası içim **Açıklama** sütununu seçmedik çünkü bu senaryonun gereksinimleri genişletilmiş fiyatın dağıtımları olacak tek tutar olduğunu onayladı. Bu nedenle, kullanıcının dağıtım yapılacak tutar türünü belirlemek için başka bir alan istemeyecektir. Ancak, sonraki senaryoda, bu bilgiyi **kullanacağız** çünkü bu senaryo için gereksinimler diğer tutar türlerinin (örneğin, satış vergisi) dağıtımları olduğunu belirtiyor.
8.  Düzenleme modundan çıkmak için **Bitti**'ye tıklayın.
9.  Çalışma alanından çıkmak için **Geri**'ye ve sonra **Bitti**'ye tıklayın.
10. Çalışmanızı kaydetmek için **Çalışma alanını yayımla**'ya tıklayın

**Not:****Muhasebeyi görüntüle** mobil sayfası şu anda şimdiye kadar tasarlanan mobil sayfalara bağlı değildir. Kullanıcı mobil cihazda **Fatura ayrıntıları** sayfasından **Muhasebeyi görüntüle** sayfasına gidemeyeceğinden, **Fatura ayrıntıları** sayfasından **Muhasebeyi görüntüle** sayfasına gezinme olanağı sağlamamız gerekir. Bu gezintiyi JavaScript aracılığıyla ek bir mantık kullanarak kurarız.

1.  Daha önce oluşturduğunuz .js dosyasını açın ve aşağıdaki kodda vurgulanan satırları ekleyin. Bu kod iki şey gerçekleştirir:
    1.  Bu, kullanıcıların doğrudan çalışma alanından **Muhasebeyi görüntüle** sayfasına gidememesini garanti etmeye yardımcı olur.
    2.  **Fatura ayrıntıları** sayfasından **Muhasebeyi görüntüle** sayfasına gitme denetimi kurar.

> [!NOTE] 
> Sayfaların ve JS kodundaki diğer denetimlerin adının çalışma alanındakiyle aynı olması gerekir.

1.  function main(metadataService, dataService, cacheService, $q) {        return {            appInit: function (appMetadata) {                // Hide controls that need to be present, but not visible                metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });              metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });                metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });            metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });                // Hide pages not applicable for root navigation                metadataService.hideNavigation('View-accounting');                //Link to view accounting                metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);            },            pageInit: function (pageMetadata, params) {     if (pageMetadata.Name == 'Invoice-details') {                    // Show/hide workflow actions based on workflow step                    metadataService.configureAction('Accept', { visible: true });                    metadataService.configureAction('Approve', { visible: true });                    metadataService.configureAction('Reject', { visible: true });                    metadataService.configureAction('Delegate', { visible: true });                    metadataService.configureAction('Request-change', { visible: true });                    metadataService.configureAction('Recall', { visible: true });                    metadataService.configureAction('Complete', { visible: true });                    metadataService.configureAction('Resubmit', { visible: true });

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

2.  Önceki kodun üzerine yazmak için **Mantık** sekmesini seçerek kod dosyasını çalışma alanına yükleyin
3.  Düzenleme modundan çıkmak için **Bitti**'ye tıklayın.
4.  Çalışma alanından çıkmak için **Geri**'ye ve sonra **Bitti**'ye tıklayın.
5.  Çalışmanızı kaydetmek için **Çalışma alanını yayımla**'ya tıklayın

### <a name="validation"></a>Doğrulama

Mobil cihazınızdan uygulamayı açın ve Dynamics 365 for Operations kurulumunuza bağlanın. Satıcı faturalarının gözden geçirilmek üzere size atandığı şirkette oturum açtığınızdan emin olun. Aşağıdaki eylemleri gerçekleştirebilmeniz gerekir:

-   **Onaylarım** çalışma alanına bakın.
-   **Onaylarım** çalışma alanı ayrıntılarına bakın **Satıcı faturalarım** sayfasını görüntüleyin.
-   **Satıcı faturalarım** sayfasının ayrıntılarına bakın ve size atanmış olan faturaların listesini görün.
-   Faturalardan birinin ayrıntılarına bakın ve fatura başlığı ayrıntılarını ve satır ayrıntılarını görün.
-   Ayrıntılar sayfasında eklerin bağlantısına bakın ve bu bağlantıyı ekler listesine gitmek ve ekleri görüntülemek için kullanın.
-   Ayrıntılar sayfasında, **Muhasebeyi görüntüle** sayfasının bağlantısına bakın ve bu bağlantıyı dağıtımlar sayfasına gitmek ve dağıtımları görüntülemek için kullanın.
-   Ayrıntılar sayfasında aşağıdaki **Eylemler** menüsüne tıklayın ve iş akışı adımı için geçerli olan iş akışı eylemlerini gerçekleştirin.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Fabrikam için karmaşık bir fatura onayı senaryosu tasarlama
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
<td>Kullanıcı mobil deneyimde fatura başlığından hangi alanları ve hangi sırayla görmek ister?</td>
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
<td>Kullanıcı mobil deneyimde fatura satırlarından hangi alanları ve hangi sırayla görmek ister?</td>
<td><ol>
<li>Tedarik kategorisi</li>
<li>Miktar</li>
<li>Birim fiyatı</li>
<li>Satır net tutarı</li>
<li>Vergi beyan tutarı</li>
</ol></td>
</tr>
<tr class="odd">
<td>Faturada kaç adet fatura satırı var? Burada 80-20 kuralını uygulayın ve yüzde 80 için iyileştirme yapın.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Kullanıcılar incelemeler sırasında mobil cihazda muhasebe dağıtımlarını (fatura kodlama) görmek istiyor mu?</td>
<td>Evet</td>
</tr>
<tr class="odd">
<td>Bir fatura satırı için kaç tane hesap dağıtımı (genişletilmiş fiyat, satış vergisi, giderler, vb.) vardır? Yine, 80-20 kuralını uygulayın.</td>
<td>Genişletilmiş fiyat: 2 Satış vergisi: 2 Giderler: 2</td>
</tr>
<tr class="even">
<td>Faturaların fatura başlığında da hesap dağıtımları var mı? Öyleyse, bu hesap dağıtımlarının cihazda kullanılabilir olması gerekir mi?</td>
<td>Kullanılmıyor</td>
</tr>
<tr class="odd">
<td>Kullanıcılar cihazda fatura için ekleri görmek ister mi?</td>
<td>Evet</td>
</tr>
</tbody>
</table>

### <a name="exercise"></a>Alıştırma

Senaryo 1 için senaryo 2 gereksinimleri temel alınarak aşağıdaki çeşitlemeler yapılabilir. Bu bölümü, öğrenme amaçları için tamamlayabileceğiniz bir alıştırma olarak kullanın.

1.  Senaryo 2'de daha fazla fatura satırı beklendiğinden, tasarımda yapılacak aşağıdaki değişiklikler mobil cihazdaki kullanıcı deneyimini en iyi duruma getirmeye yardımcı olacaktır:
    1.  Fatura satırlarını ayrıntılar sayfasında görüntülemek yerine (senaryo 1'de olduğu gibi), kullanıcılar satırları ayrı bir mobil sayfada görüntülemeyi seçebilir.
    2.  Bu senaryoda birden fazla fatura satırı olması beklendiğinden, mobil için dağıtımları tasarlamak amacıyla **VendMobileInvoiceAllDistributionTree** sayfası kullanılırsa (senaryo 1'de olduğu gibi), kullanıcı için satırları dağıtımlarla ilişkilendirmek kafa karıştırıcı olabilir. Bu nedenle, dağıtımlar sayfasını tasarlamak için **VendMobileInvoiceLineDistributionTree** sayfasını kullanın.
    3.  İdeal olarak, bu senaryoda dağıtımların bir fatura satırı bağlamında gösterilmesi gerekir. Bu nedenle, kullanıcının dağıtımlar sayfasını görmek için bir satırın ayrıntılarına inebildiğinden emin olun. Senaryo 1'de başlık ve ayrıntılar sayfaları için yaptığınız gibi, detaylandırma kurmak için sayfa bağlantısı yeteneğini kullanın.

2.  Senaryo 2'deki dağıtımlarda birden fazla tutar türü olması beklendiğinden (satış vergisi, giderler, vb.) tutar türü açıklamasını görüntülemek yararlı olacaktır. (Bu bilgiyi senaryo 1'de atlamıştık.)

## <a name="conclusion"></a>Sonuç
Mobil platform ve uygulama yetenekleri, bir kuruluştaki kullanıcı tabanı için optimize edilmiş mobil senaryoları tasarlamanızı sağlar. Bu konuda sağlanan örnekleri temel alarak, farklı çeşitlemeler deneyebilir ve belirli bir gereksinimi karşılayan farklı deneyimler oluşturabilirsiniz.




