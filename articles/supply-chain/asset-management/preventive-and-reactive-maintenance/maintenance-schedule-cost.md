---
title: Bakım zamanlaması maliyeti
description: Bu konuda Varlık Yönetimi'nde bakım zamanlaması maliyeti açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b30fa3c142057b43202a8f5a323c0b425865e971
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571335"
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

6. **Bakım zamanlaması maliyeti** sekmesinde > **Gruplama ölçütü...** eylem bölmesi gruplarında, maliyet hesaplamasının gereken ayrıntı düzeyini göstermek için ilgili düğmelere tıklayın. Seçilen eylem bölmesi grup düğmeleri vurgulanır. Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.

7. Yeni bir maliyet hesaplaması yapmak isterseniz **Maliyeti hesapla** düğmesine tıklayın.

Aşağıdaki çizimde bir bakım zamanlaması maliyet hesaplamasının sonuçları gösterilmektedir.

![Şekil 1](media/17-preventive-maintenance.png)

