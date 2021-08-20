---
title: Kıymet hata maliyeti denetimi
description: Bu konuda Varlık Yönetimi'nde varlık arıza maliyet denetimini açıklanmaktadır.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c36fc791fac6cce0433935adb88eb8cdc23003368204a87efc12cf5a419ec9d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752045"
---
# <a name="asset-fault-cost-control"></a>Kıymet hata maliyeti denetimi

[!include [banner](../../includes/banner.md)]

 

Varlık Yönetimi'nde, varlık arıza kayıtlarındaki maliyetleri hesaplayarak fiili maliyetlerin bütçe maliyetlerine karşılaştırmasına genel bakış elde edebilirsiniz. Fiili maliyetler deftere nakledilen hareketleri temel alarak yapılır. Tarih, belirtinin kaydedildiği arıza tarihidir.

1. **Varlık Yönetimi** > **Sorgular** > **Varlık hatası** > **Varlık hata maliyet denetimi**'ni tıklatın.

2. **Varlık arıza maliyeti denetimi** iletişim kutusunda, gerekirse hesaplamaya dahil edilecek bir mali boyut kümesi seçin.

4. Sıfır saat içeren sonuçları göstermek istemiyorsanız, **sıfır atlama** düğmesi üzerinde "Evet" seçeneğini belirleyin.

5. İşlem yapılacak yerleşimlerle ilgili olarak maliyet denetimi satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz. 

    Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm varlık arızası maliyet denetimi satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir. 
    
    **Düzey** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm varlık arıza maliyet denetimi satırlarını gösteren ayrıntılı bir sonuç görürsünüz.

6. Aramayı sınırlandırmak istiyorsanız, Hızlı Sekme **dahil edilecek kayıtlar** üzerinde belirli kıymetleri, arıza tarihlerini, arıza nedenlerini ve arızaları seçebilirsiniz.

7. Hesaplamayı başlatmak için **Tamam**'a tıklayın.

8. **Gruplandırma ölçütü** düğmelerine tıklayarak hesaplamanın gerekli ayrıntı düzeyini görüntüleyin. Seçilen **Gruplandırma ölçütü** düğmeleri vurgulanır. Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.

## <a name="example"></a>Örnek

Bu örnekte, varlık arıza maliyeti denetim hesaplaması gösterilmektedir.

- **Orijinal bütçe** alanı, bütçe maliyetlerini iş emri tahmininden gösterir. 
- **Fiili maliyet** alanı, iş emirlerinde deftere nakledilen maliyetleri gösterir. 
- **Taahhüt edilen maliyet** alanı, şirketinizin iş siparişleri ile ilgili olarak taahhüt edildiği toplam maliyet miktarını gösterir.

    ![Şekil 1.](media/05-controlling-and-reporting.png)

Arızaları ayarlama hakkında bilgi için [Arıza yönetimi](../setup-for-work-orders/fault-management.md) konusuna bakın.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]