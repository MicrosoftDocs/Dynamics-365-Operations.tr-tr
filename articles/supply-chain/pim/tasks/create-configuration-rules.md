---
title: Yapılandırma kuralları oluşturma
description: Bu yordam, çeşitli ürün reçetesi satırlarının oluşmasını engellemek veya zorlamak için boyut tabanlı yapılandırmada kullanılmak üzere konfigürasyon kurallarını oluşturur.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d75e9ecaa814085e8fce1836125553511cf4f48b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999743"
---
# <a name="create-configuration-rules"></a>Yapılandırma kuralları oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, çeşitli ürün reçetesi satırlarının oluşmasını engellemek veya zorlamak için boyut tabanlı yapılandırmada kullanılmak üzere konfigürasyon kurallarını oluşturur. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Boyut tabanlı yapılandırma birleşimlerini nasıl oluşturulacağını açıklayan sekiz prosedür arasındaki yedinci budur.

1. Ürün bilgi yönetimi > Ürün reçeteleri, malzemeler ve formülleri > Ürün reçetesi seçeneğine git.
2. Listede, istenen kaydı bulun ve seçin.
    * Boyut tabanlı yapılandırma için ürün reçetesini bulun ve seçin.  
3. Eylem Bölmesinde, Seçenekler'e tıklayın.
4. Görünümü değiştir'e tıklayın.
5. Başlık görünümü'ne tıklayın.
    * Konfigürasyon rotası hızlı sekmesine erişim için üstbilgi görünümünü açın.  
6. Yapılandırma yolu bölümünü genişletin veya daraltın.
    * Konfigürasyon rotası hızlı sekmesinin genişletilmiş modda olması gerekir.  
7. Konfigürasyon kuralları'na tıklayın.
8. Yeni'ye tıklayın.
9. Listede, seçili satırı işaretleyin.
10. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Geçerli konfigürasyon grubu içindeki öğeler görüntülenir. Kuraldaki koşulu temsil eden birini seçin.  
11. Listede, seçili satırdaki bağlantıya tıklayın.
12. Yöntem alanında bir seçenek belirtin.
    * Başka bir konfigürasyon grubundaki bir maddenin seçilmesi veya seçiminin kaldırılmasını zorlamak mümkündür.  
13. Türetilen grup alanında, aramayı açmak için açılır menü düğmesine tıklayın.
14. Listede, istenen kaydı bulun ve seçin.
15. Listede, seçili satırdaki bağlantıya tıklayın.
    * İstenen konfigürasyon grubunu seçin.  
16. Türetilen madde numarası alanında, aramayı açmak için açılır menü düğmesine tıklayın.
17. Listede, seçili satırdaki bağlantıya tıklayın.
    * Tercih edilen yönteme göre seçilecek veya seçimi kaldırılacak madde numarasını seçin.  
18. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]