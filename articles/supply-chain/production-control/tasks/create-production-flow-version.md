---
title: Üretim akışı sürümü oluşturma
description: Bu yordam, yeni bir üretim akışı sürümünü oluşturmaya odaklanır.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 115463c57b28e681d4c6bdc227e35272861779aa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006928"
---
# <a name="create-a-production-flow-version"></a>Üretim akışı sürümü oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, yeni bir üretim akışı sürümünü oluşturmaya odaklanır. Bu yordam için yalın üretim ve sınıf zaman ölçümü birimleri için üretim parametreleri tanımlanmalıdır. Ayrıca bir değer akışı ve üretim grubu tanımlamanız gerekir. Üretim akışları ve yalın üretim faaliyetleri hakkında daha fazla bilgi için Microsoft Dynamics AX için yalın üretim teknik incelemelerine bakın. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-a-production-flow"></a>Üretim akışı oluşturun
1. Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.
6. Listede, seçili satırdaki bağlantıya tıklayın.
    * Değer akış türünde bir işletme birimi seçin. Bir değer akışı, değer akışının tüm aktivitelerini ve hareketlerini kapsayan işletme bir birimidir. Bu aşamada, işletme birimleri bir tüzel varlık ile sınırlıdır ve hiçbir ek işlevselliğe sahip değildirler.  
7. Üretim grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.
8. Listede, seçili satırdaki bağlantıya tıklayın.
    * Üretim akışı için bir üretim grubu seçin. Üretim grupları, bir üretim işlemi için malzeme, işçilik ve Süren iş hesaplarını tanımlamayı sağlar. Üretim akışını bir hesap bağlamıyla ilişkilendirmek için bir üretim grubu seçilmelidir.  
9. Kaydet'e tıklayın.

## <a name="create-a-production-flow-version"></a>Üretim akışı sürümü oluşturma
1. Ekle öğesini tıklatın.
2. Bitiş tarihi alanına bir tarih ve saat girin.
    * Gerekirse, sürüm için bir sona erme tarihi tanımlayın. Etkin versiyonlar için bile verilen istediğiniz zaman güncelleştirebilirsiniz. Aşama bir sürümünü planlamak için kullanabilirsiniz.  
3. Tamam'a tıklayın.
4. Listede, seçili satırı işaretleyin.
5. Birim alanına bir değer yazın.
6. Takt birimini ResolveChanges.
7. Ortalama takt zamanı alanına bir sayı girin.
    * Sürümün ortalama takt süresini tanımlayın. Üretim akışı sürümünün takt denetimi için hedeflenen ortalama takt zamanını tanımlayın. Takt, zaman aralığına düşen miktar olarak tanımlanır. Örnekte, takt zamanı 10 parça başına 0.2 saattir. 8 saatlik bir çalışma zamanı için, günlük 400 parçalık üretim kapasitesine karşılık gelir.  
8. Miktar esası döngüsü alanında bir sayı girin.
    * Ortalama takt zamanına düşen döngü başına miktarı tanımlayın.  
9. Sürüm detayları bölümünün genişletilmiş görünümüne geçin.
10. Minimum takt zamanı alanına bir sayı girin.
    * Minimum takt zamanını tanımlayın. Minimum takt zamanı ortalama takt süresine eşit veya daha küçük olmalıdır.  
11. Maksimum takt zamanı alanına bir sayı girin.
    * Maksimum takt zamanı ortalama takt süresine eşit veya daha büyük olmalıdır.  
12. Döneme ait gerçek döngü süresi (gün) alanına bir sayı girin.
    * Döneme ait gerçek döngü süresini, gün sayısı olarak girin. Döneme ait gerçek döngü süresi, güncel dakikadan geriye yönelik toplanarak hesaplanan gerçek döngü süresinin gün olarak sayısıdır. Değer herhangi bir zamanda değiştirilebilir ve yalnızca gerçek döngü zamanının hesaplanması için kullanılır.  
13. Kaydet'e tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]