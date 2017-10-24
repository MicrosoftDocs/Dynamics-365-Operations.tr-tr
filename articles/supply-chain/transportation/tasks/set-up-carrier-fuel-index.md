--- 
title: "Taşıyıcı yakıt dizinini ayarlama"
description: "Bu kılavuz yakıt dizin bölgesi, yakıt dizini ve taşıyıcı yakıt dizini oluşturmayı gösterir."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 81f3244ff42cf13cd93ac10656c47f8a9204ef99
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-carrier-fuel-index"></a>Taşıyıcı yakıt dizinini ayarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu kılavuz yakıt dizin bölgesi, yakıt dizini ve taşıyıcı yakıt dizini oluşturmayı gösterir. Yakıt dizin bölgesi, yakıt dizininin hangi bölgeye uygulanacağını belirtmektedir ve yakıt dizini belirli bir süre için yakıt fiyatını belirtir. Zaman içerisinde yakıt fiyatlarındaki değişimi yansıtmak için bir taşıyıcı ile birden fazla yakıt dizini ilişkilendirebilirsiniz.  Bu görevler genellikle taşımacılık düzenleyicisi tarafından yapılır. Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizi kullanarak kullanabilirsiniz.


## <a name="create-a-fuel-index-region"></a>Bir yakıt dizini bölgesi oluştur
1. Taşıma yönetimi > Kurulum > Yakıt dizinleri > Yakıt dizini bölgeleri öğesine gidin.
    * Önce faaliyet gösterdiğiniz ve farklı yakıt ek giderleri hesapladığınız bölgeleri oluşturmanız gerekir.  
2. Yeni'ye tıklayın.
3. Bölge alanına bir değer yazın.
4. İsim alanına bir değer yazın.
5. Kaydet'e tıklayın.

## <a name="create-a-fuel-index"></a>Yakıt dizini oluştur
1. Taşıma yönetimi > Kurulum > Yakıt dizinleri > Yakıt dizinleri öğesine gidin.
    * Ayarlamış olduğunuz bölgeler için geçerli yakıt fiyatını girmeniz gerekir.  
2. Yeni'ye tıklayın.
3. Bölge alanında, aramayı açmak için açılır menü düğmesine tıklayın.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Galon başına fiyat alanına bir sayı girin.
6. Yürürlükteki başlangıç tarihi ve saati alanına bir tarih ve saat girin.
7. Kaydet'e tıklayın.

## <a name="create-a-carrier-fuel-index"></a>Taşıyıcı yakıt dizini oluştur
1. Taşıma yönetimi > Kurulum > Yakıt dizinleri > Taşıyıcı yakıt dizinleri öğesine gidin.
2. Yeni'ye tıklayın.
3. Taşıyıcı yakıt dizini alanında bir değer girin.
4. Açıklama alanına bir değer girin.
5. Yeni'yi tıklatın.
6. Yürürlükteki başlangıç tarihi ve saati alanına bir tarih ve saat girin.
7. Gelen PPG alanına bir sayı girin.
    * Bu örnekte, Gelen PPG alanını 1,95'e ayarlayabilirsiniz.  
8. Giden PPG alanına bir sayı girin.
    * Bu örnekte, Giden PPG alanını 2'e ayarlayabilirsiniz.  
9. Yüzde alanına bir sayı girin.
    * Bu örnekte, yüzdeyi 3'e ayarlayabilirsiniz.  
10. Para birimi alanında, açılır menü düğmesine tıklayarak aramayı açın.
11. Listede, istenen kaydı bulun ve seçin.
12. Listede, seçili satırdaki bağlantıya tıklayın.
13. Kaydet'e tıklayın.


