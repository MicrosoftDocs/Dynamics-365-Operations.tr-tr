---
title: Mali raporlama ile ilgili SSS
description: Bu konuda, diğer kullanıcıların mali raporlama ile ilgili soruları listelenmektedir.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a0718db77399901acc8c88278c5b373b77b3cb16
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811322"
---
# <a name="financial-reporting-faq"></a>Mali raporlama ile ilgili SSS 

Bu konuda, diğer kullanıcıların mali raporlama ile ilgili soruları listelenmektedir. 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Ağaç güvenliğini kullanarak bir rapora erişimi nasıl kısıtlayabilirim?

Senaryo: USMF demo şirketinin tüm mali raporlama kullanıcılarının D365'te görüntülemesini istemediği bir bilanço raporu bulunuyor. Çözüm: Rapora yalnızca belirli kullanıcıların erişmesini sağlamak üzere tek bir rapora erişimi kısıtlamak için Ağaç güvenliğini kullanabilirsiniz. 

1.  Mali Raporlayıcı Rapor Tasarımcısında oturum açma

2.  Yeni Ağaç Tanımı oluşturma (Dosya | Yeni | Ağaç Tanımı) a.    **Birim Güvenliği** sütununda **Özet** satırına çift tıklayın.
  i.    Kullanıcılar ve Gruplar'a tıklayın.  
          1. Bu rapora erişmesini istediğiniz Kullanıcılar veya Grupları seçin. 
          
[![kullanıcı ekranı](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)

[![güvenlik ekranı](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)

  b.    **Kaydet**'e tıklayın.
  
[![kaydet düğmesi](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)

3.  Rapor Tanımınızda, yeni Ağaç Tanımınızı ekleyin

[![ağaç tanımı formu](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)

A.  Ağaç Tanımındayken, Ayar'a tıklayın ve "Raporlama birimi seçimi" altından, "Tüm birimleri dahil et"i işaretleyin

[![raporlama birimi seçim formu](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)

**Öncesi:** [![öncesi ekran görüntüsü](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)

**Sonrası:** [![sonrası ekran görüntüsü](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)

Not: Yukarıdaki iletinin nedeni, Birim Güvenliği uygulandıktan sonra kullanıcımın o rapora erişim izninin olmamasıdır



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a>D365'te hangi hesaplarda bakiyelerin eşleşmediğini nasıl belirleyebilirim?

D365'te beklediğiniz şekilde eşleşmeyen bir raporunuz varsa bu hesapları ve farkları tanımlamak için gerçekleştirebileceğiniz adımlar burada verilmiştir. 

### <a name="in-financial-reporter-report-designer"></a>Mali Raporlayıcı Rapor Tasarımcısında

1.  Yeni Satır Tanımı oluşturun a.    Düzenle | Boyutlardan Satır Ekle'yi tıklayın i.  MainAccount'u seçme [![Ana ekranı seçme_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)
    
    ii. Tamam'a tıklayın b.    Satır Tanımını kaydedin

2.  Yeni Sütun Tanımı oluşturma     [![Yeni Sütun Tanımı oluşturma](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)

3.  Yeni Rapor Tanımı oluşturun a.    Ayarlar'a tıklayın ve işaretleri kaldırın [![Ayarlar formu](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)
   
4.  Raporu oluşturun. 

5.  Raporu Excel'e dışarı aktarın.

### <a name="in-d365"></a>D365'te: 
1.  Genel Muhasebe | Sorgular ve Raporlar | Mizan'a tıklayın a.    Parametreler i.  Başlangıç Tarihi: Mali Yılın başlangıcı ii. Bitiş Tarihi: Raporu oluşturduğunuz tarih (şunun için: iii.    Finansal Boyut Ayarı "Ana Hesap Ayarı") [![Ana Hesap Formu](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)
      
  b.    Hesapla'ya tıklayın

2.  Raporu Excel'e dışarı aktarın

Artık FR Excel raporundan ve D365 Mizan raporuna veri kopyalayabilir ve "Kapanış Bakiyesi" sütunlarını karşılaştırabilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]