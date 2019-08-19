---
title: Üretim akışını ve sürümünü doğrulama
description: Bu yordam, yalın imalat için yeni bir üretim akışının ve bir ilk sürümün nasıl oluşturulacağını gösterir.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 523f6414ec212aef48eece487f4199ea2cf4b87e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836172"
---
# <a name="validate-a-production-flow-and-version"></a>Üretim akışını ve sürümünü doğrulama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, yalın imalat için yeni bir üretim akışının ve bir ilk sürümün nasıl oluşturulacağını gösterir. Önkoşullar: Yalın imalat için üretim parametreleri ve sınıf zamanı için ölçü birimleri tanımlanmalıdır. Bir Değer akışı ve Üretim grubu tanımlamanız gerekir. Üretim akışları ve faaliyetleri kavramlarını öğrenmek üzere Yalın imalat hakkındaki teknik incelemelere bakın. Bu yordam, demo verilerindeki USMF tüzel kişiliğini referans alır. Ancak, tüzel kişiliklerin Yalın imalat için yapılandırıldığı varsayılarak diğer tüzel kişilikler de kullanılabilir.


## <a name="create-a-production-flow"></a>Üretim akışı oluşturun
1. Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.
6. Listede, seçili satırdaki bağlantıya tıklayın.
    * Bir değer akışı, değer akışının tüm faaliyetlerini ve hareketlerini kapsayan faaliyet birimidir.   Bu aşamada, işletme birimleri bir tüzel varlık ile sınırlıdır ve hiçbir ek işlevselliğe sahip değildirler.  
7. Üretim grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.
8. Listede, seçili satırdaki bağlantıya tıklayın.
    * Üretim grupları, bir üretim işlemi için malzeme, işçilik ve Süren iş hesaplarını tanımlamayı sağlar. Üretim akışını bir hesap bağlamıyla ilişkilendirmek için bir üretim grubu seçilmelidir.  
9. Kaydet'e tıklayın.

## <a name="create-a-production-flow-version"></a>Üretim akışı sürümü oluşturma
1. Ekle öğesini tıklatın.
2. Bitiş tarihi alanına bir tarih ve saat girin.
    * Sürümün bitiş tarihini, etkin sürümler için bile, istediğiniz zaman güncelleştirebilirsiniz. Sürüm dışında bir aşama planlamak için sürümün bitiş tarihini kullanın.  
3. Tamam'a tıklayın.
4. Listede, seçili satırı işaretleyin.
5. Birim alanına bir değer yazın.
6. Takt birimini seçin.
7. Ortalama takt zamanı alanına bir sayı girin.
    * Üretim akışı sürümünün takt denetimi için hedeflenen ortalama takt zamanını tanımlayın.   Takt, zaman aralığına düşen miktar olarak tanımlanır.  Verilen örnekte, takt zamanı 10 parça başına 0,2 saattir. 8 saatlik bir çalışma zamanı için, günlük 400 parçalık üretim kapasitesine karşılık gelir.  
8. Miktar esası döngüsü alanında bir sayı girin.
9. Sürümler detayları bölümünü genişletin veya daraltın.
10. Minimum takt zamanı alanına bir sayı girin.
    * Minimum takt zamanı ortalama takt süresine eşit veya daha küçük olmalıdır.  
11. Maksimum takt zamanı alanına bir sayı girin.
    * Maksimum takt zamanı ortalama takt süresine eşit veya daha büyük olmalıdır.  
12. Gerçek döngü süresi için dönem alanında bir gün sayısı gir
    * Döneme ait gerçek döngü süresi, güncel dakikadan geriye yönelik toplanarak hesaplanan gerçek döngü süresinin gün olarak sayısıdır. Değer herhangi bir zamanda değiştirilebilir ve yalnızca gerçek döngü zamanının hesaplanması için kullanılır.  
13. Kaydet'e tıklayın.

