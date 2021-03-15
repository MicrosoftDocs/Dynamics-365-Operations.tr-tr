---
title: Tüketim raporları oluşturma
description: Bu konuda Varlık Yönetimi'nde tüketim raporları oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e32924c71fd221caee4a7f413908120014ec8c5
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022545"
---
# <a name="create-consumption-reports"></a>Tüketim raporları oluşturma

[!include [banner](../../includes/banner.md)]

 

Varlık Yönetiminde iş emirleriyle ilgili tüketim kayıtları oluşturup deftere naklettiğinizde, tüketim ayrıntılarını görüntülemek için iki rapor kullanılabilir.


## <a name="asset-consumption-report"></a>Varlık tüketim raporu

İş emirleriyle ilgili tüketimi deftere naklettiğinizde, bir varlık tüketim raporu yazdırabilirsiniz. Rapor saatleri, saat maliyetlerini, madde maliyetlerini ve varlıklarda nakledilen giderleri gösterir.

1. **Varlık yönetimi** > **Raporlar** > **Varlıklar** > **Varlık tüketimi**'ne tıklayın.

2. **Varlık tüketimi** iletişim kutusunda, ilgili düğmelerde **Evet** seçeneğini belirleyerek **Göster** bölümünde bir işlem yapılacak yerleşim düzeyi ekleyerek görmek istediğiniz parametreleri ve ayrıntı düzeyini seçin.
    - İşlem yapılacak yerleşimlerle ilgili olarak varlık satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzeyler** alanını kullanabilirsiniz. 
    
        Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm varlıklar üst düzeyde gösterilir ve dolayısıyla bir satır alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir. 
        
        **Düzeyler** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeyinde bulunan tüm varlıkları gösteren ayrıntılı bir sonuç görürsünüz. 
        
    - Rapordaki her bir alt varlığın toplamlarını görmek için **Tüm alt kıymetlerin toplamı** düğmesinde **Evet** seçeneğini belirleyin.

3. **Tarihler** bölümünde bir tarih aralığı seçin.

4. **Hedef** hızlı sekmesinde raporu ekranda görüntülemek, yazdırmak veya bir dosya veya e-posta olarak kaydetmek isteyip istemediğinizi seçin.

5. Gerekirse, raporda görüntülenecek belirli varlıklar seçebilirsiniz. **Dahil edilecek raporlar** hızlı sekmesinde, **Filtre**'ye tıklayıp rapora dahil etmek istediğiniz varlıkları ekleyin.

6. Raporu oluşturmak için **Tamam**'a tıklayın.


## <a name="work-order-consumption-report"></a>İş emri tüketim raporu

İş emirleriyle ilgili tüketimi deftere naklettiğinizde, bir iş emri tüketim raporu yazdırabilirsiniz. Rapor saatleri, saat maliyetlerini, madde maliyetlerini ve iş emirlerinde nakledilen giderleri gösterir.

1. **Varlık yönetimi** > **Raporlar** > **İş emirleri** > **İş emri tüketimi**'ne tıklayın.

2. **İş emri tüketimi** iletişim kutusunda, **Göster** bölümünde ilgili iki durumlu düğmelerde **Evet** seçeneğini belirleyerek rapora dahil etmek istediğiniz parametreleri seçin.

3. **Tarihler** bölümünde bir tarih aralığı seçin.

4. **Hedef** hızlı sekmesinde raporu ekranda görüntülemek, yazdırmak veya bir dosya veya e-posta olarak kaydetmek isteyip istemediğinizi seçin.

5. Gerekirse, raporda görüntülenecek belirli iş emirleri seçebilirsiniz. **Dahil edilecek raporlar** hızlı sekmesinde, **Filtre**'ye tıklayıp rapora dahil etmek istediğiniz iş emirlerini ekleyin.

6. Raporu oluşturmak için **Tamam**'a tıklayın.


>[!NOTE]
>Ayrıca, daha fazla iş emri ayrıntısı içeren [iş emri raporu](../work-orders/work-order-report.md) da oluşturabilirsiniz.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]