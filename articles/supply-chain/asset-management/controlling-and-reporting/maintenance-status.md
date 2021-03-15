---
title: Bakım durumu
description: Bu konuda Kıymet Yönetimi'nde bakım durumu hesaplama işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b5bac42d5cdc62361ee9a562e59bafa09ca7a215
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018508"
---
# <a name="maintenance-status"></a>Bakım durumu

[!include [banner](../../includes/banner.md)]

 

Varlık Yönetiminde belirli bir döneme ait yeni, etkin ve tamamlanmış bakım isteklerinin, iş emirlerinin ve bakım kesinti süresi faaliyetlerinin genel görünümünü hesaplayabilirsiniz. Aynı dönem için tamamlanan koşul değerlendirmelerinin sayısını da görebilirsiniz. Gelen ve tamamlanan bakım istekleriyle ve iş siparişleriyle ilgili iş yükünün özetini almak için bu hesaplamayı kullanın.

## <a name="make-a-maintenance-status-calculation"></a>Bakım durumu hesaplaması yap

1. **Varlık Yönetimi** > **Sorgular** > **Bakım durumu**' nu tıklatın.

2. **Durumu hesapla** iletişim kutusunda, **Başlangıç tarihi** ve **Bitiş tarihi** alanlarına hesaplamayı yapmak istediğiniz zaman aralığını girin.

3. İşlem yapılacak yerleşimlerle ilgili olarak bakım satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz. 

  Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm bakım satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki durum, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir. 
  
  **Düzey** alanına "0" değerini girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm bakım satırlarını gösteren ayrıntılı bir sonuç görürsünüz.

4. Hesaplamayı başlatmak için **Tamam**'a tıklayın.

5. **Gruplandırma ölçütü** düğmelerine tıklayarak hesaplamanın gerekli ayrıntı düzeyini görüntüleyin. Seçilen **Gruplandırma ölçütü** düğmeleri vurgulanır. Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.

6. **Gruplandırma ölçütü** düğmelerini etkinleştirerek veya devre dışı bırakarak her değişiklik yaptığınızda hesaplamayı güncelleştirmek için **Güncelleştir** düğmesine basmayı unutmayın.

7. Yeni bir bakım durumu hesaplaması oluşturmak istiyorsanız **durum**'ı tıklatın.

>[!NOTE]
>**Bakım durumunda** gösterilen sonuçlar yalnızca gerçek başlangıç tarihi ve saatine sahip bakım isteklerini ve çalışma emirlerini içerir. Bitiş tarihi ve saati boş olabilir.

## <a name="example-1"></a>Örnek 1

Aşağıdaki ekran görüntüsünde, **Yıl** ve **Ay** düğmeleri etkinleştirilmiştir. Bu **Gruplandırma ölçütü** seçenekleri seçili olduğunda, bakım istekleriyle ve iş emirleriyle ilgili iş yükü ve iş emirleri hakkında genel bakış elde edebilirsiniz. 

![Aylık iş yükü örneği](media/13-controlling-and-reporting.png)

## <a name="example-2"></a>Örnek 2

Aşağıdaki ekran görüntüsünde, işlem yapılacak yerleşim bilgileri eklendi. Şimdi, coğrafi konumları, fabrikaları veya çalışma alanlarını temsil eden işlem yapılacak konumlar arasında iş yükü ve iş yükünü karşılaştırmak mümkündür. 

![İşlem yapılacak yerleşimlere sahip aylık iş yükü örneği](media/14-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]