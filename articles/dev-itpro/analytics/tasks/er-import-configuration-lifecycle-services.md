--- 
title: "Elektronik raporlama (ER) için Lifecycle Services'tan bir yapılandırmayı içe aktarma"
description: "Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) sürümü oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'den içe aktarabilir."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9eb4f54897c84b98828c927f0f93613583fd4599
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="import-a-configuration-from-lifecycle-services-for-electronic-reporting-er"></a>Elektronik raporlama (ER) için Lifecycle Services'tan bir yapılandırmayı içe aktarma

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) sürümü oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'den içe aktarabilir.

Bu örnekte Litware, Inc. örnek şirketi için bir istenilen ER yapılandırmasını seçecek ve bunu LCS'ye içe aktaracaksınız. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir. Bu adımları tamamlamak için, öncelikle "Bir ER yapılandırmasını Lifecycle Services'a içeri almak" yordamındaki adımları tamamlamanız gerekir. Bu adımları tamamlamak için LCS erişimi de gereklidir.

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
2. Yapılandırmalar'a tıklayın.

## <a name="delete-a-shared-version-of-data-model-configuration"></a>Veri modeli yapılandırmasının paylaşılan bir sürümünü silin
1. Ağaçta seçin 'Örnek model yapılandırması' seçeneğini işaretleyin.
    * Örnek veri modeli yapılandırmasının ilk sürümü oluşturuldu ve LCS'ye "ER yapılandırmasını Lifecycle Services'a karşıya yüklemek" yordamında yayımlandı. Bu yordamda, ER yapılandırmasının bu sürümünü sileceksiniz. Bir örnek veri modeli yapılandırmasının bu modeli daha sonra LCS'den içe aktarılacaktır.  
2. Listede, istenen kaydı bulun ve seçin.
    * Bu yapılandırmanın 'Paylaşımlı' durumda olan sürümünü seçin. Bu durum, yapılandırmanın LCS için yayımlandığını gösterir.  
3. Durumu değiştir öğesine tıklayın.
4. Devam ettirme'ye tıklatın.
    * Seçili sürümün durumunu, silinebilir duruma gelmesi için 'Paylaşılan'dan 'Devam ettirilmeyen' olarak değiştirin.  
5. Tamam'a tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
    * Bu yapılandırmanın 'Devam ettirilmeyen' durumda olan sürümünü seçin.  
7. Sil'i tıklatın.
8. Evet'i tıklatın.
    * Yalnızca seçili veri modeli yapılandırması için taslak sürümü 2'nin kullanılabilir olduğunu unutmayın.  
9. Sayfayı kapatın.

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a>Veri modeli yapılandırmasının paylaşılan bir sürümünü LCS'den içeri alın
1. Listede, seçili satırı işaretleyin.
    * 'Litware, Inc.' yapılandırma sağlayıcısı için havuzların listesini açın. yapılandırma sağlayıcısı.  
2. Depolar'a tıklayın.
3. Aç'a tıklayın.
    * LCS deposunu seçin ve açın.  
4. Listede, seçili satırı işaretleyin.
    * 'Örnek yapılandırma modeli'nin ilk sürümü sürümlerin listesinde seçin.  
5. İçe aktar'ı tıklatın.
6. Evet'i tıklatın.
    * Seçili sürümün LCS'den aktarıldığını onaylayın.  
    * Bilgi iletisinin (formun üstünde bulunan) seçili sürümün alma işleminin başarılı tamamlama onayladığını dikkate alın.  
7. Sayfayı kapatın.
8. Sayfayı kapatın.
9. Yapılandırmalar'a tıklayın.
10. Ağaçta seçin 'Örnek model yapılandırması' seçeneğini işaretleyin.
11. Listede, istenen kaydı bulun ve seçin.
    * Bu yapılandırmanın 'Paylaşılan' durumda olan sürümünü seçin.  
    * Yalnızca seçili veri modeli yapılandırması için paylaşılan sürümü 1'in de artık kullanılabilir olduğunu unutmayın.  


