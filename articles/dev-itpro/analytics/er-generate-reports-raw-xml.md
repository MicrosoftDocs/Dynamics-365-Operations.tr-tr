---
title: İçeriği ham XML olarak ekleyerek raporlar oluşturma
description: XML biçiminde giden belgeler oluşturan Elektronik raporlama (ER) biçimleri tasarlayabilirsiniz.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 39503d051e3b4686bbaa0130fe5be7cb980fbcb4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "312198"
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
