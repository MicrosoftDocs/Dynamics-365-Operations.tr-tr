---
title: Satış vergisi ödemesi oluşturma
description: Satış vergisini kapat ve deftere naklet işi yordamı, satış vergisi hesaplarındaki satış vergisi bakiyelerini kapatır ve bu bakiyeleri belirli bir dönemin satış vergisi kapatma hesabına mahsup olarak işler.
author: twheeloc
ms.date: 10/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54132ca4775482b4a06ff7e73125e804aff40cb4
ms.sourcegitcommit: f8b597b09157d934b62bd5fb9a4d05b8f82b5a0e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/26/2021
ms.locfileid: "7700125"
---
# <a name="create-a-sales-tax-payment"></a>Satış vergisi ödemesi oluşturma

[!include [banner](../../includes/banner.md)]

Satış vergisini kapat ve deftere naklet işi yordamı, satış vergisi hesaplarındaki satış vergisi bakiyelerini kapatır ve bu bakiyeleri belirli bir dönemin satış vergisi kapatma hesabına mahsup olarak işler.

1. **Vergi > Bildirimler > Satış vergisi > Satış vergisini kapat ve deftere naklet**'e gidin.
2. **Kapatma dönemi** alanında, açılır menü düğmesine tıklayarak aramayı açın.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. **Başlangıç tarihi** alanına bir tarih girin.
    - **Genel muhasebe parametreleri** sayfasında **Düzeltmeleri dahil et** seçeneğini belirlemezseniz kapatma işlemi farklı sürümler için yapılabilir. Orijinal sürüm, dönem aralığının ilk kapatma işlemidir ve bir dönem aralığı için yalnızca bir kez işlenebilir. En son düzeltmeler, orijinal sürüm oluşturulduktan sonra deftere nakledilen satış vergisi hareketlerini kapatır.
5. **Hareket tarihi** alanına bir tarih girin.
6. **Tamam**'a tıklayın.

## <a name="performance-consideration"></a>Performans konuları

Satış vergisi ödeme yordamının tamamlanması uzun sürebilir. Yordamın performansını etkileyen başlıca etmenler, kapatma dönemindeki faturaların sayısı ve satış vergisi kapatma fişindeki deftere nakledilmesi gereken giriş sayısıdır. Performansın artırılmasına yardımcı olmak için, işleminiz için gerekli olmayan bazı işlevleri atlayabilirsiniz.

### <a name="enable-the-sales-tax-payment-performance-improvement-feature"></a>Satış vergisi ödemesi performans iyileştirme özelliğini etkinleştirme

**Satış vergisi ödemesi performans iyileştirme** özelliği, aynı ana firma, genel muhasebe boyutu ve para birimine sahip satış vergisi ödeme fiş satırlarındaki tek bir satıra, muhasebe para tutarına ve raporlama para birimi tutarına toplayarak satış vergisi ödeme yordamının performansını artırmaya yardımcı olur.

1. **Sistem Yönetimi** \> **Çalışma alanları** \> **Özellik yönetimi** seçeneğine gidin.
2. **Tümü** sekmesinde, **Satış vergisi ödemesi performans geliştirmesini** arayın ve seçin.
3. **Etkinleştir**'i seçin.

### <a name="prevent-generation-of-offset-tax-transactions"></a>Mahsup vergi hareketlerinin üretilmesini engelleme

Varsayılan olarak, satış vergisi ödeme fişi, satış vergisi ödemesi yordamında kapatılan her bir satış vergisi hareketine karşı mahsup satış vergisi hareketlerini deftere nakleder. Bu mahsup satış vergisi hareketleri, **Satış vergisi/Genel muhasebe mutabakatı** raporuna dahil edilir. Bunlar, dönem içinde kapatılmayan satış vergisi hareketlerinin bekleyen bakiyesini gösterir.

Ancak, mahsup satış vergisi hareketleri satış vergisi ödeme yordamındaki yükü artırabilir. Bu nedenle, **TaxReportGenOffsetTaxTransPerRecordSetFlighting** adlı bir deneme isteğe bağlı olarak etkinleştirilebilir. Bu deneme; Tayland, Polonya, Macaristan, Litvanya, Malezya, Hindistan, İtalya, Rusya, Çek Cumhuriyeti, Estonya ve Letonya dışındaki ülkeler ve bölgeler için mahsup vergi hareket oluşturma performansını artırmaya yardımcı olur.

> [!NOTE]
> KDV hareket tablosunda özelleştirilmiş alanlar varsa, deneme etkinleştirilemez.

**Satış vergisi/Genel muhasebe mutabakat** raporu genellikle yalnızca dahili kontrol amacıyla kullanıldığı ve birçok vergi bölgesinde gerekli olmadığı için, satış vergisi ödeme fişindeki mahsup satış vergisi hareketleri üretmemeyi tercih edebilirsiniz.

1. **Vergi** \> **Dolaylı vergiler** \> **Satış vergisi** \> **Satış vergisi kapatma dönemleri**'ne gidin.
2. Bir kapatma dönemi seçin.
3. **Genel** hızlı sekmesinde, **Mahsup vergisi hareketlerini oluşturmayı önle** seçeneğini **Evet** olarak ayarlayın.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
