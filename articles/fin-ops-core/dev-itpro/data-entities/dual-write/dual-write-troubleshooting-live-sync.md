---
title: Canlı eşitleme sorunlarını giderme
description: Bu konu,canlı eşitlemeyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b40b71eb45ae5a95a732c9554356afcddecb750e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566825"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Canlı eşitleme sorunlarını giderme

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar. Bu konu,canlı eşitlemeyle ilgili sorunları çözmenize yardımcı olabilecek bilgileri sağlar.

> [!IMPORTANT]
> Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Bir Finance and Operations uygulamasında satır oluşturduğunuzda, canlı eşitleme 403 Yasak hatası oluşturur

Finance and Operations uygulamasında bir satır oluşturduğunuzda aşağıdaki hata iletisini alabilirsiniz:

*\[{\\"hata\\":{\\"kod\\":\\"0x80072560\\",\\"mesaj\\":\\"Kullanıcı kurumun bir üyesi değil.\\"}}\], Uzak sunucu hata gönderdi: (403) Yasak."}}".*

Bu sorunu gidermek için, [sistem gereksinimleri ve önkoşulları](requirements-and-prerequisites.md) adımlarını izleyin. Bu adımları tamamlamak için, Dataverse'de oluşturulan ikili yazma uygulaması kullanıcılarının sistem yöneticisi rolüne sahip olması gerekir. Varsayılan sahip olan takımın sistem yöneticisi rolü de olmalıdır.

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Bir Finance and Operations uygulamasında satır oluşturduğunuzda, her tablo için canlı eşitleme benzer bir hata oluşturur

**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi

Bir Finance and Operations uygulamasındaki tablo verilerini her kaydetmeye çalıştığınızda aşağıdakine benzer bir hata iletisi alabilirsiniz:

*Değişiklikler veritabanına kaydedilemiyor. İş birimi, hareketi kaydedemiyor. Veriler varlık uyglarına yazılamıyor. UnitOfMeasureEntity yazma işlemi hata iletisiyle başarısız oldu varlık uoms ile eşitlenemiyor.*

Bu sorunu gidermek için, önkoşul başvuru verilerinin her iki Finance and Operations uygulamada ve Dataverse'te bulunduğundan emin olmanız gerekir. Örneğin, Finance and Operations uygulamanızda olduğunuz müşteri belirli bir müşteri grubuna aitse, müşteri grubunun Dataverse'te bulunduğundan emin olun .

Her iki tarafta da veri varsa ve sorunun veriyle ilgili olmadığını doğrulamamışsanız, aşağıdaki adımları izleyin.

1. İlgili tabloyu durdurun.
2. Finance and Operations uygulamasında oturum açın ve başarısız olan tabloya ait satırların DualWriteProjectConfiguration ve DualWriteProjectFieldConfiguration tablolarında mevcut olduğundan emin olun. Örneğin, **Müşteriler** tablosu başarısız olduğunda sorgu şöyle görünür.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. Tablo eşlemesini durdurduktan sonra bile başarısız olan tabloyla ilgili satırlar varsa başarısız olan tabloyla ilişkili satırları silin. DualWriteProjectConfiguration tablosundaki **projectname** sütununu not edin ve satırı silmek için proje adını kullanarak DualWriteProjectFieldConfiguration tablosundaki satırı getirin.
4. Tablo eşlemesini başlatın. Verilerin herhangi bir sorun olmadan eşitlenip eşitlenmediğini doğrulayın.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Bir Finance and Operations uygulamada veri oluşturduğunuzda okuma veya yazma ayrıcalık hatalarını işleme

Bir Finance and Operations uygulamada veri oluşturduğunuzda, aşağıdaki örneğe benzer bir "Hatalı istek" hata iletisi alabilirsiniz.

![Hatalı istek hata iletisi örneği](media/error_record_id_source.png)

Sorunu gidermek için, eksik ayrıcalığını etkinleştirmek amacıyla eşlenen Dynamics 365 Sales veya Dynamics 365 Customer Service departmanı ekibine doğru güvenlik rolünü atamanız gerekir.

1. Finance and Operations uygulamada, veri tümleştirme bağlantısı kümesinde eşlenen iş birimini bulun.

    ![Organizasyon eşleme](media/mapped_business_unit.png)

2. Dynamics 365 model kullanan uygulamadaki ortama oturum açın, **Ayar \> Güvenlik** gidin ve eşlenen departmanın ekibini bulun.

    ![Eşlenen departmanın ekibi](media/setting_security_page.png)

3. Düzenleme için takıma ait sayfayı açın ve sonra **takım rollerini Yönet** iletişim kutusunu açmak için **rolleri Yönet**'i seçin.

    ![Rolleri Yönet düğmesi](media/manage_team_roles.png)

4. İlgili tablolar için okuma/yazma ayrıcalığına sahip rolü atayın ve **Tamam**'ı seçin.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>En son değiştirilen Dataverse ortamı olan ortamlarda eşitleme sorunlarını giderme

**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi

Finance and Operations uygulamasında bir veri oluşturduğunuzda aşağıdaki hata iletisini alabilirsiniz:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**CustCustomerV3Entity varlığı için yük oluşturulamıyor**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Geçersiz URI hatasıyla yük oluşturma başarısız oldu: URI boş."}\],"isErrorCountUpdated":true}*

Burada, Dynamics 365'deki model kullanımlı uygulamasında hatanın nasıl göründüğü açıklanmaktadır:

*ISV kodundan beklenmeyen bir hata oluştu. (ErrorType = ClientError) Eklentiden beklenmeyen özel durum (Yürüt):  Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: varlık hesabı işlenemedi - (Bağlanılan taraf bir süre içinde doğru şekilde yanıt vermediğinden bir bağlantı girişimi başarısız oldu veya bağlanılan ana bilgisayar yanıt vermediğinden bağlantı kurulamadı*

Bu hata, Finance and Operations uygulamada veri oluşturmaya çalıştığınız sırada Dataverse ortam yanlış sıfırlandığında oluşur.

Sorunu düzeltmek için şu adımları izleyin.

1. Finance and Operations sanal makinesinde (VM) oturum açın, SQL Server Management Studio'yu (SSMS) açın ve DUALWRITEPROJECTCONFIGURATIONENTITY tablosunda, **internalentityname** öğesinin **Customers V3**'e, **externalentityname** öğesinin **accounts** öğesine eşit olduğu satırları arayın. Sorgu şöyle görünür.

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. Aşağıdaki sorguyu çalıştırmak için önceki sorgunun sonuçlarından proje adını kullanın.

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. **Externalenvironmenturl** sütununda doğru Dataverse veya uygulama URL 'sinin bulunduğundan emin olun. Yanlış Dataverse URL'sini işaret eden tüm yinelenen satırları silin. DUALWRITEPROJECTFIELDCONFIGURATION ve DUALWRITEPROJECTCONFIGURATION tablolarındaki ilgili satırları silin.
4. Tablo eşlemesini durdurun ve yeniden başlatın


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]