---
title: Yük satırlarındaki ağırlık alanları, yükteki ağırlık alanlarıyla eşleşmiyor
description: Yük satırlarındaki ağırlık alanları, yükteki ağırlık alanlarıyla eşleşmiyor
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f71ac7b2777cb77fccdf1a4c72a47c9b406bbd68b2d20c41ddc96028d2ffc348
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756715"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a>Yük satırlarındaki ağırlık alanları, yükteki ağırlık alanlarıyla eşleşmiyor

Hata kodları: WHSLoadWeightOnLinesDoNotMatchLoadWarning

## <a name="symptoms"></a>Belirtiler

Sistem, aşağıdaki hata iletisini gösterir:

> Yük satırlarındaki ağırlık alanları, %1 yükündeki ağırlık alanlarıyla eşleşmiyor. Ağırlık alanlarını yeniden hesaplamak için Ambar yükü ağırlığı tutarlılık denetimini çalıştırın.

## <a name="cause"></a>Nedeni

**Net ağırlık** ve **Dara ağırlık** alanları, yük satırında *0* (sıfır) olarak ayarlı. Ancak, ürün üzerindeki ağırlık ölçüleri için ağırlık alanları *0* olarak ayarlı değil. Yük satırında ağırlık alanları ayarlanmamışsa, yük satırındaki miktarla ilgili tüm düzeltmeler yüklemede yanlış ağırlık hesaplamasına neden olabilir. Bu sorun, yük satırı oluşturulduktan sonra üründeki ağırlıklar değiştirilirse oluşabilir.

## <a name="resolution"></a>Çözünürlük

Varsayılan olarak, bir yük satırı oluşturulduğunda, ürünün ağırlık alanları üzerine girilir. Ağırlık sıfırsa, *Ambar yükü ağırlığı tutarlılık denetimi* işlevini kullanarak bunu yeniden hesaplayabilirsiniz.

1. **Sistem yönetimi \> Periyodik görevler \> Veritabanı \> Tutarlılık denetimi** bölümüne gidin.
1. **Tutarlılık denetimi** iletişim kutusunda, **Modül** alanını *Ambar yönetimi* olarak ayarlayın.
1. **Denetle/Onar** alanını *Hatayı düzelt* olarak ayarlayın.
1. Onay kutusu listesinde **Ambar yük ağırlığı tutarlılık denetimi** onay kutusunu seçin ve yalnızca bu onay kutusunun satırının vurgulandığından emin olun.
1. Onay kutusu listesinin en üstünde üç nokta düğmesini (**...**) seçin ve menüden **İletişim kutusu**'nu seçin.
1. **Ambar yük ağırlığı tutarlılık denetimi** iletişim kutusunda, tutarlılık denetiminin çalışacağı ölçütü belirtmek için aşağıdaki alanları ayarlayın:

    - **Yük kodu:** Bir yük kodu belirtin. Tüm yük kodlarını denetlemek için bu alanı boş bırakın.
    - **Madde numarası:** Bir madde numarası belirtin. Tüm maddeleri denetlemek için bu alanı boş bırakın.
    - **Yükte her zaman ağırlığı yeniden hesapla:** Bu seçeneği *Evet* olarak ayarlayın.
    - **Yük satırlarında ağırlık üzerine yazmaya izin ver:** Bu seçeneği *Evet* olarak ayarlayın.

1. **Ambar yükü ağırlığı tutarlılık denetimi** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Üç nokta düğmesini seçin ve menüden **Yürüt**'ü seçin.

Ağırlık, belirttiğiniz ölçütlere göre yeniden hesaplanır. Tutarlılık denetiminin sonucunu görmek için **İleti ayrıntıları** bağlantısını seçin.
