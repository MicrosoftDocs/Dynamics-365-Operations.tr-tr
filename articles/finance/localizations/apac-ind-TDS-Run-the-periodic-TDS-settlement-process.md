---
title: Dönemsel TDS kapatma işlemini yürütme
description: Bu konu, dönemsel Kaynakta Kesilen Verginin (TDS) nasıl kapatılacağını açıklamaktadır.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: cfab08a4190bf51518bd4a9b445b229a5081e87d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023647"
---
# <a name="run-the-periodic-tds-settlement-process"></a>Dönemsel TDS kapatma işlemini yürütme

[!include [banner](../includes/banner.md)]

Bu konu, dönemsel Kaynakta Kesilen Verginin (TDS) nasıl kapatılacağını açıklamaktadır.

1. **Vergi \> Beyanlar \> Stopaj vergisi \> Stopaj vergisi ödemesi**'ne gidin.

    [![Stopaj vergisi ödemesi iletişim kutusu](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)

2. **Stopaj vergisi ödemesi** iletişim kutusunda, **Vergi türü** alanında **TDS** seçeneğini belirleyin.
3. **Vergi Hesap Numarası (TAN)** alanında, kapatma işleminin adına çalıştırılacağı Vergi Hesap Numarasını (TAN) seçin.
4. **Stopaj vergisi bileşen grubu** alanında, kapatma işleminin adına çalıştırılacağı TDS bileşen grubunu seçin.
5. **Kapatma dönemi** alanında, kapatma işleminin adına çalıştırılacağı TDS kapatma dönemini seçin.

    > [!NOTE]
    > TDS kapatma işlemi, **Stopaj vergisi kapatma dönemleri** sayfasının (**Vergi \> Dolaylı vergiler \> Stopaj vergisi \> Stopaj vergisi kapatma dönemleri**) **Dönemler** sekmesinde TDS kapatma periyodu için ayarlanmış tüm dönemler için çalıştırılır.

6. **Başlangıç tarihi** alanında, TDS kapatma işleminin çalıştırılacağı başlangıç tarihini seçin.

    Kapatma dönemi içinde belirli bir dönem için, dönem için tanımlanan başlangıç tarihi "başlangıç" tarihi olarak alınır. Örneğin, TDS kapatma döneminde iki dönem olduğunu düşünelim: 1 Nisan 2009'dan 30 Nisan 2009'a kadar ve 1 Mayıs 2009'dan 31 Mayıs 2009'a kadar. **Başlama tarihi** alanında başlangıç tarihi olarak **06/04/2009** (6 Nisan 2009) öğesini seçerseniz, kapatma işlemi 1 Nisan 2009'dan itibaren yine de çalışmaya devam eder.

    **Başlangıç tarihi** alanına daha ileri bir dönem girip de kapanış dönemi içindeki önceki dönemi kapatmazsanız kapatma önceki dönemler için gerçekleşmez. Örneğin, TDS kapatma döneminin üç dönemi olsun: 1 Nisan 2009'dan 30 Nisan 2009'a kadar, 1 Mayıs 2009'dan 31 Mayıs 2009'a kadar ve 1 Haziran 2009'dan 30 Haziran 2009'a kadar. **Başlangıç tarihi** alanında başlangıç tarihi olarak **01/05/2009**'u (1 Mayıs 2009) seçerseniz, kapatma işlemi yalnızca 1 Mayıs 2009 ile 31 Mayıs 2009 arasında çalışır. Kapatma işlemi, 1 Nisan 2009 ile 30 Nisan 2009 arası için gerçekleştirilmez.

7. **Hareket tarihi** alanında, TDS kapatma hareketini deftere nakletmek için tarihi seçin.
8. **Stopaj vergisi ödemesi sürümü** alanında, TDS kapatma sürümünü seçin:

     - **Orijinal** – TDS kapatma işlemini ilk kez çalıştırmak için bu seçeneği kullanın. Orijinal ödeme sürümü, TDS kapatma işlemini bir TAN, stopaj vergisi bileşen grubu ve stopaj vergisi kapanış dönemi birleşimi ile ilgili olarak çalıştırmak için yalnızca bir kere kullanılır.
    - **En son sürümler** – Bu seçeneği, TDS kapatma işlemi belirtilen dönem için zaten çalıştırılmışsa kullanın. Kapatma işlemi dönem için daha önce çalıştırıldıktan sonra deftere nakledilen, eski tarihli hareketleri dahil edin. Bu seçeneği, kapatma işlemini istediğiniz kadar çalıştırmak için kullanabilirsiniz.

9. TDS kapatma sürecini çalıştırmak ve tutarları genel muhasebe hesaplarına nakletmek için **Güncelleştir** onay kutusunu seçin. Bu onay kutusu temizlenirse, kapatma işlemi çalıştırılmaz ve mali girişler oluşturulmaz.
10. TDS kapatma işlemini çalıştırmak ve stopaj vergisi ödeme raporunu oluşturmak için **Tamam**'ı seçin. Kapatma işlemine dahil edilen TDS hareketlerinin durumu **Kapatma** sayfasında **Kapatılmış** olarak gösterilir (**Borç hesapları \> Ödemeler \> Satıcı ödeme günlüğü**'ne gidin, **Satırlar**'ı seçin, **İşlevler**'i seçin ve sonra **Kapatma**'yı seçin).

### <a name="important-points"></a>Önemli noktalar

- Bir stopaj vergisi bileşen grubu, kapatma işlemi sırasında seçilmemişse seçili TAN ve kapatma dönemine ait tüm stopaj vergisi bileşen grupları için kapatma gerçekleşir. **Açık hareket düzenleme** sayfasındaki her stopaj vergisi bileşen grubu için ayrı bir satır oluşturulur.
- Kapatma işlemi, bir kapatma döneminin değerlendirilen kategorisinin yapısı temel alınarak yapılır. Değerlendirilen kategorisi yapısı **Şirket** olan hareketler kapatılır ve **Açık hareket düzenleme** sayfasında tek bir satır olarak görüntülenir. Değerlendirilen yapısı **Şirket** dışında bir şey olan hareketler kapatılır ve **Açık hareket düzenleme** sayfasında tek bir satır olarak görüntülenir.
- **Açık hareket düzenleme** sayfasındaki kapatılan TDS hareket satırlarının vade tarihi, **Satıcılar** sayfasında TDS yetkili satıcısı için tanımlanan ödeme koşullarına bağlıdır. TDS yetkilisi satıcısı için ödeme koşulları tanımlanmamışsa, kapatma döneminin son günü vade tarihi olarak gösterilir.
