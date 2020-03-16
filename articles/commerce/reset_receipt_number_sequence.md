---
title: Makbuz numaralarını sıfırlama
description: Bu konuda, istenen tarihteki çeşitli eylemler için kullanılan giriş numaralarının nasıl sıfırlanacağı açıklanmaktadır (örneğin, mali yıl veya takvim yılı).
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-Commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail, Commerce
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Application update 10.0.9
ms.openlocfilehash: e81ff86a8b8a4dca6b14a21d6e982b03a928d29e
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020090"
---
# <a name="reset-receipt-numbers"></a>Makbuz numaralarını sıfırlama 

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Perakendeciler, mağaza gibi çeşitli eylemler için giriş numaraları (örneğin nakit ve hareketleri, iade hareketleri, müşteri siparişleri, teklifler ve ödemeler) oluşturur. Perakendeciler kendi makbuz biçimlerini tanımlamakla birlikte, bazı ülkelerde veya bölgelerde bu makbuz biçimlerine sınırlamalar koymak için gereken düzenlemeler vardır. Örneğin, bu düzenlemeler Makbuzdaki karakter sayısını sınırlayabilir, birbirini izleyen Makbuz numaraları gerektirebilir, bazı özel karakterleri sınırlayabilir veya yılın başlangıcında makbuz numaralarının sıfırlanmasını gerektirebilir. Microsoft Dynamics 365 Commerce, perakendecilerinin yasal gereksinimleri karşılamasına yardımcı olmak için makbuz numaralarının yönetimi sürecini çok esnek yapar. Bu konu, makbuz numaralarının sıfırlanması için işlevselliğin nasıl kullanıldığını açıklamaktadır.

Commerce'da makbuz biçimleri alfasayısal olabilir. Hem statik içeriği hem de dinamik içeriği yerleştirebilirsiniz. Statik içerik alfabetik karakter, sayı ve özel karakterleri içerir. Dinamik içerik, otomatik olarak artan mağaza numarası, Terminal numarası, tarih, ay, yıl ve numara serileri gibi bilgileri temsil eden bir veya daha fazla karakter içerir. Formatlar, işlevsellik profilinin **makbuz numaralandırma** bölümünde tanımlanmıştır. Aşağıdaki tabloda dinamik içeriği temsil eden karakterler açıklanmıştır.

| Karakterler | Tanım |
|------------|-------------|
| C          | Mağaza numarası için **S** karakteri kullanılır. Örneğin, bir mağaza HOUSTON1 numaralandırılmışsa, **SSS** biçimi alındı bilgisi olarak "ON1" gösterir. **SSSSS** biçimi makbuzda "STON1" gösterir. |
| T          | Terminal numarası için **T** karakteri kullanılır. Örneğin, bir terminal 0001 numaralandırılmışsa, **TTTT** biçimi alındı bilgisi olarak "0001" gösterir. |
| A          | Personel kimlik numarası için **C** karakteri kullanılır. Örneğin, bir personel üyesinin 000160 kodu varsa, **CCCC** formatı makbuz üzerinde "0160" görüntüler. |
| ggg        | **ggg** karakterleri , 1 ile 366 arasındaki bir yılın gününe karşılık gelir. Örneğin, 15 Ocak tarihinde, **ggg** olarak biçim, girişte "015" sözcüklerini gösterir. |
| MM         | İki basamaklı ay için **AA** karakterleri kullanılır. Örneğin, Ocak ayında, **AA** olarak biçim, girişte "01" gösterir. |
| GG         | İki basamaklı ayın günü için **GG** karakterleri kullanılır. Örneğin, 15 Ocak tarihinde, **GG** olarak biçim, girişte "15" sözcüklerini gösterir. |
| YY         | İki basamaklı yıl için **YY** karakterleri kullanılır. Örneğin, 2020 yılı boyunca herhangi bir ayda, **YY** biçimi makbuzda "20" olarak gösterilir. |
| \#         | Bir sayı işareti (**\#**) sıralı numaralandırma için kullanılır. Örneğin, **####** olarak biçim, girişte "0001," "0002," "0003" ve bu şekilde gösterir. |

