---
title: Genel muhasebe hesabı kapatma sorgusu
description: Bu makalede, Genel muhasebe kapatma sorgusu penceresi açıklanmaktadır
author: kweekley
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33ae49d9503c0a83bda7e0093ab6ef69fb4aef0a
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853148"
---
# <a name="ledger-settlement-inquiry"></a>Genel muhasebe hesabı kapatma sorgusu

[!include [banner](../includes/banner.md)]

Bu makalede, bir mali dönemdeki kapatılan, kapatılmayan veya hem kapatılan hem kapatılmayan genel muhasebe hareketlerinin görüntülemek için kullanılabilecek **Genel muhasebe kapatma sorgusu** penceresi açıklanmaktadır.

## <a name="view-ledger-settlement-transactions"></a>Genel muhasebe kapatma hareketlerini görüntüleme
1.  **Genel muhasebe > Sorgular ve raporlar > Genel muhasebe kapatma sorgusu**'na gidin.
2.  Bir tarih aralığı belirtmek için **Başlangıç tarihi** ve **Bitiş tarihi** alanlarını veya **Tarih aralığı** alanını kullanın. Mizan için, tarih aralığının tek bir mali yıl içinde olması gerekir.
3.  **Ana hesaplar** alanında, genel muhasebe hareketlerini görüntülemek üzere bir veya daha fazla ana hesap seçin. Açılan liste, yalnızca **Genel muhasebe parametreleri** sayfasında genel muhasebe kapanışı için ayarlanmış ana hesapları gösterir.
4.  **Mali boyutları kılavuzda göstermek için mali boyut kümesi** alanını kullanın. Ana hesap gerekli olduğu için, **Ana hesap** alan değeri her zaman ilk sütun olarak gösterilir, bu birincil hesabı içermeyen bir mali boyut kümesi seçseniz bile.
5.  **Durum** alanında, şunu seçin:
-   Kapatılan ve kapatılmayan hareketleri görüntülemek için **Tümü**
-   Yalnızca kapatılmayan hareketleri görüntülemek için **Kapatılmayan** 
-   Yalnızca kapatılan hareketleri görüntülemek için **Kapatılan**
6.  **Hareketleri göster**'i seçin. Genel muhasebe hareketleri kılavuzda, girdiğiniz ölçütlere göre görünür. Daha fazla analiz için sorgu sonuçlarını Microsoft Excel'e aktarabilirsiniz. Kılavuzda seçin ve tutun (veya sağ tıklayın).

### <a name="column-details"></a>Sütun ayrıntıları
**Genel muhasebe kapatma sorgusu** sayfasındaki ızgara aşağıdaki sütunları içerir:
-   **Ana hesap** – Bu alan gereklidir ve her zaman gösterilir.
-   **Mali boyutlar** – Mali boyutlar seçilen mali boyut kümesi temel alınarak gösterilir.
-   **Hareket tarihi** - Genel muhasebe hareketinin deftere nakil tarihi.
-   **Orijinal hareket tarihi** – Yıl sonu kapanışı çalıştırılmış ve genel muhasebe kararlaştırma bir ana hesabın ayrıntılarını koruyacak şekilde ayarlanmışsa, kapatılmayan hareketler açılış bakiyesi olarak ayrıntıdan alınır. Genel Muhasebe hareketinin orijinal deftere nakil tarihi **Orijinal hareket tarihi** alanında sürdürülür.
-   **Hareket yaşı** – Kapatılan tüm hareketler için bu değer 0'dır (sıfır). Kapatılmayan hareketler için, değer orijinal hareket tarihinden veya hareket tarihinden sorgunun çalıştırıldığı tarihe kadar olan günlerin sayısı olarak hesaplanır.
Örneğin, bir genel muhasebe hareketinin hareket tarihi 1 Ocak 2022 (1/1/2022) ve orijinal hareket tarihi de 30 Aralık 2021 (12/30/2021) olur. Sorgu, mali yıl 2022 için 2 Ocak 2022 (1/2/2022) üzerinde çalışıyorsa, **Hareket yaşı değeri** 4 olur. Bu değer, orijinal hareket tarihi (12/30/2021) ve 1/2/2022 arasındaki gün sayısı olarak hesaplanır.

Orijinal hareket tarihi yoksa, bunun yerine hareket tarihi kullanılır.
-   **(Diğer işlem bilgileri)** – Ek sütunlar fiş numarası, açıklama ve borç ve alacak tutarlarının tüm üç para birimi cinsinden bilgilerini gösterir (hareket, muhasebe ve raporlama).
-   **Durum** – Bu değer **Kapatılır** veya **Kapatılmaz**.
-   **Kapatma Numarası** - Kapatılan hareketlere atanan kod.

[![Genel muhasebe hesabı kapatma sorgusu sayfası](./media/Inquiry1.png)](./media/Inquiry1.png)

 
Toplamlar, ızgara altında gösterilebilir.
1.  Kılavuzun sağında üç noktayı (...) seçin ve **Altbilgiyi göster**'i seçin.
2.  Her bir tutar sütununu seçin ve basılı tutun (veya sağ tıklayın) ve sonra toplamları göstermek için **Bu sütuna göre grupla**'yı seçin. Toplamlar alt bilgide gösterilir. Yalnızca kapatılmayan hareketleri gösteren sorgu için filtre uygulanmışsa, tutarları mizan olarak mutabık kılmak için toplamları kullanabilirsiniz.







