---
title: Hesap yapısı etkinleştirme performans iyileştirmesi
description: Bu makalede, hesap yapısı etkinleştirme işlemi için yeni performans iyileştirmesi açıklanmaktadır.
author: RyanCCarlson2
ms.date: 10/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-10-08
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 42f8fcebba6465261489f74a9bb1dd46c2d5fa16
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2022
ms.locfileid: "9714014"
---
# <a name="account-structure-activation-performance-enhancement"></a>Hesap yapısı etkinleştirme performans iyileştirmesi

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Bu performans iyileştirmesi, aynı anda birden fazla hareket güncelleştirmesi çalıştırarak hesap yapılarını daha hızlı etkinleştirmenize olanak tanır. Ek olarak, yapının kendisi doğrulandıktan sonra etkin olarak işaretlenir ve deftere nakledilmeyen mevcut hareketler yeni yapıya güncelleştirilirken hareket işlenmeye devam edebilir. Hareket güncelleştirmeleri biraz zaman alabileceğinden **Hesap yapıları** sayfasında ızgaranın üstündeki **Etkinleştirme durumunu görüntüle** seçeneğini belirleyerek etkinleştirme durumunuzu izleyebilirsiniz. Ayrıca, Eylem Bölmesi'nde **Görüntüle**'yi seçip ardından açılır menüde **Etkinleştirme durumu** seçeneğini belirleyerek etkinleştirme durumunuzu görüntüleyebilirsiniz.

[![Hesap yapıları sayfası.](./media/AccountStructure1.png)](./media/AccountStructure1.png)

**Etkinleştirme durumunu görüntüle**'yi seçtikten sonra etkinleştirme sürecinin parçası olarak çalışan görevleri tek tek gösteren bir iletişim kutusu görüntülenir. Her görev için durumu ve görev tamamlandıktan sonra tamamlanma tarihi ile saatini görüntüleyebilirsiniz.

[![Hesap yapısı etkinleştirme zaman çizelgesi.](./media/AccountStructureTimeline.png)](./media/AccountStructureTimeline.png)

## <a name="account-structure-activation-tips"></a>Hesap yapısı etkinleştirme ipuçları

**Nakledilmeyen hareketleri güncelleştir** adlı bir sekme bölümüne sahip taslak hesap yapısı için **Etkinleştir**'i seçtiğinizde görüntülenen hesap yapısı etkinleştirme iletişim kutusu. Bu bölümde, **Güncelleştirmeye zorla** adlı bir seçenek bulunur. Deftere nakledilmeyen tüm hareketleri geçerli yapıda güncelleştirmek için bu seçeneği belirleyebilirsiniz. Ancak bu seçeneği yalnızca bir hata oluştuğunda veya Microsoft Desteği sizi yönlendirdiğinde kullanmanız gerekir.

Etkinleştirme işleminin performansını etkileyebilecek bazı faktörler şunlardır:

- Deftere nakledilmeyen çok sayıda günlük kaydı
- Serbest metin faturaları, satıcı faturaları ve kaynak belge çerçevesini kullanan ve açık muhasebe dağıtımlarına sahip ilgili belgeler gibi çok sayıda açık kaynak belge kaydı
- TaxUncommitted içindeki veri miktarı
- Açık bütçe verilerinin miktarı
- Etkinleştirme görevleri çalışmaya devam ederken günlük verilerini içe aktarma

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
