---
title: Plan geçmişini ve planlama günlüklerini görüntüleme
description: Bu makalede planlama işleri geçmişinin nasıl görüntüleneceği açıklanmaktadır.
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
ms.openlocfilehash: ab469686a009364bf53cb963506fd2107075a283
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740944"
---
# <a name="view-plan-history-and-planning-logs"></a>Plan geçmişini ve planlama günlüklerini görüntüleme

[!include [banner](../../includes/banner.md)]

Bu makalede Microsoft Dynamics 365 Supply Chain Management uygulamasında, planlama işleri geçmişinin nasıl görüntüleneceği açıklanmaktadır.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
