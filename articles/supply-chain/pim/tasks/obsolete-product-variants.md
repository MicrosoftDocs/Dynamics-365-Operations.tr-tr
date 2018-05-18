--- 
title: "Eski ürün çeşitlerini bulma"
description: "Bu yordam eski ürünleri veya ürün çeşitlerini nasıl bulabileceğinizi ve bir ürün yaşam döngüsü durumunu eski ürünlerle nasıl ilişkilendirebileceğinizi gösterir."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d445ea2f2362f146a1e3e7bcf747898dc2cc89ba
ms.openlocfilehash: 3a59f988de5290d1d69d013b762f87d0cce10e39
ms.contentlocale: tr-tr
ms.lasthandoff: 02/08/2018

---
# <a name="find-obsolete-product-variants"></a>Eski ürün çeşitlerini bulma 

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam eski ürünleri veya ürün çeşitlerini nasıl bulabileceğinizi ve bir ürün yaşam döngüsü durumunu eski ürünlerle nasıl ilişkilendirebileceğinizi gösterir. Önkoşul: Bu görev kılavuzunu çalıştırmadan önce etkin durumda olmayan en az bir ürün yaşam döngüsü durumu tanımlamanız gerekir.


## <a name="run-a-simulation"></a>Benzetimi çalıştırma
1. Ürün yönetimi bilgileri > Periyodik görevler > Eski ürünler için yaşam döngüsü durumunu değiştir öğesine gidin.
2. Yeni ürün yaşam döngüsü durumu alanına bir değer girin veya buradan bir değer seçin.
3. Ürün verilerini güncelleştirmeden benzetimi çalıştır alanında Evet'i seçin.
4. Bu sayıda gün içinde oluşturulan ürünleri hariç tut alanına bir sayı girin.
5. Hareketlerde (belirtilen sayıda gün içinde) kullanılan ürünleri hariç tut alanına bir sayı girin.
6. Eklenecek kayıtlar bölümünü genişletin.
7. Filtre'ye tıklayın.
8. Listede, seçili satırı işaretleyin.
9. Ölçütler alanına bir değer yazın.
10. Tamam'a tıklayın.
11. Tamam'a tıklayın.

> [!NOTE]
> Çok sayıda ürün araması yapılmasını bekliyorsanız simülsayonu toplu işte çalıştırmanız önerilir. Ayrıca, simülasyonun şirketin en yoğun çalıştığı saatlerde çalışmadığından emin olun.  

## <a name="review-the-simulation-results"></a>Benzetim sonuçlarını inceleme
1. Ürün bilgileri yönetimi >Sorgular ve raporlar > Ürün yaşam döngüsü durumu bakım geçmişi öğesine gidin.
   
> [!NOTE]
> Bu sayfada, benzetim sonuçlarını inceleyebilir ve benzetim olmadan güncelleştirme çalıştırıldığında ne kadar ürün ve ürün çeşidinin yeni bir ürün yaşam döngüsü durumuyla ilişkilendirileceğini değerlendirebilirsiniz.  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a>Eski ürünler için ürün yaşam döngüsü durumu güncelleştirmesini çalıştırma
1. Sayfayı kapatın.
2. Ürün yönetimi bilgileri > Periyodik görevler > Eski ürünler için yaşam döngüsü durumunu değiştir öğesine gidin.
3. Eklenecek kayıtlar bölümünü genişletin.

> [!NOTE]
> Son seçimin kaydedildiğini unutmayın.  

4. Ürün verilerini güncelleştirmeden benzetimi çalıştır alanında Hayır'ı seçin.
5. Arka planda çalıştır bölümünü genişletin.

> [!NOTE]
> Kaç ürün ve ürün çeşidinin etkilendiğine bağlı olarak, bu işi toplu iş olarak çalıştırmayı düşünün. Büyük bir güncelleştirme işini şirketin yoğun olduğu saatlerde çalıştırmadığınızdan emin olun.  

6. Tamam'a tıklayın.
7. Ürün bilgileri yönetimi >Sorgular ve raporlar > Ürün yaşam döngüsü durumu bakım geçmişi öğesine gidin.

> [!NOTE]
> Değiştirilen serbest bırakılmış ürünleri ve ürün çeşitlerini inceleyin.  

8. Listede, istenen kaydı bulun ve seçin.


