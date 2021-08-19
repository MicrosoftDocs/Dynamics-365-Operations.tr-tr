---
title: Eski ürün çeşitlerini bulma
description: Bu yordam eski ürünleri veya ürün çeşitlerini nasıl bulabileceğinizi ve bir ürün yaşam döngüsü durumunu eski ürünlerle nasıl ilişkilendirebileceğinizi gösterir.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 212e2a3a4ea38e60af16b8a50fdfe6f038666fdc241e3bb28ad5c57d6149ccd7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765942"
---
# <a name="find-obsolete-product-variants"></a>Eski ürün çeşitlerini bulma 

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]