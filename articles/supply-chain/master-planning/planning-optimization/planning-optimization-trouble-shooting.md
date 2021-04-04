---
title: Planlamayı En İyi Duruma Getirmeyle İlgili Sorunları Giderme
description: Bu konu, Planlamayı En İyi Duruma Getirme ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 39583c244f09f54551d560e8b1dd9f1a5a1590cc
ms.sourcegitcommit: 72f70c81176e86cda714a4712525f73514c895b7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/16/2021
ms.locfileid: "5457341"
---
# <a name="troubleshoot-planning-optimization"></a>Planlamayı En İyi Duruma Getirmeyle İlgili Sorunları Giderme 

[!include [banner](../../includes/banner.md)]

Bu konu, Planlamayı En İyi Duruma Getirme ile çalışırken karşılaşabileceğiniz yaygın sorunların nasıl düzeltileceğini açıklamaktadır.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>Planlamayı En İyi Duruma Getirme eklentisinin yüklenmesi tamamlanmadı

Planlamayı En İyi Duruma Getirme; etkin bir LifeCycle Services (LCS), yüksek kullanılabilirlik ortamı, katman 2 veya üstü (OneBox ortamı olmayan), Dynamics 365 Supply Chain Management 10.0.7 veya daha yeni bir sürümünü gerektirir. Eklentiyi OneBox ortamına yüklemeye çalışırsanız, yükleme tamamlanmaz.

**Düzeltme**: Yüklemeyi iptal edin ve yüksek kullanılabilirlik ortamı, katman 2 veya daha yüksek bir ortam (OneBox ortamı olmayan) kullanın.

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Planlamayı En İyi Duruma Getirme etkinleştirildiğinde toplu işler planlanamıyor

Planlamayı En İyi Duruma Getirme'yi etkinleştirdiğinizde, yerleşik ana planlama altyapısı otomatik olarak devre dışı bırakılır. Yerleşik Supply Chain Management planlama altyapısı için oluşturulan ana planlama toplu işleri, Planlamayı En İyi Duruma Getirme etkinken tetiklenirse bu işler başarısız olur. *Bu işlem, Planlamayı En İyi Duruma Getirme etkinken desteklenmeyen ana planlamayı tetikledi* gibi bir hata iletisi alabilirsiniz.

**Düzeltme**: Yerleşik Supply Chain Management planlama altyapısı için oluşturulan tüm ana planlama toplu işlerini iptal edin.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>Planlamayı En İyi Duruma Getirme sonuçları önceki sonuçlardan farklı

Planlamayı En İyi Duruma Getirme, bazı alanlardaki yerleşik ana planlama tasarımdan farklıdır. Bunun nedeni beklemedeki özellikler de olabilir.

**Düzeltme**: Planlamayı En İyi Duruma Getirme uygun analizini çalıştırın ve sonra, etkisini anlamak için ilgili belgelere başvurarak sonuçları analiz edin. Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).

## <a name="cant-enable-planning-optimization"></a>Planlamayı En İyi Duruma Getirme etkinleştirilemiyor

**Planlamayı En İyi Duruma Getirmeyi Kullan** ayarını **Evet** olarak ayarlamadan önce **Bağlantı durumu** değerinin **Bağlı** olması gerekir. Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirmeye başlayın](get-started.md).

**Düzeltme**: Planlamayı En İyi Duruma Getirme eklentisinin başarıyla yüklendiğinden emin olun.

## <a name="error-message-is-shown-during-ctp"></a>CTP sırasında hata iletisi gösteriliyor

Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, bir satış siparişinden teslim edilebilir miktarı (CTP) çalıştırmayı denerseniz şu hata iletisini alırsınız: *Bu işlem, Planlamayı En İyi Duruma Getirme etkinken desteklenmeyen ana planlamayı tetikledi*.

Bu, üretim emirleri desteğinin bir parçası olarak planlanan beklemedeki bir özellikle ilgilidir.

**Düzeltme:** CTP desteği kullanılabilir hale gelene kadar Planlamayı En İyi Hale Getirme etkinken CTP hesaplamalarından kaçının.

## <a name="additional-resources"></a>Ek kaynaklar

[Planlamayı En İyi Duruma Getirmeyi kullanmaya başlama](get-started.md)

[Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]