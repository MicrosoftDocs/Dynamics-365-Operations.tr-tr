---
title: Model yönetimi yaşam döngüsü
description: Bu makalede, oluşturdukları tahminleri iyileştirmek için kuruluşunuzun makine öğrenme modellerini yönetme yolları açıklamaktadır.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 526916929e4bc079f9cea82d8ea9f80813e89b83
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880917"
---
# <a name="model-management-lifecycle"></a>Model yönetimi yaşam döngüsü

[!include [banner](../includes/banner.md)]

Bu makalede, oluşturdukları tahminleri iyileştirmek için kuruluşunuzun makine öğrenme modellerini yönetme yolları açıklamaktadır.

Yapay zeka modelini bir korumalı alan ortamında eğitmenizi ve sonra bunu üretim ortamına dağıtmak için Yönetilen çözümleri kullanmanızı öneririz. Bu yaklaşım, model yaşam döngüsünü yönetmek için doğru denetimlerin yerinde olmasını sağlamaya yardımcı olur.

Yapay zeka modeli mevcut fatura ve müşteri verilerini temel aldığından, korumalı alan ortamının üretim verilerinin en son kopyası olması önemlidir. [Müşteri ödeme tahminlerini kullan](use-customer-payment-predictions.md) adımlarını izleyerek modelinizin eğitimi yapmaya başlayabilirsiniz. Model yeniden elde eğitildikten sonra, [Başlangıçtaki müşteri ödeme tahmini modelini değerlendir](evaluate-payment-prediction.md) konusunda açıklandığı gibi sonuçları değerlendirin. Modeli geliştirmeye yardımcı olabilecek özellik ve filtre birleşimlerini denemek için [tahmin modelini geliştirme](improve-model.md) içindeki bilgileri kullanın.

Eğitim sonuçları istediğiniz gibi olduğunda, modeli üretim ortamınıza aktarmak için [AI modelinizi dağıtma](/ai-builder/distribute-model) adımlarını izleyin.
