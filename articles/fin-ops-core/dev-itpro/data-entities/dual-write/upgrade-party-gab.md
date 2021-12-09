---
title: Taraf ve genel adres defteri modeline yükseltme
description: Bu konuda, çift yazma verilerinin taraf ve genel adres defteri modeline nasıl yükseltileceği açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 7434c2ed486fe0546a746afdd2c4c4aacdcc3d5c
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817300"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Taraf ve genel adres defteri modeline yükseltme

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[Microsoft Azure Data Factory şablonları](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema), çift yazmadaki aşağıdaki verileri, taraf ve genel adres defteri modellerine çift yazmalı olarak yükseltmenize yardımcı olur: **Firma**, **İlgili Kişi** ve **Satıcı** tabloları ve posta ile elektronik adresler.

Aşağıdaki üç Data Factory şablonu sağlanır. Bunlar, Finance and Operations uygulamaları ve Customer Engagement uygulamalarındaki veriler arasında mutabakat sağlar.

- **[Taraf şablonu](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (Verileri, Taraf-GAB şeması/arm_template.json öğesine çiftli yazacak şekilde yükselt)** – Bu şablon, **Firma**, **İlgili Kişi** ve **Satıcı** verileriyle ilişkili **Taraf** ve **İlgili Kişi** verilerini yükseltmenize yardımcı olur.
- **[Taraf posta adresi şablonu](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) (Verileri, Taraf-GAB şeması/Taraf Posta Adresine yükselt - GAB/arm_template.json öğesine çiftli yazacak şekilde yükselt)** – Bu şablon, **Firma**, **İlgili kişi** ve **Satıcı** verileriyle ilişkili posta adreslerini yükseltmenize yardımcı olur.
- **[Taraf elektronik adres şablonu](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (Verileri, Taraf-GAB şeması/Taraf Elektronik Adresine yükselt - GAB/arm_template.json öğesine çiftli yazacak şekilde yükselt)** – Bu şablon, **Firma**, **İlgili kişi** ve **Satıcı** verileriyle ilişkili elektronik adresleri yükseltmenize yardımcı olur.

İşlemin sonunda, aşağıdaki virgülle ayrılmış değerler (.csv) dosyaları oluşturulur.

| Dosya adı | Amaç |
|---|---|
| FONewParty.csv | Bu dosya, Finance and Operations uygulaması içinde yeni **Taraf** kayıtları oluşturmaya yardımcı olur. |
| ImportFONewPostalAddressLocation.csv | Bu dosya, Finance and Operations uygulamasında yeni **Posta Adresi Konumu** kayıtlarının oluşturulmasına yardımcı olur. |
| ImportFONewPartyPostalAddress.csv | Bu dosya, Finance and Operations uygulamasında yeni **Taraf Posta adresi** kayıtlarının oluşturulmasına yardımcı olur. |
| ImportFONewPostalAddress.csv | Bu dosya, Finance and Operations uygulamasında yeni **Posta Adresi** kayıtlarının oluşturulmasına yardımcı olur. |
| ImportFONewElectronicAddress.csv | Bu dosya, Finance and Operations uygulamasında yeni **Elektronik Adres** kayıtlarının oluşturulmasına yardımcı olur. |

Bu konu, Data Factory şablonlarını kullanma ve verilerinizi yükseltmeyi açıklar. Herhangi bir özelleştirmeleriniz yoksa, şablonları oldukları gibi kullanabilirsiniz. Ancak, **Hesap**, **İlgili Kişi** ve **Satıcı** verileri için özelleştirmeleriniz varsa, şablonları bu konuda açıklandığı şekilde değiştirmeniz gerekir.

> [!IMPORTANT]
> Taraf posta adresi ve Taraf elektronik adres şablonlarını çalıştırabilmeniz için özel yönergeler vardır. Önce Taraf şablonunu, sonra Taraf posta adresi şablonunu ve Taraf elektronik adres şablonunu çalıştırmalısınız.

## <a name="prerequisites"></a>Önkoşullar

Parti ve genel adres defteri modeline yükseltmek için aşağıdaki önkoşulların olması gerekir:

+ Bir [Azure aboneliğiniz](https://portal.azure.com/) olmalıdır.
+ [Şablonlara](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) erişiminiz olmalıdır.
+ Mevcut bir çift yazma müşterisi olmanız gerekir.

## <a name="prepare-for-the-upgrade"></a>Yükseltmek için hazırlık

Yükseltme için aşağıdaki hazırlık gereklidir:

+ **Tam eşitleme:** Hem Finance and Operations ortamı hem de Customer Engagement ortamı, **Firma (Müşteri)**, **İlgili kişi** ve **Satıcı** tabloları için tam olarak eşitlenmiş durumda bulunur.
+ **Tümleştirme anahtarları:** Müşteri etkileşimi uygulamalarındaki **Hesap (Müşteri)**, **İlgili Kişi** ve **Satıcı** tabloları kullanıma hazır gönderilen tümleştirme anahtarlarını kullanıyor. Tümleştirme anahtarlarını özelleştirdiyseniz, şablonu özelleştirmeniz gerekir.
+ **Taraf numarası:** Yükseltilecek tüm **Hesap (Müşteri)**, **İlgili Kişi** ve **Satıcı** kayıtlarında bir taraf numarası bulunur. Taraf numarası olmayan kayıtlar yok sayılır. Bu kayıtları yükseltmek istiyorsanız, yükseltme işlemine başlamadan önce onlara bir taraf numarası ekleyin.
+ **Sistem kesintisi:** Yükseltme işlemi sırasında, hem Finance and Operations ortamı hem de Customer Engagement ortamını çevrimdışına almanız gerekir.
+ **Anlık görüntü:** Hem Finance and Operations uygulamaları hem de Customer Engagement uygulamalarının anlık görüntüsünü alın. Gerekirse önceki durumu geri yüklemek için anlık görüntüleri kullanabilirsiniz.

## <a name="deployment"></a>Dağıtım

1. [Dynamics-365-FastTrack-Implementation-Assets](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) konumundan şablonları indirin.
2. [Azure portalında](https://portal.azure.com/) adresinden oturum açın.
3. [Kaynak grubu](/azure/azure-resource-manager/management/manage-resource-groups-portal) oluşturun.
4. Oluşturduğunuz kaynak grubunda bir [depolama hesabı](/azure/storage/common/storage-account-create?tabs=azure-portal) oluşturun.
5. Oluşturduğunuz kaynak grubunda bir [veri fabrikası](/azure/data-factory/quickstart-create-data-factory-portal) oluşturun.
6. Veri fabrikasını açın ve **Yaz ve İzle** kutucuğunu seçin.
7. **Yönet** sekmesinde **ARM şablonu** seçeneğini belirleyin.
8. **Taraf** şablonunu içe aktarmak için **ARM şablonunu içer aktar**'ı seçin.
9. Şablonu veri fabrikasına aktarın. **Proje ayrıntıları** ve **Kurulum ayrıntıları** için aşağıdaki değerleri girin.

    | Alan | Değer |
    |---|---|
    | Abonelik | Azure aboneliği |
    | Kaynak grubu | Altında depolama hesabı oluşturulan aynı kaynağı sağlayın. |
    | Bölge | Bölge |
    | Fabrika Adı | Fabrika adı |
    | FO Linked Service_service Principal Key | Uygulamanın anahtarı |
    | Azure Blob Storage_connection String | Azure Blob depolama bağlantı dizesi |
    | Dynamics Crm Linked Service_password | Kullanıcı adı olarak belirttiğiniz kullanıcı hesabının parolası |
    | FO Linked Service_properties_type Properties_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO Linked Service_properties_type Properties_tenant | Uygulamanızın altında bulunduğu kiracı bilgileri (etki alanı adı veya kiracı kimliği) |
    | FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO Linked Service_properties_type Properties_service Principal Id | Uygulamanın istemci kimliği |
    | Dynamics Crm Linked Service_properties_type Properties_username | Dynamics 365'e bağlanmak için kullanılan kullanıcı adı |

    Daha fazla bilgi edinmek için aşağıdaki konulara bakın:

    - [Her ortam için kaynak yöneticisi şablonunu el ile yükseltme](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Bağlı hizmet özellikleri](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Azure Data Factory kullanarak veri kopyalama](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Dağıtımdan sonra, veri fabrikasının bağlantılı hizmetini, veri kümelerini ve veri akışını doğrulayın.

    ![Veri kümeleri, veri akışı ve bağlantılı hizmet.](media/data-factory-validate.png)

11. **Yönet**'e gidin. **Bağlantılar** altından, **Bağlantılı Hizmet**'i seçin. Sonra **DynamicsCrmLinkedService** öğesini seçin. **Bağlantılı hizmeti düzenle (Dynamics CRM)** iletişim kutusunda aşağıdaki değerleri girin.

    | Alan | Değer |
    |---|---|
    | Ad | DynamicsCrmLinkedService |
    | Tanım | Varlık verilerini getirmek üzere CRM kurulumuyla bağlantı kurulacak bağlantılı hizmetler |
    | Tümleştirme çalışma zamanı aracılığıyla bağlan | AutoResolvelntegrationRuntime |
    | Dağıtım türü | Çevrimiçi |
    | Hizmet URI'si | `https://<organization-name>.crm[x].dynamics.com` |
    | Kimlik doğrulaması türü | Office365 |
    | Kullanıcı adı | |
    | Parola veya Azure Key Vault | Parola |
    | Parola | |

## <a name="prepare-to-run-the-data-factory-templates"></a>Data Factory şablonlarını çalıştırmaya hazırla

Bu bölümde, Taraf posta adresi ve Taraf elektronik adres Data Factory şablonlarını çalıştırmadan önce gereken ayarlar açıklanmaktadır.

### <a name="setup-to-run-the-party-postal-address-template"></a>Taraf posta adresi şablonunu çalıştırmak için kurulum

1. Customer Engagement uygulamalarına oturum açın ve **Ayarlar** \> **Kişiselleştirme Ayarları**'na gidin. **Genel** sekmesinde, sistem yöneticisi hesabı için saat dilimini konfigüre edin. Posta adreslerinin "geçerlilik başlangıcı" ve "geçerlilik sonu" tarihlerini Finance and Operations uygulamalarından güncelleştirmek için saat diliminin Eşgüdümlü Evrensel Saat'te (UTC) olması gerekir.

    ![Sistem yöneticisi hesabı için saat dilimi ayarı.](media/ADF-1.png)

2. Data Factory'de, **Yönet** sekmesindeki **Genel parametreler** altında aşağıdaki genel parametreyi oluşturun.

    | Numara | Ad | Tür | Değer |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | dize | Bu parametre, yeni oluşturulan posta adreslerine bir seri numarası öneki ekler. Finance and Operations uygulamaları ve Customer Engagement uygulamalarında, posta adresleriyle çakışmayan bir dize sağladığınızdan emin olun. Örneğin, **ADF-PAD-** kullanın. |

    ![PostalAddressIdPrefix genel parametresi, Yönet sekmesinde oluşturulur.](media/ADF-2.png)

3. Tamamladıktan sonra **Tümünü yayımla**'yı seçin.

    ![Tümünü yayımla düğmesi.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Taraf elektronik adresi şablonunu çalıştırmak için kurulum

1. Data Factory'de, **Yönet** sekmesindeki **Genel parametreler** altında aşağıdaki genel parametreleri oluşturun.

    | Numara | Ad | Tür | Değer |
    |---|---|---|---|
    | 1 | IsFOSource | bool | Bu parametre, çakışmalar durumunda hangi birincil sistem adreslerinin değiştirildiğini belirler. Değer **doğru** ise, Finance and Operations uygulamalarındaki birincil adresler, Customer Engagement uygulamalarındaki birincil adreslerin yerini alır. Değer **yanlış** ise, Customer Engagement uygulamalarındaki birincil adresler, Finance and Operations uygulamalarındaki birincil adreslerin yerini alır. |
    | 2 | ElectronicAddressIdPrefix | dize | Bu parametre, yeni oluşturulan elektronik adreslere bir seri numarası öneki ekler. Finance and Operations uygulamaları ve Customer Engagement uygulamalarında, elektronik adreslerle çakışmayan bir dize sağladığınızdan emin olun. Örneğin, **ADF-EAD-** kullanın. |

    ![Yönet sekmesinde oluşturulan IsFOSource ve ElectronicAddressIdPrefix genel parametreleri.](media/ADF-4.png)

2. Tamamladıktan sonra **Tümünü yayımla**'yı seçin.

## <a name="run-the-templates"></a>Şablonları çalıştır

1. Finance and Operations uygulamasını kullanan aşağıdaki **Hesap**, **İlgili Kişi** ve **Satıcı** çift yazma eşlemelerini durdurun:

    + Müşteriler V3 (hesaplar)
    + Müşteriler V3(ilgili kişiler)
    + CDS İlgili Kişileri V2(ilgili kişiler)
    + CDS İlgili Kişileri V2(ilgili kişiler)
    + Satıcı V2 (msdyn_vendor)

2. Dataverse'de haritaların **msdy_dualwriteruntimeconfig** tablosundan kaldırıldığından emin olun.
3. AppSource'tan [Çift Yazma Taraf ve Genel Adres Defteri Çözümleri](https://aka.ms/dual-write-gab)'ni yükleyin.
4. Finance and Operations uygulamasında, aşağıdaki tablolar veri içeriyorsa bu tablolar için **Başlangıç Eşitlemesi**'ni çalıştırın:

    + Selamlamalar
    + Kişisel karakter türleri
    + Kapanış sözleri
    + İlgili kişi unvanları
    + Karar verici roller
    + Bağlılık programı düzeyleri

5. Customer Engagement uygulamasında aşağıdaki eklenti adımlarını devre dışı bırakın:

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

    + Customeraddress

        + Oluştur

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: customeraddress oluşumu

        + Güncelleştirme

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: customeraddress güncelleştirmesi

        + Dil

            + Microsoft.Dynamics.GABExtended.Plugins.DeleteCustomerAddress: customeraddress silinmesi

    + msdyn_partypostaladdress

        + Oluştur

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress oluşumu
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress oluşumu

        + Güncelleştirme

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress güncelleştirmesi
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress güncelleştirmesi

    + msdyn_postaladdress

        + Oluştur

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: msdyn_postaladdress oluşumu
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: msdyn_postaladdress oluşumu
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress oluşumu

        + Güncelleştirme

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: msdyn_postaladdress güncelleştirmesi
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress güncelleştirmesi

    + msdyn_partyelectronicaddress

        + Oluştur

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress oluşumu

        + Güncelleştirme

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress güncelleştirmesi

        + Dil

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: msdyn_partyelectronicaddress silinmesi

6. Müşteri etkileşimi uygulamasında aşağıdaki iş akışlarını devre dışı bırakın.

    + Hesaplar Tablosunda Satıcılar oluşturma
    + Hesaplar Tablosunda Satıcılar oluşturma
    + İlgili Kişiler Tablosunda Kişi türünde Satıcılar oluşturma
    + Satıcılar Tablosunda Kişi türünde Satıcılar oluşturma
    + Hesaplar Tablosunda Satıcıları Güncelleştirme
    + Satıcılar Tablosunda Satıcıları Güncelleştirme
    + İlgili Kişiler Tablosunda Kişi türünde Satıcıları Güncelleştirme
    + Satıcılar Tablosunda Kişi türünde Satıcıları Güncelleştirme

7. Veri fabrikasında, aşağıdaki ilüstrasyonda gösterildiği şekilde **Şimdi tetikle**'yi seçerek şablonu çalıştırın. Bu işlemin tamamlanması, veri hacmine göre birkaç saat sürebilir.

    ![Şablonu çalıştırma.](media/data-factory-trigger.png)

    > [!NOTE]
    > **Hesap**, **İlgili Kişi** ve **Satıcı** için özelleştirmeleriniz varsa, şablonu değiştirmeniz gerekir.

8. Finance and Operations uygulamasına yeni **Taraf** kayıtlarını içe aktarın.

    1. Azure Blob depolamadan **FONewParty.csv** dosyasını indirin. Yol şöyledir: **partybootstrapping/output/FONewParty.csv**.
    2. **FONewParty.csv** dosyasını bir Excel dosyasına dönüştürüp Excel dosyasını Finance and Operations uygulamasına aktarın. Alternatif olarak, CSV içe aktarma işlemi sizin için uygunsa, .csv dosyasını doğrudan içe aktarabilirsiniz. Bu adımın tamamlanması, veri hacmine göre birkaç saat sürebilir. Daha fazla bilgi için bkz. [Verileri içeri ve dışarı aktarma işlerine genel bakış](../data-import-export-job.md).

    ![Dataverse Taraf kayıtlarını içe aktarma.](media/data-factory-import-party.png)

9. Data Factory'de, Taraf posta adresi ve Taraf elektronik adres şablonlarını art arda çalıştırın.

    + Taraf posta adresi şablonu, Customer Engagement uygulamasında bulunan tüm posta adresi kayıtlarını çıkarır ve bunları ilgili **Firma**, **İlgili kişi** ve **Satıcı** kayıtlarıyla ilişkilendirir. Ayrıca üç .csv dosyası da oluşturur: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv ve ImportFONewPostalAddress.csv.
    + Taraf elektronik adres şablonu, Customer Engagement uygulamasında bulunan tüm elektronik adres kayıtlarını çıkarır ve bunları ilgili **Firma**, **İlgili kişi** ve **Satıcı** kayıtlarıyla ilişkilendirir. Ayrıca bir .csv dosyası oluşturur: ImportFONewElectronicAddress.csv.

    ![Taraf posta adresi ve Taraf elektronik adres şablonlarını çalıştırma.](media/ADF-7.png)

10. Bu verilerle Finance and Operations uygulamasını güncelleştirmek için .csv dosyalarını bir Excel çalışma kitabına dönüştürmeniz ve bunu [Finance and Operations uygulamasına aktarmanız gerekir](/data-entities/data-import-export-job). Alternatif olarak, CSV içe aktarma işlemi sizin için uygunsa, .csv dosyalarını doğrudan içe aktarabilirsiniz. Bu adımın tamamlanması, hacme göre birkaç saat sürebilir.

    ![İçe aktarma başarılı.](media/ADF-8.png)

11. Customer Engagement uygulamasında aşağıdaki eklenti adımlarını devre dışı etkinleştirin:

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

    + msdyn_partypostaladdress

        + Oluştur

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress oluşumu
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress oluşumu

        + Güncelleştirme

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress güncelleştirmesi
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress güncelleştirmesi

    + msdyn_postaladdress

        + Oluştur

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: msdyn_postaladdress oluşumu
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: msdyn_postaladdress oluşumu
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress oluşumu

        + Güncelleştirme

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: msdyn_postaladdress güncelleştirmesi
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: msdyn_postaladdress güncelleştirmesi
 
    + msdyn_partyelectronicaddress

        + Oluştur

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress oluşumu

        + Güncelleştirme

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress güncelleştirmesi

        + Dil

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: msdyn_partyelectronicaddress silinmesi

12. Customer Engagement uygulamasında, önceki adımlarda devre dışı bıraktıysanız aşağıdaki iş akışlarını etkinleştirin:

    + Hesaplar Tablosunda Satıcılar oluşturma
    + Hesaplar Tablosunda Satıcılar oluşturma
    + İlgili Kişiler Tablosunda Kişi türünde Satıcılar oluşturma
    + Satıcılar Tablosunda Kişi türünde Satıcılar oluşturma
    + Hesaplar Tablosunda Satıcıları Güncelleştirme
    + Satıcılar Tablosunda Satıcıları Güncelleştirme
    + İlgili Kişiler Tablosunda Kişi türünde Satıcıları Güncelleştirme
    + Satıcılar Tablosunda Kişi türünde Satıcıları Güncelleştirme

13. **Taraf** kaydı ile ilgili haritaları [Taraf ve genel adres defteri](party-gab.md)'nde belirtildiği şekilde çalıştırın.

## <a name="explanation-of-the-data-factory-templates"></a>Data Factory şablonlarının açıklaması

Bu bölüm, sizi her bir Data Factory şablonundaki adımlara götürür.

### <a name="steps-in-the-party-template"></a>Taraf şablonundaki adımlar

1. 1 ile 6 arasındaki adımlar, çift yazma için etkinleştirilen şirketleri tanımlar ve bunlar için bir filtre yan tümcesi oluşturur.
2. 7-1 ile 7-9 arasındaki adımlar, hem Finance and Operations uygulaması hem de Customer Engagement uygulamasından verileri alır ve bu verileri yükseltme için aşamalandırır.
3. 8 ile 9 arasındaki adımlar; Finance and Operations uygulaması ve Customer Engagement uygulaması arasında **Firma**, **İlgili Kişi**, ve **Satıcı** kayıtları için taraf numarasını kıyaslar. Taraf numarası olmayan kayıtlar atlanır.
4. Adım 10, Customer Engagement uygulamasında ve Finance and Operations uygulamasında oluşturulması gereken taraf kayıtları için iki .csv dosyası oluşturur.

    - **FOCDSParty.csv** – Bu dosya, şirketin çift yazma için etkinleştirilmiş olup olmamasına bakmaksızın her iki sistemde bulunan tüm taraf kayıtlarını içerir.
    - **FONewParty.csv** – Bu dosya, Dataverse'ün bilincinde olduğu taraf kayıtlarının bir alt kümesini oluşturur (örneğin **Aday müşteri** türünün hesapları).

5. Adım 11, tarafları Customer Engagement uygulamasında oluşturur.
6. Adım 12, Customer Engagement uygulamasına ait tarafların genel benzersiz tanımlayıcılarını (GUID'ler) alır ve bunları sonraki adımlarda bulunan **Firma**, **İlgili kişi** ve **Satıcı** kayıtlarıyla ilişkilendirilebilecek şekilde aşamalar.
7. Adım 13, **Firma**, **İlgili kişi** ve **Satıcı** kayıtlarını taraf GUID'leri ile ilişkilendirir.
8. 14-1-ile 14-3 arası adımlar Customer Engagement uygulamasında **Firma**, **İlgili kişi** ve **Satıcı** kayıtlarını taraf GUID'leri ile güncelleştirir.
9. 15-1-ile 15-3 arası adımlar; **Firma**, **İlgili kişi** ve **Satıcı** kayıtları için **Taraf için İlgili Kişi**'yi hazırlar.
10. 16-1 ile 16-7 arasındaki adımlar, selamlama ve kişisel karakter türleri gibi başvuru verilerini alır ve **Taraf için İlgili Kişi** kayıtlarıyla ilişkilendirir.
11. Adım 17; **Firma**, **İlgili kişi** ve **Satıcı** kayıtları için **Taraf için İlgili Kişi**'yi birleştirir.
12. Adım 18, **Taraf için İlgili Kişi** kayıtlarını, Customer Engagement uygulamasına aktarır.

### <a name="steps-in-the-party-postal-address-template"></a>Taraf posta adresi şablonundaki adımlar

1. 1-1 ile 1-10 arasındaki adımlar, hem Finance and Operations uygulaması hem de Customer Engagement uygulamasından verileri alır ve bu verileri yükseltme için aşamalandırır.
2. Adım 2'de, posta adresi ve taraf posta adresini birleştirerek Finance and Operations uygulamasındaki posta adresi verileri normalleştirilir.
3. Adım 3, Customer Engagement uygulamasından hesap, ilgili kişi ve satıcı adresi verilerinde yinelenleri siler ve birleştirir.
4. Adım 4; firma, ilgili kişi ve satıcı adreslerine dayalı yeni adres verileri oluşturmak üzere Finance and Operations uygulaması için .csv dosyaları oluşturur.
5. Adım 5-1, Customer Engagement uygulaması için, hem Finance and Operations uygulamasına hem de Customer Engagement uygulamasına dayalı olarak tüm adres verilerini oluşturmak üzere .csv dosyaları oluşturur.
6. Adım 5-2, .csv dosyalarını el ile içe aktarmak için Finance and Operations içe aktarma biçimine dönüştürür.

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. Adım 6, posta adresi toplama verilerini Customer Engagement uygulamasına aktarır.
8. Adım 7, posta adresi toplama verilerini Customer Engagement uygulamasından alır.
9. Adım 8, müşteri adres verilerini oluşturur ve posta adresi toplama kodunu ilişkilendirir.
10. 9-1 ile 9-2 arasındaki adımlar, taraf ve posta adresi koleksiyon kimliklerini posta adresleriyle ve taraf posta adresleriyle ilişkilendirir.
11. 10-1 ile 10-3 arasındaki adımlar, Customer Engagement uygulaması şirket adreslerini, posta adreslerini ve parti posta adreslerini içe aktarır.

### <a name="steps-in-the-party-electronic-address-template"></a>Taraf elektronik adres şablonundaki adımlar

1. 1-1 ile 1-5 arasındaki adımlar, hem Finance and Operations uygulaması hem de Customer Engagement uygulamasından verileri alır ve bu verileri yükseltme için aşamalandırır.
2. Adım 2; elektronik adresleri firma, ilgili kişi ve satıcı varlıklarından alınan Customer Engagement uygulamasında birleştirir.
3. Adım 3, Customer Engagement uygulaması ve Finance and Operations uygulamasından alınan birincil elektronik adres verilerini birleştirir.
4. Adım 4, .csv dosyaları oluşturur.

    - Firma, ilgili kişi ve satıcı adreslerine göre Finance and Operations uygulaması için yeni elektronik adres verileri oluşturun.
    - Finance and Operations uygulamasındaki elektronik adrese, firmaya, ilgili kişiye ve satıcı adreslerine göre, Customer Engagement uygulaması için yeni elektronik adres verileri oluşturun.

5. Adım 5-1, elektronik adresleri Customer Engagement uygulamasına aktarır.
6. Adım 5-2, Customer Engagement uygulamasında firmaların ve ilgili kişilerin birincil adreslerini güncelleştirmek için .csv dosyaları oluşturur.
7. 6-1 ile 6-2 arasındaki adımlar, Customer Engagement uygulamasına firmaları ve ilgili kişi birincil adreslerini içe aktarır.

## <a name="troubleshooting"></a>Sorun Giderme

1. İşlem başarısız olursa, Data Factory'yi yeniden çalıştırın. Başarısız olan etkinlikten başlayın.
2. Data Factory tarafından oluşturulan bazı dosyalar, veri doğrulaması için kullanılabilir.
3. Data Factory, .csv dosyaları temel alınarak çalışır. Bu nedenle, bir alan değerine virgül dahil edilirse sonuçları karıştırabilir. Alan değerlerinden tüm virgülleri kaldırmalısınız.
4. **İzleme** sekmesi, tüm adımlar ve işlenen veriler hakkında bilgi sağlar. Hata ayıklamak için belirli bir adımı seçin.

    ![İzleme sekmesi.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Şablon hakkında daha fazla bilgi edinin

Şablon hakkında ek bilgiler için bkz. [Azure Data Factory için Yorumlar şablonu beni oku](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
