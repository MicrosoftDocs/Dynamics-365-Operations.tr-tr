---
title: Model yönetimi yaşam döngüsü (önizleme)
description: Bu konu, oluşturdukları tahminleri en iyi duruma getirmek için kuruluşunuzun makine öğrenme modellerini yönetme yollarını açıklamaktadır.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 3daec03b7ba349d8f72863317e2d601a83417d58
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638404"
---
# <a name="model-management-lifecycle-preview"></a>Model yönetimi yaşam döngüsü (önizleme)

[!include [banner](../includes/banner.md)]

Bu konu, oluşturdukları tahminleri en iyi duruma getirmek için kuruluşunuzun makine öğrenme modellerini yönetme yollarını açıklamaktadır.

Yapay zeka modelini bir korumalı alan ortamında eğitmenizi ve sonra bunu üretim ortamına dağıtmak için Yönetilen çözümleri kullanmanızı öneririz. Bu yaklaşım, model yaşam döngüsünü yönetmek için doğru denetimlerin yerinde olmasını sağlamaya yardımcı olur.

Yapay zeka modeli mevcut fatura ve müşteri verilerini temel aldığından, korumalı alan ortamının üretim verilerinin en son kopyası olması önemlidir. [Müşteri ödeme tahminlerini kullan](use-customer-payment-predictions.md) adımlarını izleyerek modelinizin eğitimi yapmaya başlayabilirsiniz. Model yeniden elde eğitildikten sonra, [Başlangıçtaki müşteri ödeme tahmini modelini değerlendir](evaluate-payment-prediction.md) konusunda açıklandığı gibi sonuçları değerlendirin. Modeli geliştirmeye yardımcı olabilecek özellik ve filtre birleşimlerini denemek için [tahmin modelini geliştirme](improve-model.md) içindeki bilgileri kullanın.

Eğitim sonuçları istediğiniz gibi olduğunda, modeli üretim ortamınıza aktarmak için [AI modelinizi dağıtma](https://docs.microsoft.com/ai-builder/distribute-model) adımlarını izleyin.
