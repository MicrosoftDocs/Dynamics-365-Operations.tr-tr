---
title: Yıl sonu kapanışında eksik açılış bakiyeleri
description: Bu konuda, bir yılı kapatırken açılış bakiyelerin neden eksik olabileceği ve eksik olduklarında bu bakiyelerin nasıl yeniden oluşturulacağı açıklanmaktadır.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 582363ba6c5f6e63e695d41e73ee2f0b382cf26e
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727186"
---
# <a name="year-end-close-missing-opening-balances"></a>Yıl sonu kapanışında eksik açılış bakiyeleri

[!include [banner](../includes/banner.md)]

Bu konuda, bir yılı kapatırken açılış bakiyelerin neden eksik olabileceği ve eksik olduklarında bu bakiyelerin nasıl yeniden oluşturulacağı açıklanmaktadır.

### <a name="symptom"></a>Belirti

Genel muhasebe yıl sonu kapanışını çalıştırdıktan sonra neden hiç başlangıç bakiyesi yok? 

### <a name="resolution"></a>Çözüm

Genel muhasebede bir yılı kapattıysanız ve ardından sonraki mali yıl için açılış bakiyelerini görüntülemeyen bir mizan oluşturduysanız denetleyeceğiniz şeyler şunlardır:

**Önceki kapanış geri al** alanı **Evet** olarak ayarlanırsa aynı mali yıl için önceki yıl sonu kapanışı tersine çevrilir. Yıl sonu kapanışını tersine çevirme işlemi çalıştırılırken yıl hiç kapatılmamış gibi kapanış ve açılış bakiyeleri için tüm girişler silinir. Ayrıca fişler de silinir. Yıl sonu kapanışı işlemi otomatik olarak yeniden çalıştırılmaz. İşlemi yeniden başlatmanız gerekir, bu kez **Önceki kapanışı geri al** seçeneğini **Hayır** olarak güncelleştirin.

Bu senaryo, yıl sonu kapanışıyla ilgili SSS konusunda kapsanmaktadır. Daha fazla bilgi için bkz. [Yıl sonu faaliyetleriyle ilgili SSS](faq-year-end-activities.md).

### <a name="symptom"></a>Belirti

Yıl sonu kapanışını **Önceki kapanışı geri al** seçeneğini **Hayır** olarak ayarlayarak çalıştırdım ve yine de mali yılım için açılış bakiyelerim yok.

### <a name="resolution"></a>Çözüm

Öncelikle toplu işin durumunu denetleyin. Bir yılı kapatmak bir dizi ayrı görev içerir ancak en önemli adım, görev açıklaması **Adım 5.0.0** olan toplu görevdir. Genel muhasebe için açılış işlemlerini ve isteğe bağlı olarak kapanış işlemlerini deftere nakletme bu adım sırasında gerçekleşir. 

[![Toplu iş geçmişi listesi.](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)

Bu adım başarıyla sonlandıysa ancak **Mizan sorgusu** sayfasında (**Genel muhasebe > Sorgular ve raporlar > Mizan**) açılış bakiyelerini göremiyorsanız Bakiyeleri yeniden oluşturma adımının başarıyla tamamlanıp tamamlanmadığını görmek için yıl sonu kapanışı toplu işinin sonuçlarını inceleyin.

[![Yıl sonu kapanışı toplu işinin sonuçları.](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)

Bu adım bir nedenle başarısız olursa açılış (ve isteğe bağlı olarak kapanış) işlemleri büyük olasılıkla başarılı şekilde deftere nakledilmiştir. Fiş numarasını belirterek **Fiş hareketleri sorgusu** sayfasını ve kapattığınız yıl için yıl sonu kapanışı iletişim kutusunda sağlanan tarihi kullanarak (**Genel Muhasebe > Sorgular ve raporlar > Fiş hareketleri**) Genel muhasebe işlemlerinin başarıyla deftere nakledildiğini doğrulayabilirsiniz.

[![Fiş hareketleri sorgusu.](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)

Açılış (ve isteğe bağlı olarak kapanış) fişleri varsa yıl sonu kapanışını yeniden çalıştırmanız gerekmez. Bunun yerine, nasıl ilerleyeceğiniz hakkında bilgi için sonraki bölüme bakın.

### <a name="symptom"></a>Belirti

Yıl sonu kapanışında "Bakiyeleri yeniden oluşturma" adımı başarısız olduysa tüm yıl sonu kapanışı işlemini yeniden çalıştırmam gerekir mi?

### <a name="resolution"></a>Çözüm

Bakiyeleri yeniden oluşturma adımında, Mizan sorgusu oluşturulduğunda kullanılan Genel muhasebe bakiyeleri güncelleştirilir.  Bu, yıl sonu kapanışı işlemindeki son adımdır.  Bu başarısız olan tek adım ise Genel muhasebe işlemleri başarıyla deftere nakledilmiştir.  Yıl sonu kapanışını yeniden çalıştırmanız gerekmez. **Mali boyut kümeleri** sayfasını (**Genel muhasebe > Hesap planı > Boyutlar > Mali boyut kümeleri**) kullanarak bakiyeleri el ile yeniden oluşturma işlemini çalıştırabilirsiniz.

[![Mali boyut kümeleri sayfasında bakiyeleri yeniden oluşturma düğmesi.](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)

Bu adımın işlenmesi uzun sürerse [Mali boyut kümelerini güncelleştirmek için en iyi uygulamalar](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets) bölümünde açıklandığı gibi mali boyut kümeleri için en iyi uygulamaları incelemeyi öneririz. 

