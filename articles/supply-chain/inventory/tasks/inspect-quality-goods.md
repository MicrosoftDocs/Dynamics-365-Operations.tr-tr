---
title: Malların kalitesini denetleme
description: Bu konu, kalite emirlerinin nasıl işleneceğini açıklar.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b881f9c6f872061864d4254ce880d981ca71c479
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219049"
---
# <a name="inspect-the-quality-of-goods"></a>Malların kalitesini denetleme

[!include [banner](../../includes/banner.md)]

Bu konu, kalite emirlerinin nasıl işleneceğini açıklar. Kalite incelemeleri genellikle bir kalite memuru tarafından gerçekleştirilir.

Standart [demo verileri](../../../fin-ops-core/fin-ops/get-started/demo-data.md) yüklüyse, bu konudaki prosedürleri tamamlamak için kullanabilirsiniz. Demo verilerini kullanmak için, başlamadan önce *USMF* tüzel kişiliğini seçin. Daha sonra satınalma siparişi *000016*'yı onaylamanız ve bir ürün girişini deftere nakletmeniz gerekir. Bir kalite emri otomatik olarak oluşturulur.

## <a name="step-1-select-a-quality-order"></a>1. Adım: Bir kalite emri seçin

Bir kalite emri seçmek için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Kalite emirleri**'ne gidin.
1. Bu yordamı başlatmadan önce oluşturulan kalite emrini seçin.

## <a name="step-2-record-test-results"></a>2. Adım: Test sonuçlarını kaydetme

Test sonuçlarını kaydetmek için aşağıdaki adımları izleyin.

1. **Sonuçlar**'ı seçin.
1. **Düzenle** öğesini seçin.
1. **Sonuç miktarı** alanında bir sayı girin.
1. **Sonuç** alanında, istenilen kaydı seçin. Bu örnekte sonuç, önceden tanımlanmış bir sonuca bağlıdır. Genellikle, bir ebat veya başka bir boyut gibi, daha belirli bir test sonucu kaydedersiniz.
1. **Kaydet**'i seçin.
1. Sayfayı kapatın.

## <a name="step-3-validate-the-quality-order"></a>3. Adım: Kalite emrini doğrulayın

Bir kalite emrini doğrulamak için aşağıdaki adımları izleyin.

1. **Doğrula**'yı seçin.
1. **Doğrulayan kişi** alanında, denetimi yapan kullanıcıyı seçin.
1. **Seç** öğesini seçin.
1. **Tamam**'ı seçin.
1. Sayfayı kapatın.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
