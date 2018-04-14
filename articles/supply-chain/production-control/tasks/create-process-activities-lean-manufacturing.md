--- 
title: "Yalın imalat için işlem faaliyetleri oluşturma"
description: "Yalın imalat için bir işlem faaliyeti oluşturun."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: dd77c20b622fd8a14e1cdf77883043699f9a6317
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-process-activities-for-lean-manufacturing"></a>Yalın imalat için işlem faaliyetleri oluşturma

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Yalın imalat için bir işlem faaliyeti oluşturun. 

Ön koşullar: 

1. Bir üretim akışı ve etkin olmayan sürüm oluşturulmalıdır.

2. Bir iş hücresi oluşturulmalıdır.


## <a name="find-the-production-flow-version"></a>Üretim akışı sürümünü bul
1. Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="create-a-new-activity"></a>Yeni bir faaliyet oluştur
1. Faaliyetler'i tıklatın.
    * Seçili üretim akışında taslak halde bir sürüm olduğundan emin olun ve o sürümü seçin.  
2. Yeni plan faaliyeti oluştur'u tıklatın.
3. İleri düğmesini tıklatın.
4. İsim alanına bir değer yazın.
5. İsim alanına bir değer yazın.
    * Adın, tüm sürümlerde, sağlanan üretim akışına özgü olması gerektiğini unutmayın.  
6. İşlem miktarı alanında bir sayı girin.
    * Bunun, işçilik miktarını hesaplamak için, ne miktarda iş işleme alınacağına bakılmaksızın iş başına minimum miktar olduğunu unutmayın. İş miktarları bu miktardan saparsa, işçilik maliyeti farkı ortaya çıkar.  
7. İleri düğmesini tıklatın.

## <a name="select-the-work-cell"></a>İş hücresini seç
1. İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.
2. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="define-the-inventory-updates"></a>Stok güncelleştirmelerini tanımla
1. Eldeki girişi güncelleştir onay kutusunu işaretleyin veya işaretini kaldırın.
    * Eldekini Güncelleştir = Hayır ise, faaliyeti yarı bitmiş bir ürünü alacak şekilde tanımlayabilirsiniz (faaliyet bir sonraki ürün reçetesi düzeyine ulaşmaz).    Yarı bitmiş ürünleri tüketmek için de seçebilirsiniz.  

## <a name="define-the-picking-activities"></a>Malzeme çekme faaliyetlerini tanımla
1. İleri düğmesini tıklatın.
2. Listede, seçili satırı işaretleyin.
    * Seçili iş hücresinin giriş konumu için varsayılan bir malzeme çekme faaliyeti oluşturulur.  
3. Ekle öğesini tıklatın.
    * İş hücresi giriş faaliyeti aşamasında olmayan belirli ürünler için ek malzeme çekme faaliyetleri oluşturabilirsiniz.  
4. Listede, istenen kaydı bulun ve seçin.
5. Madde numarası alanına bir değer girin.
6. Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Bu tanım ile, faaliyette tüketilen tüm malzemeler (ikinci malzeme çekme faaliyetinde tanımlanan ürün dışında) varsayılan giriş ambarından ve konumundan çekilir. Bu ürün farklı bir ambar ve konumdan çekilir.  
7. Listede, istenen kaydı bulun ve seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. Hurda kaydet onay kutusunu işaretleyin veya işaretini kaldırın.
10. İleri düğmesini tıklatın.

## <a name="define-the-activity-times"></a>Faaliyet sürelerini tanımla
1. Listede, istenen kaydı bulun ve seçin.
    * Çalışma zamanı tanımı gereklidir. Çalışma zamanı, kanban işlerinin maliyetlerini ve iş çıkarma yeteneği sürelerini hesaplamak için kullanılır. Çalışma zamanları kapasite yükü ve tüketimi hesaplamak için kullanılmaz, bu, üretim akışı sürümü görevinden türetilmiş döngü süresiyle hesaplanır.  
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


