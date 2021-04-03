---
title: İçeriği ham XML olarak ekleyerek raporlar oluşturma
description: XML biçiminde giden belgeler oluşturan Elektronik raporlama (ER) biçimleri tasarlayabilirsiniz.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 07fb63f7d4255ca4f693e399a066fe3952e3df1b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566686"
---
# <a name="generate-reports-by-adding-content-as-raw-xml"></a>İçeriği ham XML olarak ekleyerek raporlar oluşturma

[!include[banner](../includes/banner.md)]

XML biçiminde giden belgeler oluşturan Elektronik raporlama (ER) biçimleri tasarlamak için yeni **HAM XML** biçimi öğesini kullanabilirsiniz. Bazı durumlarda, aşağıdaki nedenlerden biri veya daha fazlası için bu raporlara ham XML verileri eklemeyi tercih edebilirsiniz:

- Bir raporun özgün tasarımı ve sürekli bakımı için ham XML kullanmak daha rahattır çünkü XML yapısı bir çalışma zamanı ifadesiyle otomatik olarak oluşturulabilir. Bu sayede, tasarım zamanında birden çok biçim öğesi için birden çok bağlama belirlenmesi gerekmez. Kullanmakta olduğunuz veri kaynaklarında, rapor oluşturulurken XML öğeleri oluşturmak için kullanılabilecek bilgiler bulunduğu zaman bu mümkündür.
- Raporu daha önce alınan ve sistemde depolanan XML içeriğiyle doldurmak için başka bir yöntem kullanılamaz. Örneğin, oluşturulan XML yanıtı, daha önce gönderilmiş XML isteği içeriğini barındırabilir.
- Oluşturulan belgeye sayısal kodlarına göre karakterler eklemek için başka yöntem kullanılamaz. Bazı diller ve karakterler için bu tür kodlar yoktur. Örneğin: Yunanca harf rho (ρ) ve HTML varlık kodları (tiz aksanlı *e* (é) için \&eacute; gibi).

> [!NOTE]
> Çerçevenin, oluşturulan belgeye **HAM XML** biçim öğesi kullanarak yerleştirilen XML içeriğinin doğruluğunu denetlemediğini unutmayın.

Bu özellik hakkında daha fazla bilgi için, **7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin birer parçası olan ve [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684)'dan indirilebilen **ER - XML raporları oluşturmak için ham XML kullanma (Bölüm 1: Veri modeli tasarlama)** ve **ER - XML raporları oluşturmak için ham XML kullanma (Bölüm 2: Rapor tasarlama ve çalıştırma)** görev kılavuzlarını oynatın. Bu görev kılavuzları, oluşturulan dosyalara ham XML verileri eklemek için bir ER biçimi yapılandırma işleminde size yol gösterir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]