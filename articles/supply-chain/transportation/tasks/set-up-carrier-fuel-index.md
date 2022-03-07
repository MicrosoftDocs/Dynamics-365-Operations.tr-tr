---
title: Taşıyıcı yakıt dizinini ayarlama
description: Bu kılavuz yakıt dizin bölgesi, yakıt dizini ve taşıyıcı yakıt dizini oluşturmayı gösterir.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFuelIndexRegion,TMSCarrierFuelIndexTable,TMSFuelIndex
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 504c5143fac0e46f4d7be134d400ae53d999d25b1b364fe0278343b3d7664bf0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782335"
---
# <a name="set-up-a-carrier-fuel-index"></a>Taşıyıcı yakıt dizinini ayarlama

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]