---
title: Canlı eşitleme sorunlarını giderme
description: Bu konu,canlı eşitlemeyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 82bdcc71196c22689cc65601f98187aaa9e5e9d6
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997314"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Canlı eşitleme sorunlarını giderme

[!include [banner](../../includes/banner.md)]



Bu konu, Finance and Operations uygulamaları ve Common Data Service arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar. Bu konu,canlı eşitlemeyle ilgili sorunları çözmenize yardımcı olabilecek bilgileri sağlar.

> [!IMPORTANT]
> Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>Bir Finance and Operations uygulamasında kayıt oluşturduğunuzda, canlı eşitleme 403 Yasak bir hata oluşturur

Finance and Operations uygulamasında bir kayıt oluşturduğunuzda aşağıdaki hata iletisini alabilirsiniz:

*\[{\\"hata\\":{\\"kod\\":\\"0x80072560\\",\\"mesaj\\":\\"Kullanıcı kurumun bir üyesi değil.\\"}}\], Uzak sunucu hata gönderdi: (403) Yasak."}}".*

Bu sorunu gidermek için, [sistem gereksinimleri ve önkoşulları](requirements-and-prerequisites.md) adımlarını izleyin. Bu adımları tamamlamak için, Common Data Service'de oluşturulan ikili yazma uygulaması kullanıcılarının sistem yöneticisi rolüne sahip olması gerekir. Varsayılan sahip olan takımın sistem yöneticisi rolü de olmalıdır.

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>Bir Finance and Operations uygulamasında kayıt oluşturduğunuzda, her varlık için canlı eşitleme benzer bir hata gönderir

**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi

Bir Finance and Operations uygulamadaki varlık verilerini her kaydetmeye çalıştığınızda aşağıdakine benzer bir hata iletisi alabilirsiniz:

*Değişiklikler veritabanına kaydedilemiyor. İş birimi, hareketi kaydedemiyor. Veriler varlık uyglarına yazılamıyor. UnitOfMeasureEntity yazma işlemi hata iletisiyle başarısız oldu varlık uoms ile eşitlenemiyor.*

Bu sorunu gidermek için, önkoşul başvuru verilerinin her iki Finance and Operations uygulamada ve Common Data Service'te bulunduğundan emin olmanız gerekir. Örneğin, Finance and Operations uygulamanızda olduğunuz müşteri belirli bir müşteri grubuna aitse, müşteri grubunun Common Data Service'te bulunduğundan emin olun .

Her iki tarafta da veri varsa ve sorunun veriyle ilgili olmadığını doğrulamamışsanız, aşağıdaki adımları izleyin.

1. İlgili varlığı durdurun.
2. Finance and Operations uygulamada oturum açın ve başarısız olan varlığın kayıtlarının DualWriteProjectConfiguration ve DualWriteProjectFieldConfiguration tablolarında var olduğundan emin olun. Örneğin, **müşteriler** varlığı başarısız olduğunda sorgu şöyle görünür.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. Varlık eşlemesini durdurduktan sonra bile başarısız olan varlık için kayıt varsa, başarısız olan varlıkla ilişkili kayıtları silin. DualWriteProjectConfiguration tablosundaki **ProjeAdı** sütununu not edin ve kaydı silmek için proje adını kullanarak kaydı DualWriteProjectFieldConfiguration tablosunda getirin.
4. Varlık eşlemesini Başlat. Verilerin herhangi bir sorun olmadan eşitlenip eşitlenmediğini doğrulayın.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Bir Finance and Operations uygulamada veri oluşturduğunuzda okuma veya yazma ayrıcalık hatalarını işleme

Bir Finance and Operations uygulamada veri oluşturduğunuzda, aşağıdaki örneğe benzer bir "Hatalı istek" hata iletisi alabilirsiniz.

![Hatalı istek hata iletisi örneği](media/error_record_id_source.png)

Sorunu gidermek için, eksik ayrıcalığını etkinleştirmek amacıyla eşlenen Dynamics 365 Sales veya Dynamics 365 Customer Service departmanı ekibine doğru güvenlik rolünü atamanız gerekir.

1. Finance and Operations uygulamada, veri tümleştirme bağlantısı kümesinde eşlenen iş birimini bulun.

    ![Organizasyon eşleme](media/mapped_business_unit.png)

2. Dynamics 365 model kullanan uygulamadaki ortama oturum açın, **Ayar \> Güvenlik** gidin ve eşlenen departmanın ekibini bulun.

    ![Eşlenen departmanın ekibi](media/setting_security_page.png)

3. Düzenleme için takıma ait sayfayı açın ve sonra **takım rollerini Yönet** iletişim kutusunu açmak için **rolleri Yönet** 'i seçin.

    ![Rolleri Yönet düğmesi](media/manage_team_roles.png)

4. İlgili varlıklar için okuma/yazma ayrıcalığına sahip rolü atayın ve **Tamam** 'ı seçin.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a>En son değiştirilen Common Data Service ortamı olan ortamlarda eşitleme sorunlarını giderme

**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi

Finance and Operations uygulamasında bir veri oluşturduğunuzda aşağıdaki hata iletisini alabilirsiniz:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":" **CustCustomerV3Entity varlığı için yük oluşturulamıyor** ","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Geçersiz URI hatasıyla yük oluşturma başarısız oldu: URI boş."}\],"isErrorCountUpdated":true}*

Burada, Dynamics 365'deki model kullanımlı uygulamasında hatanın nasıl göründüğü açıklanmaktadır:

*ISV kodundan beklenmeyen bir hata oluştu. (ErrorType = ClientError) Eklentiden beklenmeyen özel durum (Yürüt):  Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: varlık hesabı işlenemedi - (Bağlanılan taraf bir süre içinde doğru şekilde yanıt vermediğinden bir bağlantı girişimi başarısız oldu veya bağlanılan ana bilgisayar yanıt vermediğinden bağlantı kurulamadı*

Bu hata, Finance and Operations uygulamada veri oluşturmaya çalıştığınız sırada Common Data Service ortam yanlış sıfırlandığında oluşur.

Sorunu düzeltmek için şu adımları izleyin.

1. Finance and Operations sanal makinede (VM) oturum açın, SQL Server Management Studio'yu açın ( SSMS) ve DUALWRITEPROJECTCONFIGURATIONENTITY tablosundaki **internalentityname** , **Müşteriler V3** ve **externalentityname** **hesaplara** eşit olup olmadığına bakın. Sorgu şöyle görünür.

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

3. **Externalenvironmenturl** sütununda doğru Common Data Service veya uygulama URL 'sinin bulunduğundan emin olun. Yanlış Common Data Service URL 'yi işaret eden tüm yinelenen kayıtları silin. Karşılık gelen DUALWRITEPROJECTFIELDCONFIGURATION ve DUALWRITEPROJECTCONFIGURATION tablolarını silin.
4. Varlık eşlemesini durdurun ve yeniden başlatın
