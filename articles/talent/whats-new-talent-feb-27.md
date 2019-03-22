---
title: Dynamics 365 for Talent'daki yenilikler veya değişiklikler (27 Şubat 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 02/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b622276000c56a5af1bb258dbc3c6c4a56af4d20
ms.sourcegitcommit: 479b8cda7e411830bf1f579fab3692c980dcf850
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/08/2019
ms.locfileid: "783038"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-27-2019"></a>Dynamics 365 for Talent'daki yenilikler veya değişiklikler (27 Şubat 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içerir.

## <a name="changes-in-onboard"></a>Onboard'daki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içerir.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2163 için geçerlidir

### <a name="add-a-custom-fields-menu-item-to-system-administration"></a>Sistem yönetimine bir Özel alanlar menü öğesi ekle

**Özel alanlar** menüsüne gezinti, **Sistem yönetimi** çalışma alanına eklenmiştir.

### <a name="hide-the-import-and-create-options-for-new-mobile-applications"></a>İçe aktarmayı gizleyin ve yeni mobil uygulamalar için seçenekler oluşturun

Şu anda, yeni mobil uygulamalar Talent içinde oluşturulamaz. Yeni mobil deneyimler oluşturma seçeneği **Mobil uygulama** menüsünden kaldırılmıştır.

### <a name="variable-compensation-award-dmf-entity"></a>Değişken Ücret Ödülü (DMF varlığı)

Bu sürümde, bir **Değişken Ücret Ödülü** Veri Yönetimi Çerçevesi (DMF) varlığı şimdi dışa aktarmaya hazırdır.

### <a name="uk-addresses-appear-in-the-personnel-management-analytics-page-as-swiss-addresses"></a>İngiltere adresleri, personel yönetimi analiz sayfasında İsviçre adresi olarak görünmektedir.

Bu sürümde, adresler şehre göre gösterilir. Bu sürüm, görselleştirmelerin bir çalışanın konumunda hatalı gösterildiği sorunları düzeltir.

### <a name="the-workforce-power-bi-report-shows-an-error-when-a-workers-seniority-date-is-on-leap-day"></a>Workforce Power BI raporu, çalışan kıdem tarihi bir artık gün olduğunda hata gösteriyor

29 Şubat'a denk gelen bir hesabın kıdem tarihleri için Microsoft Power BI içinde bir düzeltme yapılmıştır.

### <a name="employee-fixed-compensation-employee-variable-awards-employee-variable-plans-enrollments-allow-for-custom-fields"></a>Personel sabit ücret, Personel değişken ikramiyeler, Personel değişken planlar (kayıtlar) özel alanlara izin ver

Özel alanlar şimdi personel sabit ücret, personel değişken ikramiyeler ve personel değişken planlar (kayıtlar) için eklenebilir. Şimdi, personel sabit ve değişken ikramiye planları hakkında daha fazla bilgiyi, varsayılan olarak kullanılabilen bilgiye ek olarak izleyebilirsiniz. Özel alanlar, kullanıcı arabirimi veya sağlanan varlıklar üzerinden girilebilir veya güncelleştirilebilir.

### <a name="other-miscellaneous-bug-fixes"></a>Diğer çeşitli hata düzeltmeleri

Bu sürüm, diğer küçük hata düzeltmeleri içerir.

## <a name="coming-soon"></a>Çok yakında

### <a name="advanced-compensation-security-fixed-and-variable"></a>Gelişmiş ücret güvenliği (Sabit ve değişken)

Pek çok kuruluşta, ücret ve kazanç yöneticilerinin yalnızca belirli ücret kayıtlarına erişimi olabilir. Bu kayıtlar yöneticiler veya bölgesel çalışanlar için olabilir. Bu, İnsan kaynakları (HR) yönetimini değiştirir ve ücret planlarını kuruluş içindeki farklı personel popülasyonları için korur. Güvenlik rolleri, sabit ve değişken planlara atanabilir ve bu planların ve bunlarla ilişkili personel verisinin erişimini belirlemek için atanabilir (örneğin, maaş bilgisi ve bonus kayıtlar). Yalnızca belirli erişime sahip roller bu çalışanlar için ücreti işleyebilirler.

### <a name="platform-update-24"></a>Platform güncelleştirmesi 24

Microsoft Dynamics 365 for Finance and Operations platform güncelleştirmeleri 24 (Mart 2019) hakkında daha fazla bilgi için bkz. [Finance and Operations platform güncelleştirmesi 24 (Mart 2019) içindeki önizleme özellikleri](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).

### <a name="make-employee-fixed-compensation-available-for-future-position-assignments"></a>Gelecekteki konum atamaları için personel sabit ücreti kullanılabilir kılın.

Kuruluşa katılan personelin gelecekte bir işe başlama tarihine sahip olması normaldir. Bu, gelecekteki konum atamalarına sahip personel için tanımlanmış sabit ücret atamalarına izin verir.

## <a name="known-issues"></a>Bilinen sorunlar

