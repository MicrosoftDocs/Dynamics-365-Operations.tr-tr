---
title: Yapılandırma kuralları oluşturma
description: Bu yordam, çeşitli ürün reçetesi satırlarının oluşmasını engellemek veya zorlamak için boyut tabanlı yapılandırmada kullanılmak üzere konfigürasyon kurallarını oluşturur.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1b0bcf126f8b438f13ec7cc3537dfe1dab8c275
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569613"
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