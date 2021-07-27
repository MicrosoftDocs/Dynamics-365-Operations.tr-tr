---
title: Taraf ve genel adres defteri modeline yükseltme
description: Bu konuda, çift yazma verilerinin taraf ve genel adres defteri modeline nasıl yükseltileceği açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 6662b6cad53c832e15fb27b435e277840afd8097
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346558"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Taraf ve genel adres defteri modeline yükseltme

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[Microsoft Azure Data Factory şablonu](https://aka.ms/dual-write-gab-adf), çift yazmadaki mevcut **Hesap**, **İlgili Kişi** ve **Satıcı** tablo verilerini taraf ve genel adres defteri modeline yükseltmenize yardımcı olur. Şablon, Finance and Operations uygulamaları ve müşteri etkileşimi uygulamalarındaki veriler arasında mutabakat sağlar. İşlemin sonunda, **Taraf** kayıtlarına ait **Taraf** ve **İlgili Kişi** alanları oluşturulur ve müşteri etkileşimi uygulamalarındaki **Hesap**, **İLgili Kişi** ve **Satıcı** kayıtlarıyla ilişkilendirilir. Finance and Operations uygulaması içinde yeni **Taraf** kayıtları oluşturmak için bir .csv dosyası (`FONewParty.csv`) oluşturulur. Bu konu, Data Factory şablonunu kullanma ve verilerinizi yükseltme yönergelerini sağlamaktadır.

Herhangi bir özelleştirmeleriniz yoksa, şablonu olduğu gibi kullanabilirsiniz. **Hesap**, **İlgili Kişi** ve **Satıcı** için özelleştirmeleriniz varsa aşağıdaki yönergeleri kullanarak şablonu değiştirmeniz gerekir.

> [!NOTE]
> Şablon yalnızca **Taraf** verilerini yükseltmeye yardımcı olur. Gelecek bir sürümde, posta ve elektronik adresler de dahil edilecektir.

## <a name="prerequisites"></a>Önkoşullar

Parti ve genel adres defteri modeline yükseltmek için aşağıdaki önkoşullar gereklidir:

+ [Azure aboneliği](https://portal.azure.com/)
+ [Şablona erişim](https://aka.ms/dual-write-gab-adf)
+ Mevcut bir çift yazma müşterisi olmanız gerekir.

## <a name="prepare-for-the-upgrade"></a>Yükseltmek için hazırlık
Yükseltmeye hazırlanmak için aşağıdaki etkinlikler gereklidir:

+ **Tamamen eşitlenmiş**: Her iki ortam **Hesap (Müşteri)**, **İlgili Kişi** ve **Satıcı** için tamamen eşitlenmiş durumda.
+ **Tümleştirme anahtarları**: Müşteri etkileşimi uygulamalarındaki **Hesap (Müşteri)**, **İlgili Kişi** ve **Satıcı** tabloları kullanıma hazır gönderilen tümleştirme anahtarlarını kullanıyor. Tümleştirme anahtarlarını özelleştirdiyseniz, şablonu özelleştirmeniz gerekir.
+ **Taraf numarası**: Yükseltilecek tüm **Hesap (Müşteri)**, **İlgili Kişi** ve **Satıcı** kayıtlarında bir **Taraf** numarası bulunur. **Taraf** numarası olmayan kayıtlar yok sayılır. Bu kayıtları yükseltmek istiyorsanız, yükseltme işlemine başlamadan önce onlara bir **Taraf** numarası ekleyin.
+ **Sistem kesintisi**: Yükseltme işlemi sırasında, hem Finance and Operations hem de Customer Engagement uygulamalarını çevrimdışına almanız gerekir.
+ **Anlık görüntü**: Hem Finance and Operations hem de Customer Engagement uygulamalarının anlık görüntüsünü alın. Gerekirse önceki durumu geri yüklemek için anlık görüntüleri kullanın.

## <a name="deployment"></a>Dağıtım

1. [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf) konumundan şablonu indirin.

2. [Microsoft Azure](https://portal.azure.com/)'da oturum açın.

3. [Kaynak grubu](/azure/azure-resource-manager/management/manage-resource-groups-portal) oluşturun.

4. Oluşturduğunuz kaynak grubunda bir [depolama hesabı](/azure/storage/common/storage-account-create?tabs=azure-portal) oluşturun.

5. Yukarıda oluşturduğunuz kaynak grubunda bir [veri fabrikası](/azure/data-factory/quickstart-create-data-factory-portal) oluşturun.

6. Veri fabrikasını açın ve **Yaz ve İzle** kutucuğunu seçin.

7. **Yönet** sekmesinde **ARM şablonu** seçeneğini belirleyin.

8. **Taraf** şablonunu içe aktarmak için **ARM şablonunu içer aktar**'ı seçin.

9. Şablonu veri fabrikasına aktarın. **Proje ayrıntıları** ve **Kurulum ayrıntıları** için aşağıdaki değerleri girin.

    Alan | Değer
    ---|---
    Abonelik | Azure aboneliği
    Kaynak grubu | Altında depolama hesabı oluşturulan kaynağı sağlayın.
    Bölge | Bölge belirtin.
    Fabrika Adı | Fabrika adını belirtin.
    FO Linked Service_service Principal Key | Uygulamanın anahtarını belirtin.
    Azure Blob Storage_connection String | Azure Blob depolama bağlantı dizesi.
    Dynamics Crm Linked Service_password | Kullanıcı adı olarak belirttiğiniz kullanıcı hesabının parolası.
    FO Linked Service_properties_type Properties_url  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    FO Linked Service_properties_type Properties_tenant | Uygulamanızın altında bulunduğu kiracı bilgilerini (etki alanı adı veya kiracı kimliği) belirtin.
    FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com`
    FO Linked Service_properties_type Properties_service Principal Id | Uygulamanın istemci kimliğini belirtin.
    Dynamics Crm Linked Service_properties_type Properties_username | Dynamics 365'e bağlanmak için kullanıcı adı.

    Daha fazla bilgi için aşağıdaki konulardan birine başvurun: 
    
    - [Her ortam için kaynak yöneticisi şablonunu el ile yükseltme](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Bağlı hizmet özellikleri](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Azure Data Factory kullanarak veri kopyalama](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Dağıtımdan sonra, veri fabrikasının bağlantılı hizmetini, veri kümelerini ve veri akışını doğrulayın.

   ![Veri kümeleri, veri akışı ve bağlantılı hizmet.](media/data-factory-validate.png)

11. **Yönet**'e gidin. **Bağlantılar** altından, **Bağlantılı Hizmet**'i seçin. **DynamicsCrmLinkedService** öğesini seçin. **Bağlantılı hizmeti düzenle ( Dynamics CRM)** formuna aşağıdaki değerleri girin.

    Alan | Değer
    ---|---
    Kuruluş adı | DynamicsCrmLinkedService
    Tanım | Varlık verilerini getirmek üzere CRM kurulumuyla bağlantı kurulacak bağlantılı hizmetler
    Tümleştirme çalışma zamanı aracılığıyla bağlan | AutoResolvelntegrationRuntime
    Dağıtım türü | Çevrimiçi
    Hizmet URI'si | `https://<organization-name>.crm[x].dynamics.com`
    Kimlik doğrulaması türü | Office365
    Kullanıcı adı |
    Parola veya Azure Key Vault | Parola
    Parola |

## <a name="run-the-template"></a>Şablonu çalıştır

1. Finance and Operations uygulamasını kullanarak aşağıdaki **Hesap**, **İlgili Kişi** ve **Satıcı** çift yazma eşlemelerini durdurun.

    + Müşteriler V3 (hesaplar)
    + Müşteriler V3(ilgili kişiler)
    + CDS İlgili Kişileri V2(ilgili kişiler)
    + CDS İlgili Kişileri V2(ilgili kişiler)
    + Satıcı V2 (msdyn_vendor)

2. Dataverse'de haritaların `msdy_dualwriteruntimeconfig` tablosundan kaldırıldığından emin olun.

3. AppSource'tan [Çift Yazma Taraf ve Genel Adres Defteri Çözümleri](https://aka.ms/dual-write-gab)'ni yükleyin.

4. Finance and Operations uygulamasında, aşağıdaki tablolar veri içeriyorsa bu tablolar için **Başlangıç Eşitlemesi**'ni çalıştırın.

    + Selamlamalar
    + Kişisel karakter türleri
    + Kapanış sözleri
    + İlgili kişi unvanları
    + Karar verici roller
    + Bağlılık programı düzeyleri

5. Müşteri etkileşimi uygulamasında aşağıdaki eklenti adımlarını devre dışı bırakın.

    + Hesap Güncelleştirme
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Hesap güncelleştirmesi
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Hesap güncelleştirmesi
    + İlgili Kişi Güncelleştirmesi
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: İlgili kişi güncelleştirmesi
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: İlgili kişi güncelleştirmesi
    + msdyn_party Güncelleştirmesi
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party güncelleştirmesi
    + msdyn_vendor Güncelleştirmesi
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor güncelleştirmesi

6. Müşteri etkileşimi uygulamasında aşağıdaki iş akışlarını devre dışı bırakın.

    + Hesaplar Tablosunda Satıcılar oluşturma
    + Hesaplar Tablosunda Satıcılar oluşturma
    + İlgili Kişiler Tablosunda Kişi türünde Satıcılar oluşturma
    + Satıcılar Tablosunda Kişi türünde Satıcılar oluşturma
    + Hesaplar Tablosunda Satıcıları Güncelleştirme
    + Satıcılar Tablosunda Satıcıları Güncelleştirme
    + İlgili Kişiler Tablosunda Kişi türünde Satıcıları Güncelleştirme
    + Satıcılar Tablosunda Kişi türünde Satıcıları Güncelleştirme

7. Veri fabrikasında, aşağıdaki görüntüde gösterildiği şekilde **Şimdi tetikle**'yi seçerek şablonu çalıştırın. Bu işlemin tamamlanması veri hacmine göre birkaç saat sürebilir.

    ![Tetik çalıştırması.](media/data-factory-trigger.png)

    > [!NOTE]
    > **Hesap**, **İlgili Kişi** ve **Satıcı** için özelleştirmeleriniz varsa şablonu değiştirmeniz gerekir.

8. Finance and Operations uygulamasında yeni **Taraf** kayıtlarını içe aktarın.

    + Azure blob depolamadan `FONewParty.csv` dosyasını indirin. Yol: `partybootstrapping/output/FONewParty.csv`.
    + `FONewParty.csv` dosyasını bir Excel dosyasına dönüştürüp Excel dosyasını Finance and Operations uygulamasına aktarın. csv içe aktarma işlemi sizin için uygunsa, csv dosyasını doğrudan içe aktarabilirsiniz. Veri hacmine bağlı olarak içe aktarma birkaç saat sürebilir. Daha fazla bilgi için bkz. [Verileri içeri ve dışarı aktarma işlerine genel bakış](../data-import-export-job.md).

    ![Dataverse taraf kayıtlarını içe aktarma.](media/data-factory-import-party.png)

9. Müşteri etkileşimi uygulamalarında aşağıdaki eklenti adımlarını devre dışı etkinleştirin:

    + Hesap Güncelleştirme
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Hesap güncelleştirmesi
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Hesap güncelleştirmesi
    + İlgili Kişi Güncelleştirmesi
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: İlgili kişi güncelleştirmesi
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: İlgili kişi güncelleştirmesi
    + msdyn_party Güncelleştirmesi
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party güncelleştirmesi
    + msdyn_vendor Güncelleştirmesi
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor güncelleştirmesi

10. Müşteri etkileşimi uygulamalarında, önceki adımlarda devre dışı bıraktıysanız aşağıdaki iş akışlarını etkinleştirin:

    + Hesaplar Tablosunda Satıcılar oluşturma
    + Hesaplar Tablosunda Satıcılar oluşturma
    + İlgili Kişiler Tablosunda Kişi türünde Satıcılar oluşturma
    + Satıcılar Tablosunda Kişi türünde Satıcılar oluşturma
    + Hesaplar Tablosunda Satıcıları Güncelleştirme
    + Satıcılar Tablosunda Satıcıları Güncelleştirme
    + İlgili Kişiler Tablosunda Kişi türünde Satıcıları Güncelleştirme
    + Satıcılar Tablosunda Kişi türünde Satıcıları Güncelleştirme

11. **Taraf** ile ilgili haritaları [Taraf ve genel adres defteri](party-gab.md)'nde belirtildiği şekilde çalıştırın.

## <a name="troubleshooting"></a>Sorun Giderme

1. İşlem başarısız olursa, başarısız olan etkinlikten başlayarak veri fabrikasını yeniden çalıştırın.
2. Bazı dosyalar veri doğrulama amacıyla kullanabileceğiniz veri fabrikası tarafından oluşturulur.
3. Veri fabrikası, virgülle sınırlanmış csv dosyaları temel alınarak çalışır. Virgül içeren bir alan değeri varsa, sonuçlarla karışabilir. Virgülleri kaldırmanız gerekir.
4. **İzleme** sekmesi, tüm adımlar ve işlenen veriler hakkında bilgi sağlar. Hata ayıklamak için belirli bir adımı seçin.

    ![İzleme sekmesi.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Şablon hakkında daha fazla bilgi edinin

Şablon hakkında ek bilgileri [Azure Data Factory için Yorumlar şablonu benioku](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md)'da bulabilirsiniz.
