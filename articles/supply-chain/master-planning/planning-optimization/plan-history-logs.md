---
title: Plan geçmişini ve planlama günlüklerini görüntüleme
description: Bu makale, Planlamayı En İyi Duruma Getirme işlevi tarafından tetiklenen planlama işlerinin geçmişini nasıl görüntüleyeceğinizi açıklar.
author: t-benebo
ms.date: 06/01/2020
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: b2c9257fc67a06b57418b2f5b035b2b540131405
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863954"
---
# <a name="view-plan-history-and-planning-logs"></a>Plan geçmişini ve planlama günlüklerini görüntüleme

[!include [banner](../../includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Supply Chain Management'ta Planlamayı En İyi Duruma Getirme işlevi tarafından tetiklenen planlama işlerinin geçmişini nasıl görüntüleyeceğinizi açıklar.

Planın geçmişini görüntülemek için **Master planlama** \> **Ayar** \> **Planlar** \> **Master planlar**'a gidip **Geçmiş**'i seçerek planı açın. Geçmiş, seçilen plan için tüm işleri listeler. Liste, tamamlanmış ve etkin işleri içerir.

Sistem, ana plan başına en fazla 60 geçmiş kaydı tutar ve 30 günden eski kayıtları siler. Yeni bir ana planlama hesaplamasını her çalıştırdığınızda, sistem yeni bir geçmiş kaydı ekler ve gerektiğinde en eski kayıtları temizler.

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
