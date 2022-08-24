---
title: Finans ve operasyon uygulamalarının yükseltmeleriyle ilgili sorunları giderme
description: Bu makalede, finans ve operasyon uygulamalarındaki yükseltmelerle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlanmaktadır.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 7ab75c3a7b6c53982a32658f376a9fd148c023e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289559"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Finans ve operasyon uygulamalarının yükseltmeleriyle ilgili sorunları giderme

[!include [banner](../../includes/banner.md)]





Bu makalede, finans ve operasyon uygulamaları ile Dataverse arasında çift yazma tümleştirmesi hakkında sorun giderme bilgileri sağlanmaktadır. Bu konu, finans ve operasyon uygulamalarındaki yükseltmelerle ilgili sorunları çözmenize yardımcı olabilecek bilgileri sağlar.

> [!IMPORTANT]
> Bu makalede ele alınan bazı sorunlar için sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="database-synchronization-errors"></a>Veritabanı eşitleme hataları

**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi

Bir finans ve operasyon uygulamasını Platform güncelleştirmesi 30'a yükseltmek için **DualWriteProjectConfiguration** tablosunu kullanmaya çalışırken aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Sorunu düzeltmek için şu adımları izleyin.

1. Finans ve operasyon uygulamasının sanal makinesinde (VM) oturum açın.
2. Yönetici olarak Visual Studio açın ve uygulama nesne ağacı (AOT) açın.
3. **DualWriteProjectConfiguration** öğesini arayın.
4. AOT'de, **DualWriteProjectConfiguration** öğesini sağ tıklatın ve **yeni projeye Ekle** 'yi seçin. Varsayılan seçenekleri kullanan yeni projeyi oluşturmak için **Tamam**'ı seçin.
5. Çözüm Gezgininde **proje özelliklerini** farenin sağ düğmesiyle tıklayın ve yapılardaki **veritabanını senkronize eti** **doğru** olarak ayarlayın.
6. Projeyi oluşturun ve yapının başarılı olduğunu onaylayın.
7. **Dynamics 365** menüsünde **veritabanını eşitle**'yi seçin.
8. Tam veritabanı eşitlemesi yapmak için **Eşitle**'yi seçin.
9. Tam veritabanı eşitleme işlemi başarılı olduktan sonra, Microsoft Dynamics Lifecycle Services (LCS) içindeki veritabanı eşitleme adımını yeniden çalıştırın ve uygun şekilde yükseltme betiklerini el ile kullanın; böylece güncelleştirmeye devam edebilirsiniz.

## <a name="missing-table-columns-issue-on-maps"></a>Eşlemelerde eksik tablo sütunları sorunu

**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi

**Çift-yazılır** sayfada aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz:

*Şemada eksik kaynak alanı \<field name\>.*

![Eksik kaynak sütun hata iletisi örneği.](media/error_missing_field.png)

Bu sorunu gidermek için, öncelikle bu sütunların tabloda olduğundan emin olmak için aşağıdaki adımları izleyin.

1. Finans ve operasyon uygulamasının sanal makinesinde oturum açın.
2. **Çalışma alanları \> Veri yönetimi**'ne gidin, **Çerçeve parametreleri** kutucuğunu seçin ve sonra **Tablo ayarları** sekmesinde, tabloları yenilemek için **Tablo listesini yenile**'yi seçin.
3. **Çalışma alanları \> Veri yönetimi**'ne gidin, **Veri tabloları** sekmesini seçin ve tablonun listelendiğinden emin olun. Tablo listede değilse finans ve operasyon uygulaması için sanal makinede oturum açın ve tablonun kullanılabilir olduğundan emin olun.
4. Finans ve operasyon uygulamasındaki **Çift yazma** sayfasından **Tablo eşleme** sayfasını açın.
5. Tablo eşlemelerindeki sütunları otomatik olarak doldurmak için **Tablo listesini yenile**'yi seçin.

Sorun yine de düzeltilmemişse, aşağıdaki adımları izleyin.

> [!IMPORTANT]
> Bu adımlar, bir tabloyu silme ve sonra yeniden ekleme sürecinde size yol gösterir. Sorunlardan kaçınmak için, adımları tam olarak takip edin.

1. Finans ve operasyon uygulamasında, **Çalışma alanları \> Veri yönetimi**'ne gidin ve **Veri tabloları** kutucuğunu seçin.
2. Özniteliğin eksik olduğu tabloyu bulun. Araç çubuğunda **Hedef eşlemeyi değiştir**'e tıklayın.
3. **Hazırlamayı hedefe eşle** bölmesinde, **Eşleme oluştur**'a tıklayın.
4. Finans ve operasyon uygulamasındaki **Çift yazma** sayfasından **Tablo eşleme** sayfasını açın.
5. Öznitelik eşlemede otomatik olarak doldurulmamışsa, **Öznitelik ekle** düğmesine ve sonra **Kaydet**'e tıklayarak el ile ekleyin. 
6. Eşlemeyi seçin **Çalıştır**'a tıklayın.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
