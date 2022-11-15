---
title: Planlama Optimizasyonu sorunlarını giderme
description: Bu makale, Planlamayı En İyi Duruma Getirme ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.
author: t-benebo
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 37c38ab9cec8ae3c9d4decf8043b43ea2251083e
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739742"
---
# <a name="troubleshoot-planning-optimization"></a>Planlama Optimizasyonu sorunlarını giderme 

[!include [banner](../../includes/banner.md)]

Bu makale, Planlamayı En İyi Duruma Getirme ile çalışırken karşılaşabileceğiniz yaygın sorunların nasıl düzeltileceğini açıklamaktadır.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>Planlamayı En İyi Duruma Getirme eklentisinin yüklenmesi tamamlanmadı

Planlamayı En İyi Duruma Getirme; etkin bir LifeCycle Services (LCS), yüksek kullanılabilirlik ortamı, katman 2 veya üstü (OneBox ortamı olmayan), Dynamics 365 Supply Chain Management 10.0.7 veya daha yeni bir sürümünü gerektirir. Eklentiyi OneBox ortamına yüklemeye çalışırsanız, yükleme tamamlanmaz.

**Düzeltme**: Yüklemeyi iptal edin ve yüksek kullanılabilirlik ortamı, katman 2 veya daha yüksek bir ortam (OneBox ortamı olmayan) kullanın.

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Planlamayı En İyi Duruma Getirme etkinleştirildiğinde toplu işler planlanamıyor

Planlama Optimizasyonu'nu etkinleştirdiğinizde, kullanımdan kaldırılan master planlama altyapısı otomatik olarak devre dışı bırakılır. Kullanımdan kaldırılan master planlama altyapısı için oluşturulan master planlama toplu işleri, Planlama Optimizasyonu etkinken tetiklenirse bu işler başarısız olur. *Bu işlem, Planlamayı En İyi Duruma Getirme etkinken desteklenmeyen ana planlamayı tetikledi* gibi bir hata iletisi alabilirsiniz.

**Düzeltme**: Kullanımdan kaldırılan master planlama altyapısı için oluşturulan tüm master planlama toplu işlerini iptal edin.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>Planlamayı En İyi Duruma Getirme sonuçları önceki sonuçlardan farklı

Planlama Optimizasyonu bazı yönleriyle kullanımdan kaldırılan master planlama altyapısı tasarımından farklıdır. Bunun nedeni beklemedeki özellikler de olabilir.

**Düzeltme**: Planlamayı En İyi Duruma Getirme uygun analizini çalıştırın ve sonra, etkisini anlamak için ilgili belgelere başvurarak sonuçları analiz edin. Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).

## <a name="cant-enable-planning-optimization"></a>Planlamayı En İyi Duruma Getirme etkinleştirilemiyor

**Planlamayı En İyi Duruma Getirmeyi Kullan** ayarını **Evet** olarak ayarlamadan önce **Bağlantı durumu** değerinin **Bağlı** olması gerekir. Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirmeye başlayın](get-started.md).

**Düzeltme**: Planlamayı En İyi Duruma Getirme eklentisinin başarıyla yüklendiğinden emin olun.

## <a name="error-message-is-shown-during-ctp"></a>CTP sırasında hata iletisi gösteriliyor

Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, bir satış siparişinden teslim edilebilir miktarı (CTP) çalıştırmayı denerseniz şu hata iletisini alırsınız: *Bu işlem, Planlamayı En İyi Duruma Getirme etkinken desteklenmeyen ana planlamayı tetikledi*.

Bu, üretim emirleri desteğinin bir parçası olarak planlanan beklemedeki bir özellikle ilgilidir.

**Düzeltme:** CTP desteği kullanılabilir hale gelene kadar Planlamayı En İyi Hale Getirme etkinken CTP hesaplamalarından kaçının.

## <a name="additional-resources"></a>Ek kaynaklar

- [Master planlamayı kullanmaya başlama](get-started.md)
- [Planlama Optimizasyonu uygunluk analizi](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]