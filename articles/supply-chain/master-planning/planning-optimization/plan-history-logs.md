---
title: Plan geçmişini ve planlama günlüklerini görüntüleme
description: Bu konu, Planlamayı En İyi Duruma Getirme işlevi tarafından tetiklenen planlama işlerinin geçmişini nasıl görüntüleyeceğinizi açıklar.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 757d2103bd629c0107a3f29599196a56ea56d431a66cf1e69c7b3cf3d817c087
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724832"
---
# <a name="view-plan-history-and-planning-logs"></a>Plan geçmişini ve planlama günlüklerini görüntüleme

[!include [banner](../../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta Planlamayı En İyi Duruma Getirme işlevi tarafından tetiklenen planlama işlerinin geçmişini nasıl görüntüleyeceğinizi açıklar.

Planın geçmişini görüntülemek için **Master planlama** \> **Ayar** \> **Planlar** \> **Master planlar**'a gidip **Geçmiş**'i seçerek planı açın. Geçmiş, seçilen plan için tüm işleri listeler. Liste, tamamlanmış ve etkin işleri içerir.

Planlama Optimizasyonu master planlama çalıştırma işlerinin geçmişi, master plan başına yalnızca 60'a kadar kayıt saklar. Yeni bir master planlama hesaplaması çalıştırdığınızda, ilgili planın en eski geçmiş kaydı silinir.

İşlerin başlama zamanını ve durumunu görmeye ek olarak, belirli bir iş için günlüğü de görüntüleyebilirsiniz. Günlük, ek bilgiler ve uyarılar içerir. Tüm işlerin günlüğü olmayabilir. İşin günlüğünü görüntülemek için **Günlük** öğesini seçin. Günlük girişleri, iş tamamlandıktan sonra yalnızca 30 gün saklanır. Bu tarihten sonra otomatik olarak silinirler.

Master planlama işlemi ayarlandığında **Arka planda çalıştır** hızlı sekmesindeki **Toplu işlem** seçeneği etkinleştirilmişse toplu işlem günlüğü ana planlama çalıştırması sırasında oluşturulan uyarılar ve hatalar hakkında daha fazla bilgi gösterir. Örneğin, otomatik kesinleştirme hataları yalnızca toplu iş günlüğünde yakalanır. **Geçmiş** sayfasındaki günlüklerde gösterilmezler.

Master planlama çalıştırması sırasında oluşan otomatik kesinleştirme hatalarını ve diğer uyarıları veya hataları görüntülemek için şu adımları izleyin.

1. **Sistem Yönetimi \> Sorgular \> Toplu işler**'e gidin.
1. İlgilendiğiniz ana planlama çalıştırmasını temsil eden kaydı bulun ve seçin. (Örneğin, **Proje açıklaması** alanının değeri *Master planlama* ile başlayabilir.)
1. **Toplu işler** sayfası için *gelişmiş formu* mu yoksa *eski (geliştirilmemiş)* formu mu kullandığınıza bağlı olarak şu adımlardan birini izleyin:

    - Gelişmiş formu kullanıyorsanız: Eylem Bölmesi'nde **Toplu işlem geçmişi**'ni seçin. Ardından, **Toplu işlem geçmişi** sayfasında, Eylem Bölmesi'nde **Günlük**'ü seçin.
    - Eski formu kullanıyorsanız: Eylem Bölmesi'nde, **Toplu işlem** sekmesinde **Günlük**'ü seçin.

1. İşlem sırasında yakalanan tüm uyarıları ve hataları görüntüleyebileceğiniz **İleti ayrıntıları** bölmesini açmak için **İleti ayrıntıları**'nı seçin.

## <a name="related-resources"></a>İlgili kaynaklar

- [Planlama Optimizasyonuna genel bakış](planning-optimization-overview.md)
- [Planlama Optimizasyonunu kullanmaya başlama](get-started.md)
- [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md)
- [Plana filtre uygulama](plan-filters.md)
- [Planlama işini iptal etme](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
