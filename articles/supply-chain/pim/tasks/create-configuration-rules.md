---
title: Yapılandırma kuralları oluşturma
description: Bu yordam, çeşitli ürün reçetesi satırlarının oluşmasını engellemek veya zorlamak için boyut tabanlı yapılandırmada kullanılmak üzere konfigürasyon kurallarını oluşturur.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6d5758b2903cd0a269f3e03e44b618c26e8b2310
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147883"
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

