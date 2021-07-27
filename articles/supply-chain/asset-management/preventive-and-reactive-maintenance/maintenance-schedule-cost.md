---
title: Bakım zamanlaması maliyeti
description: Bu konuda Varlık Yönetimi'nde bakım zamanlaması maliyeti açıklanmaktadır.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9cbb1d81f9108a908bdfdd2a27b92b685d3afdac
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361030"
---
# <a name="maintenance-schedule-cost"></a>Bakım zamanlaması maliyeti

[!include [banner](../../includes/banner.md)]

 

Varlık Yönetiminde, bakım zamanlaması satırlarında bütçe maliyetlerini hesaplayabilirsiniz. Bu, örneğin bir sonraki yıla ait planlı önleyici bakım işleriyle ilgili maliyetler gibi beklenen maliyetlere genel bakış almak istediğinizde yararlıdır. Hesaplamalar, "Bakım planları","Bakım sırası" ve "Bakım talepleri" türünde mevcut bakım zamanlaması satırlarını temel alır.

1. **Varlık yönetimi** > **Sorgular** > **Varlıklar** > **Bakım zamanlaması maliyeti**'ne tıklayın.

2. **Bakım zamanlaması maliyeti** iletişim kutusunda, mali boyutlarda gruplanmış maliyetleri görmek isterseniz bir **Mali boyut kümesi** seçebilirsiniz.

>[!NOTE]
>Mali boyut kümeleri, **Genel muhasebe** > **Hesap planı** > **Boyutlar** > **Mali boyut kümeleri**'nde ayarlanır.

3. İşlem yapılacak yerleşimlerle ilgili olarak bakım zamanlaması satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz. Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm bakım zamanlaması satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir. **Düzey** alanına "0" değerini girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm bakım zamanlaması satırlarını gösteren ayrıntılı bir sonuç görürsünüz.

4. Belirli varlıklar için hesaplama yapmak isterseniz **Eklenecek kayıtlar** hızlı sekmesinde **Filtre**'ye tıklayın ve ilgili varlıkları seçin. Gerekirse, maliyet hesaplaması için **Beklenen başlangıç** tarihini belirtebilir veya farklı bir **Durum** seçebilirsiniz

5. Maliyet hesaplamasını başlatmak için **Tamam**'a tıklayın.

6. **Bakım zamanlaması maliyeti** sekmesinde > **Gruplama ölçütü...** Eylem Bölmesi gruplarında, maliyet hesaplamasının gereken ayrıntı düzeyini göstermek için ilgili düğmelere tıklayın. Seçilen Eylem Bölmesi grup düğmeleri vurgulanır. Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.

7. Yeni bir maliyet hesaplaması yapmak isterseniz **Maliyeti hesapla** düğmesine tıklayın.

Aşağıdaki çizimde bir bakım zamanlaması maliyet hesaplamasının sonuçları gösterilmektedir.

![Şekil 1.](media/17-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]