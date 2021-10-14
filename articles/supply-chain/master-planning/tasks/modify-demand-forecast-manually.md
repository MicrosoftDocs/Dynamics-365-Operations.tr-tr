---
title: 'Kılavuz: Talep tahminini el ile değiştirme'
description: Bu konuda, bir madde için tahminin nasıl değiştirileceği açıklanmaktadır
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f48e1689d21fd0085ec38aab8f5171997fbf432
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567211"
---
# <a name="guide-modify-a-demand-forecast-manually"></a>Kılavuz: Talep tahminini el ile değiştirme

[!include [banner](../../includes/banner.md)]

Bu yordamda, bir madde için tahminin nasıl değiştirileceği gösterilmiştir. Bu yordam için üretim planlayıcısına yöneliktir.

## <a name="modify-the-forecast-for-a-selected-item"></a>Seçili bir madde için tahmin değiştirme

Seçili bir madde için tahmini değiştirmek üzere:

1. **Modüller \> Ürün bilgileri yönetimi \> Ürünler \> Serbest bırakılan ürünler**'e gidin.
1. Listede, istenen kaydı bulun ve seçin. Tahminini değiştirmek istediğiniz maddeyi seçin.
1. Eylem Bölmesi'nde **Plan** sekmesini açın ve **Talep tahmini**'ni seçin.
1. Listede bir satır seçin. Tahmin satırı yoksa, Eylem Bölmesinde **Yeni**'ye tıklayarak yeni bir satır oluşturun.  
1. **Satış miktarı** alanına pozitif bir sayı girin. Bu sayı, madde için tahmin edilmiş miktarı temsil eder. Negatif bir sayı girerseniz hata gösterilir.
1. Diğer alanları gereken şekilde doldurun.
1. Eylem Bölmesinde **Kaydet**'i seçin.

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a>Microsoft Excel ile bir veya daha fazla madde için tahmini değiştirme

Microsoft Excel ile bir veya daha fazla madde için tahmini değiştirmek için:

1. Aşağıdakilerden birini yapın:
    - Önceki bölümde açıklandığı gibi herhangi bir madde için (hangisi olduğu önemli değildir) **Talep tahmini** sayfasını açın.
    - **Master planlama \> Tahmin \> El ile tahmin girişi \> Talep tahmini satırları**'na gidin.
1. Eylem Bölmesinde **Microsoft Office'te Aç \>Talep tahmini girişleri**'ni seçin.
1. Bir indirme konumu seçin, kaydedin ve indirilen dosyayı Excel'de açın.
1. Bir uyarı görürseniz **Düzenlemeyi etkinleştir**'i seçin.
1. Excel'de, Microsoft Dynamics görev bölmesini kullanarak Supply Chain Management'ta oturum açın. **Oturumumu açık tut** seçeneğini etkinleştirerek oturum açmanız ve veri bağlantısı uygulamasına güvenmeniz gerekir.
1. Excel elektronik tablosu artık şirketiniz için geçerli tüm talep tahmini satırlarını gösterir.  Talep tahmin satırlarını gereken şekilde ekleyin, silin ve düzenleyin.
1. Değişikliklerinizi Supply Chain Management'a geri yüklemek için Microsoft Dynamics görev bölmesinde **Yayımla**'yı seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
