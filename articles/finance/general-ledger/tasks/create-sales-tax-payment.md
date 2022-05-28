---
title: Satış vergisi ödemesi oluşturma
description: Satış vergisini kapat ve deftere naklet işi yordamı, satış vergisi hesaplarındaki satış vergisi bakiyelerini kapatır ve bu bakiyeleri belirli bir dönemin satış vergisi kapatma hesabına mahsup olarak işler.
author: twheeloc
ms.date: 01/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c388a8f98cd4581abe2ec13d8922e232321e4039
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735945"
---
# <a name="create-a-sales-tax-payment"></a>Satış vergisi ödemesi oluşturma

[!include [banner](../../includes/banner.md)]

Satış vergisini kapat ve deftere naklet işi yordamı, satış vergisi hesaplarındaki satış vergisi bakiyelerini kapatır ve bu bakiyeleri belirli bir dönemin satış vergisi kapatma hesabına mahsup olarak işler.

1. **Vergi > Bildirimler > Satış vergisi > Satış vergisini kapat ve deftere naklet**'e gidin.
2. **Kapatma dönemi** alanında, açılır menü düğmesini seçerek aramayı açın.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. **Başlangıç tarihi** alanına bir tarih girin. **Genel muhasebe parametreleri** sayfasında **Düzeltmeleri dahil et** seçeneğini belirlemezseniz kapatma işlemi farklı sürümler için yapılabilir. **Orijinal sürüm**, dönem aralığının ilk kapatma işlemidir ve bir dönem aralığı için yalnızca bir kez işlenebilir. En son düzeltmeler, orijinal sürüm oluşturulduktan sonra deftere nakledilen satış vergisi hareketlerini kapatır.
5. **Hareket tarihi** alanına bir tarih girin.
6. **Tamam**'ı seçin. **Satış vergisi ödemeleri** raporu, dönemdeki kapatılan satış vergisi hareketlerini incelemek için yazdırılır.

Finance sürüm 10.0.24'ten başlayarak, **Özellik yönetimi** çalışma alanındaki **Satış vergisi ödeme raporu oluşturmayı, satış vergisi kapatma işleminden ayır** altında **Satış vergisini kapat ve deftere naklet** periyodik prosedürü uygulandıktan hemen sonra oluşturulan **Satış vergisi ödemeleri** raporunu atlayabilirsiniz.

Özellik etkinleştirildiğinde, kapatma işlemi tamamlandıktan sonra hiçbir satış vergisi ödeme raporu yazdırılmaz. Bunun yerine şu mesajı alırsınız: "Satış vergisi kapatma ve deftere nakletme işlemi tamamlandı. 'xxxx, a/g/yyyy' fişi deftere nakledildi."

Yine de **Vergi** > **Sorgular ve raporlar** > **Satış vergisi sorguları** > **Satış vergisi ödemeleri**'ne giderek satış vergisi ödeme raporunu elle çalıştırabilirsiniz.

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
