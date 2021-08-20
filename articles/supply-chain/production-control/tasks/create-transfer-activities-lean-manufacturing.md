---
title: Yalın imalat için transfer faaliyetleri oluşturma
description: Yalın imalat için bir transfer faaliyeti oluşturun.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a7d65b3de38f74f1b4d8b5170cd3eba585cecfb19e7e349bda9a6306f335f58
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742088"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a>Yalın imalat için transfer faaliyetleri oluşturma

[!include [banner](../../includes/banner.md)]

Yalın imalat için bir transfer faaliyeti oluşturun. 

Ön koşullar: 

1. Bir üretim akışı ve etkin olmayan sürüm oluşturulmalıdır.

2. Başlangıç ve bitiş ambarı ve konumları oluşturulmalıdır. İsteğe bağlı olarak, yenileme veya yenilenen iş hücresi oluşturulmalıdır.


## <a name="find-the-production-flow-version"></a>Üretim akışı sürümünü bul
1. Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.
2. Listede, istenen kaydı bulun ve seçin.
    * Üretim akışı sürümünün taslak durumda olması gerektiğini unutmayın.  
3. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="create-a-new-activity"></a>Yeni bir faaliyet oluştur
1. Faaliyetler'i tıklatın.
    * Seçili üretim akışında taslak halde bir sürüm olduğundan emin olun ve o sürümü seçin.  
2. Yeni plan faaliyeti oluştur'u tıklatın.
3. İleri düğmesini tıklatın.
4. İsim alanına bir değer yazın.
5. Faaliyet türü alanında, 'Transfer' seçeneğini işaretleyin.
6. İşlem miktarı alanında bir sayı girin.
7. İleri düğmesini tıklatın.

## <a name="select-the-work-cells"></a>İş hücrelerini seç
1. Yenileme alanında, aramayı açmak için açılır menü düğmesini tıklatın.
    * İş hücresi çıkış konumunu transfer faaliyetindeki çıkış konumu olarak kullanmak için bir iş hücresi seçin. Aynı işlem transfer faaliyetinin hedef konumunu ayarlayan yenilenen iş hücresi için de yapılabilir.  
2. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="define-the-inventory-updates"></a>Stok güncelleştirmelerini tanımla
1. Ürün türü alanında bir seçenek seçin.
    * Yapılan bir transferin ürünün türünü değiştirmeyeceğini unutmayın. Bitmiş ürünlerin veya yarı bitmiş ürünlerin transferini gerçekleştirebilirsiniz (bir üretim akışı ve olası bir kanban akışı iki faaliyet arasındaki transfer).     Bitmiş ürünlerin transferi yapılırken, malzeme çekilmesi veya alınması sonuçlarını bir stok hareketinde görmeyi seçebilirsiniz.  

## <a name="define-the-transfer-locations"></a>Transfer konumlarını tanımla
1. İleri düğmesini tıklatın.
2. Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.
3. Listede, istenen kaydı bulun ve seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Yerleşim alanında, açılır menü düğmesine tıklayarak aramayı açın.
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. Navlun sorumlusu alanında 'Sevkiyatçı' öğesini seçin.
    * Seçenekler şunlardır: Sevkiyatçı - sevk ambarını işleten şirket, Alıcı - alım ambarını işleten şirket, Taşıyıcı - üçüncü taraf sağlayıcı. Faaliyet gösteren şirket bir satıcıysa, transfer faaliyeti için bir alt sözleşme gerekir.  
8. İleri düğmesini tıklatın.

## <a name="define-the-activity-times"></a>Faaliyet sürelerini tanımla
1. Listede, istenen kaydı bulun ve seçin.
    * Çalışma zamanı tanımı gereklidir. Çalışma zamanı, kanban işlerinin maliyetini ve iş çıkarma yeteneği sürelerini hesaplamak için kullanılır. Çalışma zamanları kapasite yükü ve tüketimi hesaplamak için kullanılmaz, üretim akışı sürümü görevinden türetilmiş döngü süresiyle hesaplanır.  
2. Zaman alanında bir sayı girin.
3. Birim alanına bir değer yazın.
4. Zaman birimini seçin.
5. Miktar başına alanında bir sayı girin.
6. Listede, istenen kaydı bulun ve seçin.
    * Kuyruk süreleri isteğe bağlıdır.  
7. Zaman alanında bir sayı girin.
8. Birim alanına bir değer yazın.
9. Zaman birimini seçin.
10. Miktar başına alanında bir sayı girin.
11. İleri düğmesini tıklatın.
12. Son düğmesini tıklatın.
13. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]