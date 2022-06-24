---
title: Kalite yönetimi test gereçleri
description: Bu makale, Microsoft Dynamics 365 Supply Chain Management'ta kalite emirleriyle testlerin kullanılabilmesi için, test araçlarının nasıl oluşturulacağını açıklar.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36b712e6a99a0625af28ef121d0c9c39c1e32603
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857677"
---
# <a name="quality-management-test-instruments"></a>Kalite yönetimi test gereçleri

[!include [banner](../includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Supply Chain Management'ta kalite emirleriyle testlerin kullanılabilmesi için, test araçlarının nasıl oluşturulacağını açıklar.

**Test araçları** sayfasını, kalite emirleriyle ilgili testleri gerçekleştirmek için kullanılan cihazlar hakkında ayrıntılı bilgi tanımlamak ve görüntülemek için kullanabilirsiniz. Test araçları isteğe bağlıdır. Ancak, bu araçlar çalışanların belirli bir testi gerçekleştirmek için hangi cihaz veya aracı kullanmaları gerektiğini bilmelerini sağlamaya yardımcı olabilirler.

## <a name="test-instrument-example"></a>Test aracı örneği

Elektrik bileşenleri üzerinde çeşitli testler gerçekleştiriyorsunuz. Bazı testler, bileşenlerin voltaj çıkışı, bir test sıcaklıkları ve bir test de ağırlıkları içindir. Her bir testi gerçekleştirmek için farklı araçlar, cihazlar veya ekipman kullanılır. Örneğin, voltaj ölçmek için bir voltaj ölçer kullanılır, sıcaklığı ölçmek için bir termometre kullanılır ve ağırlığı ölçmek için bir tartı kullanılır. Bu cihazların her birini bir test aracı olarak yapılandırabilir ve test sonuçlarının kaydedilmesi için gereken ölçü birimini belirtebilirsiniz. Örneğin, voltaj ölçerden gelen sonuçlar volt olarak kaydedilir, termometreden gelen sonuçlar Fahrenhayt veya Santigrat derece olarak kaydedilir ve tartının sonuçları libre veya kilogram olarak kaydedilir.

## <a name="create-a-test-instrument"></a>Yeni bir test aracı oluşturma

1. **Stok yönetimi \> Kurulum \> Kalite kontrol \> Test araçları** öğesine gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Test aracı** – Test aracı için benzersiz bir kod ya da ad girin.
    - **Açıklama** – Test aracının detaylı bir açıklamasını girin.
    - **Birim** – Aracın sonuçları ölçeceği birimi seçin. **Duyarlık** alanı, seçtiğiniz birime göre otomatik olarak ayarlanır.

1. Sayfayı kapatın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite yönetimi testi](quality-tests.md)
- [Kalite yönetimi test grupları](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
