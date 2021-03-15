---
title: Malların kalitesini denetleme
description: Bu konu, bir kalite emrinin nasıl işleyeceğini açıklar.
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbfb3733cc52f0f8f54ab4388764429387358ee7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011534"
---
# <a name="inspect-the-quality-of-goods"></a>Malların kalitesini denetleme

[!include [banner](../../includes/banner.md)]

Bu konu, bir kalite emrinin nasıl işleyeceğini açıklar. Bu kılavuzu USMF demo şirketinde çalıştırabilirsiniz. Bu örnek işleme başlamadan önce "000016" satınalma siparişini onaylamanız ve ürün alış irsaliyesini deftere nakletmeniz gerekir. Bu otomatik olarak bir kalite emri oluşturur. Kalite incelemeleri genellikle bir kalite memuru tarafından gerçekleştirilir.


## <a name="select-a-quality-order"></a>Bir kalite emri seçin
1. Gezinti panelinde **Modüller > Stok yönetimi > Periyodik görevler > Kalite yönetimi > Kalite emirleri** öğesine gidin.
2. Bu yordamı başlatmadan önce oluşturulan kalite emrini seçin.  

## <a name="record-test-results"></a>Test sonuçlarını kaydetme
1. **Sonuçlar**'ı seçin.
2. **Düzenle** öğesini seçin.
3. **Sonuç miktarı** alanında bir sayı girin.
4. **Tesis** alanında, açılır menüden istediğiniz kaydı seçin.  
- Bu örnekte sonuç, önceden tanımlanmış bir sonuca bağlıdır. Normalde, örneğin bir ebat veya başka bir boyut gibi, daha belirli bir test sonucu kaydedersiniz.  
5. **Kaydet**'i seçin.
6. Sayfayı kapatın.

## <a name="validate-the-quality-order"></a>Kalite emrini doğrula
1. **Doğrula**'yı seçin.
2. **Doğrulayan** alanında, açılan menüden denetimi gerçekleştiren kullanıcıyı seçin.  
3. **Seç**'e tıklayın.
4. **Tamam**'ı seçin.
5. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]