### <a name="changes-to-the-core-hr-integration-template-talent-common-data-service-for-apps-to-finance-and-operations"></a>Core HR tümleştirme şablonunda değişiklikler (Talent Common Data Service for Apps'ten Finance and Operations'a)
Core HR için şablon, "gelişmiş sorgu şablonuna" güncelleştirilmiştir. Bu nedenle, varsayılan olarak, gelişmiş sorgu bu şablonu kullanarak oluşturulan projeler için kullanılabilir olacaktır. Ek olarak, tüm varsayılan eşleştirme işlevleri yalnızca gelişmiş sorgu düzenleyicide görünür olacaktır. (Varsayılan eşleşme işlevi, eşleştirmelerde "FN" olarak görüntülenir.)

Eşleştirme hataları hakkında daha fazla bilgi için bkz. [Dynamics 365 for Talent Core HR (14 Aralık 2018) içerisinde neler değişti](https://docs.microsoft.com/dynamics365/unified-operations/talent/whats-new-talent-december-14).

Yeni şablonu kullanmak için yeni bir proje oluşturun ve yeni Talent tümleştirme şablonunu seçin.

Varolan bir şablonu güncelleştirmek için şu adımları izleyin.

1. Aşağıdaki eşlemeleri güncelleştirin:

    - **Pozisyonlar için İş Pozisyonları:** Bu eşleştirmeyi kaldır.
    - **Ana İş Ataması Pozisyonlar için İş Pozisyonları:** Bu eşleştirmeyi kaldır.
    - **Temel Pozisyona İş Pozisyonları:** **İş Pozisyonları** Common Data Service for Apps varlığından **Taban Pozisyon** Finance and Operations varlığına yeni bir eşleşme eklemek. Serideki 7. pozisyona taşıyın.

        [![İş Pozisyonlarından Temel Pozisyona eşleme](./media/CDS-Mapping1.png)](./media/CDS-Mapping1.png)

    - **Pozisyon Ayrıntılarına İş Pozisyonları:** **İş Pozisyonları** Common Data Service for Apps varlığından **Pozisyon Ayrıntıları** Finance and Operations varlığına yeni bir eşleşme eklemek. Serideki 8. pozisyona taşıyın.

        [![İş Pozisyonlarından Pozisyon Ayrıntıları eşleme](./media/CDS-Mapping2.png)](./media/CDS-Mapping2.png)

    - **Pozisyon Süreleri İş Pozisyonları:** **İş Pozisyonları** Common Data Service for Apps varlığından **Pozisyon Süreleri** Finance and Operations varlığına yeni bir eşleşme eklemek.

        [![İş Pozisyonlarından Pozisyon Süreleri eşleme](./media/CDS-Mapping3.png)](./media/CDS-Mapping3.png)

    - **Pozisyon Hiyerarşileri İş Pozisyonları:** **İş Pozisyonları** Common Data Service for Apps varlığından **Pozisyon Hiyerarşileri** Finance and Operations varlığına yeni bir eşleşme eklemek. **Gelişmiş Sorgu**'yu seçerek gelişmiş sorguları projenizde kullanılabilir yapın.

       [![Gelişmiş Sorgu düğmesi](./media/CDS-Advanced-Query.png)](./media/CDS-Advanced-Query.png)

2. Aşağıdaki eşleşmeleri ekleyin.
    
    [![Eşleştirme](./media/CDS-Mapping4.png)](./media/CDS-Mapping4.png)

    1. cdm_jobpositionnumber cdm_jobspositionnumb... = POSITIONID cdm_parentjobpositionid.cdm-jobpositionnumb... = PARENTPOSITIONID cdm_validfrom cdm_validfrom = VALIDFROM cdm_validto cdm_validto = VALIDTO
       
    2. **Arama** alanının yanında **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.  

    3. **cdm_parentjobpositionid.cdm_jobpositionnumber** sütununu bulun ve sağ tarafındaki aşağı oku seçin.

    4. Beliren iletişim kutusunda **Boşu kaldır**'ı seçin.

    5. HIERARCHYTYPENAME için varsayılan değer dönüştürme eklemek için **Sütun ekle \> Koşullu sütun ekle** seçin.

        [![Koşullu sütun ekle komutu](./media/Add-column.png)](./media/Add-column.png)

    6. **Koşullu sütun ekle** iletişim kutusunda, **HIERARCHYTYPENAME**'i yeni sütunun adı olarak girin.
    7. Koşulun **Eğer** kısmında, herhangi bir alanı seçin, ilişki olarak **eşittir** seçin ve bir değer girin. Koşulun ***Sonra** ve **Aksi** kısımlarında, varsayılan değerin ne olacağını belirtin. Bu durumda, her iki bölüme de **Satır** girin.

        [![Koşullu sütun iletişim kutusu ekle](./media/Add-conditional-column.png)](./media/Add-conditional-column.png)

    8. **Tamam**'ı seçerek **Gelişmiş Sorgu ve Filtreleme** iletişim kutusunu kapatın.
    9. **Eşleştirme görevi** sayfasında, HIERARCHYTYPENAME için başka bir eşleme oluşturmak için yeni sütunu kaynak olarak seçin.

        [![Eşleştirme](./media/CDS-Mapping5.png)](./media/CDS-Mapping5.png)
