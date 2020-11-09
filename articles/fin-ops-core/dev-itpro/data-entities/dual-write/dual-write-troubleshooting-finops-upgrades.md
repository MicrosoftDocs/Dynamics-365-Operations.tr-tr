---
title: Finance and Operations uygulamaları yükseltmeleriyle ilgili sorunları giderme
description: Bu konu, Finance and Operations uygulamalardaki yükseltmelerle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
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
ms.openlocfilehash: 07d6bd0bab796d7839daa2bad91f7e88c2e881b5
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997930"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a>Finance and Operations uygulamaları yükseltmeleriyle ilgili sorunları giderme

[!include [banner](../../includes/banner.md)]



Bu konu, Finance and Operations uygulamaları ve Common Data Service arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar. Bu konu, Finance and Operations uygulamalardaki yükseltmelerle ilgili sorunları çözmenize yardımcı olabilecek bilgileri sağlar.

> [!IMPORTANT]
> Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="database-synchronization-errors"></a>Veritabanı eşitleme hataları

**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi

Platform Güncelleştirmesi 30'a bir Finance and Operations uygulamayı güncelleştirmek için **dualwriteprojectconfiguration** varlığını kullanmaya çalıştığınızda aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz.

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Sorunu düzeltmek için şu adımları izleyin.

1. Finance and Operations uygulamanın sanal makinesine (VM) oturum açın.
2. Yönetici olarak Visual Studio açın ve uygulama nesne ağacı (AOT) açın.
3. **DualWriteProjectConfiguration** öğesini arayın.
4. AOT'de, **DualWriteProjectConfiguration** öğesini sağ tıklatın ve **yeni projeye Ekle** 'yi seçin. Varsayılan seçenekleri kullanan yeni projeyi oluşturmak için **Tamam** 'ı seçin.
5. Çözüm Gezgininde **proje özelliklerini** farenin sağ düğmesiyle tıklayın ve yapılardaki **veritabanını senkronize eti** **doğru** olarak ayarlayın.
6. Projeyi oluşturun ve yapının başarılı olduğunu onaylayın.
7. **Dynamics 365** menüsünde **veritabanını eşitle** 'yi seçin.
8. Tam veritabanı eşitlemesi yapmak için **Eşitle** 'yi seçin.
9. Tam veritabanı eşitleme işlemi başarılı olduktan sonra, Microsoft Dynamics Lifecycle Services (LCS) içindeki veritabanı eşitleme adımını yeniden çalıştırın ve uygun şekilde yükseltme betiklerini el ile kullanın; böylece güncelleştirmeye devam edebilirsiniz.

## <a name="missing-entity-fields-issue-on-maps"></a>Haritalarda eksik varlık alanları çıkışı

**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi

**Çift-yazılır** sayfada aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz:

*Şemada eksik kaynak alanı \<field name\>.*

![Eksik kaynak alan hata iletisi örneği](media/error_missing_field.png)

Bu sorunu gidermek için, öncelikle bu alanların varlıkta olduğundan emin olmak için aşağıdaki adımları izleyin.

1. Finance and Operations uygulamanın VM 'sine oturum açın.
2. **Çalışma alanları \>veri yönetimi** 'ne gidin, **çerçeve parametreleri** kutucuğunu seçin ve sonra **varlık ayarları** sekmesinde, varlıkları yenilemek için **varlık listesini yenile** seçin.
3. **Çalışma alanları \> Veri yönetimi** 'ne gidin, **veri varlıkları** sekmesini seçin ve varlığın listelendiğinden emin olun. Varlık listelenmiyorsa, Finance and Operations uygulama için VM 'de oturum açın ve varlığın kullanılabilir olduğundan emin olun.
4. Finance and Operations uygulamadaki **ikili yazma** sayfasından **varlık eşleme** sayfasını açın.
5. Varlık eşlemelerinde alanları otomatik olarak doldurmak için **Varlık listesini yenile** seçin.

Sorun yine de düzeltilmemişse, aşağıdaki adımları izleyin.

> [!IMPORTANT]
> Bu adımlar, bir varlığı silme ve sonra yeniden ekleme sürecinde size yol gösterir. Sorunlardan kaçınmak için, adımları tam olarak takip edin.

1. Finance and Operations uygulamada, **Çalışma alanları \> Veri yönetimi** 'ne gidin ve **Veri varlıkları** döşemesini seçin.
2. Özniteliğin eksik olduğu varlığı bulun. Araç çubuğunda **Hedef eşlemeyi değiştir** 'e tıklayın.
3. **Hazırlamayı hedefe eşle** bölmesinde, **Eşleme oluştur** 'a tıklayın.
4. Finance and Operations uygulamadaki **ikili yazma** sayfasından **varlık eşleme** sayfasını açın.
5. Öznitelik eşlemede otomatik olarak doldurulmamışsa, **Öznitelik ekle** düğmesine ve sonra **Kaydet** 'e tıklayarak el ile ekleyin. 
6. Eşlemeyi seçin **Çalıştır** 'a tıklayın.