Belirli bir tarihteki girişin sıralı numaralandırmasını sıfırlayabilirsiniz. Sonra, seçili sıfırlama tarihinde 12:00'dan sonra gerçekleşen ilk hareket için, sistem girişin numara sırasını 1 olarak sıfırlar. Ayrıca, sıfırlamanın yalnızca bir kez mı yoksa her yıl yinelenip tekrarlanmadığını da belirtebilirsiniz. Yıllık tekrar belirtilirse, satıcı bunu durdurmak için seçene kadar her yıl otomatik olarak sıfırlanır. 

Sıfırlamayı açmak için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> İşlevsellik profilleri** öğesine tıklayın.
1. **Makbuz numarası** hızlı sekmesinde, **numara sıfırlama tarihini Sıfırla**'yı seçin.
1. Açılan iletişim kutusunda, **sıfırlama tarihi** alanında, sıfırlamanın gerçekleşmesi için gelecekte bir tarih seçin.
1. **Makbuz türünü Sıfırla** alanında, **yalnızca bir kez** veya **yıllık**'ı seçin.
1. **Tamam**'ı seçin.

![Makbuz sıfırlama tarihi seçme](media/Enable_receipt_reset.png "Makbuz sıfırlama tarihi seçme")

Bir tarih seçtikten sonra, **sonraki giriş numarası sıfırlama tarihi** sütununda görüntülenir. Sıfırlama tarihi tüm giriş hareketi türleri için geçerlidir. Bu nedenle, makbuz numarası serisi tüm makbuz tipleri için sıfırlanacaktır.

Sıfırlama tarihi geldiğinde, makbuz numarası her türün ilk hareketi için sıfırlanır. Ayrıca, işlevsellik profilinde, sıfırlama tarihi **sonraki giriş numarası sıfırlama tarihi** sütunundan **geçerli giriş numarası sıfırlama tarihi** sütununa taşınacaktır. Bu değişiklik, bir kaydın sıfırlama tarihinde kullanılmaması durumunda bir *sonraki* kullanıldığında sıfırlanacağı anlamına gelir. Örneğin, 3 Aralık 2019, sıfırlama tarihi olarak **1 Ocak 2020** tarihini seçersiniz. 1 Ocak tarihinde, kayıtlar ilk hareketini yaptıklarında, makbuz numarası sıfırlanır. Ancak, Aralık ve Ocak süresince hiç bir kayıt kullanılmaz, ancak Şubat ayında kullanılacak şekilde başlatılır. Bu durumda, bir sıfırlama eylemi tanımlanmıştı, bu kaydın makbuz numarası, kasanın Şubatta ilk hareketini yaptığında sıfırlanacaktır.

Sonraki sıfırlama tarihlerini temizlemek için **sıfırlama tarihini temizle** işlevini kullanabilirsiniz. Ancak, sıfırlama tarihi geçmişte oluştuysa, geri alınamaz. Bu nedenle, sıfırlanma işleminin henüz gerçekleşmemiş olduğu tüm kayıtlarda sıfırlama işlemi devam eder.

> [!NOTE]
> Seçtiğiniz sıfırlama tarihine ve makbuz formatına bağlı olarak, tekrarlanan Makbuz numaraları olabilir. Satış noktası (POS) sisteminin bu gibi durumları işleyebilmesine karşın, iadelerin işlenmesi için gereken süreyi arttırır, çünkü satışlar ilişkilendirmeleri tekrarlanan girişler arasında seçim yapmak zorundadır. Tekrarlanan girişler planlanan bir sonuç değilse, veri temizlemesine ilişkin diğer zorluklar ortaya çıkabilir. Bu nedenle, sıfırlamadan sonra tekrarlanan öğe numaralarının olmasını önlemeye yardımcı olmak için dinamik Tarih karakterleri (örneğin **ggg**, **AA**, **GG**, **YY**) kullanmanızı öneririz.