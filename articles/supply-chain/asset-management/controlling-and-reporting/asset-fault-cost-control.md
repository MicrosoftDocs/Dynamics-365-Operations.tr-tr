---
title: Kıymet hata maliyeti denetimi
description: Bu konuda Varlık Yönetimi'nde varlık arıza maliyet denetimini açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: 2fe75c327cdc2bdd76173430ed551895f5941c7b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918315"
---
# <a name="asset-fault-cost-control"></a>Kıymet hata maliyeti denetimi

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Varlık Yönetimi'nde, varlık arıza kayıtlarındaki maliyetleri hesaplayarak fiili maliyetlerin arızalardaki bütçe maliyetlerine karşılaştırmasına genel bakış elde edebilirsiniz. Fiili maliyetler deftere nakledilen hareketleri temel alarak yapılır. Tarih, belirtinin kaydedildiği arıza tarihidir.

1. **Varlık Yönetimi** > **Sorgular** > **Varlık hatası** > **Varlık hata maliyet denetimi**'ni tıklatın.

2. **Varlık arıza maliyeti denetimi** iletişim kutusunda, gerekirse hesaplamaya dahil edilecek bir mali boyut kümesi seçin.

4. Sıfır saat içeren sonuçları göstermek istemiyorsanız, **sıfır atlama** düğmesi üzerinde "Evet" seçeneğini belirleyin.

5. İşlem yapılacak yerleşimlerle ilgili olarak maliyet denetimi satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz. Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm varlık arızası maliyet denetimi satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir. **Düzey** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm varlık arıza maliyet denetimi satırlarını gösteren ayrıntılı bir sonuç görürsünüz.

6. Aramayı sınırlandırmak istiyorsanız, Hızlı Sekme **dahil edilecek kayıtlar** üzerinde belirli kıymetleri, arıza tarihlerini, arıza nedenlerini ve arızaları seçebilirsiniz.

7. Hesaplamayı başlatmak için **Tamam**'a tıklayın.

8. **Gruplandırma ölçütü...** eylem bölmesi gruplarında, hesaplamanın gerekli ayrıntı düzeyini göstermek için ilgili düğmelere tıklayın. Seçilen eylem bölmesi düğmeleri vurgulanır. Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.

Aşağıdaki şekil, varlık arıza maliyeti denetimi hesaplamasının birkaç örneğini göstermektedir.

![Şekil 1](media/05-controlling-and-reporting.png)

Varsayılanları ayarlamak hakkında bilgi için [Arıza yönetimi](../setup-for-work-orders/fault-management.md)'ne başvurun.

>[!NOTE]
>**Orijinal bütçe** alanı, bütçe maliyetlerini iş emri tahmininden gösterir. **Fiili maliyet** alanı, iş emirlerinde deftere nakledilen maliyetleri gösterir. **Taahhüt edilen maliyet** alanı, şirketinizin iş siparişleri ile ilgili olarak taahhüt edildiği toplam maliyet miktarını gösterir.
