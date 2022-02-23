---
title: Ürün yapılandırma modeli oluşturma
description: Bu yordam, bir ürün yapılandırma modelinin nasıl oluşturulacağını ve öznitelikler ve alt bileşenler gibi temel bilgilerin nasıl girileceğini gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c81b3af7460c636245dcc16affcb05b724fbc70
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439297"
---
# <a name="create-a-product-configuration-model"></a>Ürün yapılandırma modeli oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, bir ürün yapılandırma modelinin nasıl oluşturulacağını ve öznitelikler ve alt bileşenler gibi temel bilgilerin nasıl girileceğini gösterir. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-a-product-model"></a>Ürün modeli oluşturma
1. Ürün varyantı model tanımı'na tıklayın.
2. Ürün yapılandırma modelleri'ne tıklayın.
3. Yeni'yi tıklatın.
4. İsim alanına bir değer yazın.
5. Açıklama alanına bir değer girin.
6. Çözüm stratejisi alanında bir seçenek belirleyin.
    * Çözüm stratejisi, kısıtlama tabanlı bir ürün yapılandırması modelindeki kısıtlamaların nasıl işleme koyulacağını belirler. Bu seçimin ürün yapılandırma modelinin performansı üzerinde etkisi olabilir.  
7. İsim alanına bir değer yazın.
    * Kök bileşen, ürün yapılandırması modelini temsil eder ve diğer ürün modellerinde de kullanılabilir.  
8. Tamam'a tıklayın.
9. Yeniden kullanma yapılandırması alanında bir seçenek belirleyin.
    * Yapılandırmaları yeniden kullanma parametresi Evet olarak ayarlanırsa, sistem her bir yapılandırma oturumunun ardından eşdeğer yapılandırmaları denetler ve tam bir eşleşme bulunursa onları yeniden kullanır.  

## <a name="add-attributes"></a>Öznitelikler ekle
1. Öznitelikler bölümünü genişletin.
2. Ekle öğesini tıklatın.
3. Listede, seçili satırı işaretleyin.
4. İsim alanına bir değer yazın.
5. Çözücü adı alanında bir değer girin.
    * Çözücü adı, ürün yapılandırıcının çözücüsü tarafından kullanılır. Boşluk veya _ (alt çizgi) dışında özel karakterler içermemelidir.  
6. Açıklama alanına bir değer girin.
    * Açıklama metni yapılandırma kullanıcısı tarafından görülür ve dolayısıyla doğru öznitelik değerinin seçilmesine yardımcı olabilir.  
7. Öznitelik türü alanında bir değer girin veya seçin.
    * Öznitelik türü, hangi değerlerin öznitelik için kullanılabilir olduğunu belirler.  
8. Yeniden kullanıma dahil et onay kutusunu işaretleyin.
    * Bu seçenek yalnızca Yapılandırmaları yeniden kullanma seçeneği belirlendiğinde kullanılabilir. Yeniden kullan onay kutusunda öznitelik eklenmesi, bu özniteliğin sistem tam bir eşleşme aradığında göz önüne alınacağı anlamına gelir.  

## <a name="add-subcomponents"></a>Alt bileşenler ekleme
1. Alt bileşenler bölümünü genişletin.
2. Ekle öğesini tıklatın.
3. Listede, seçili satırı işaretleyin.
4. İsim alanına bir değer yazın.
5. Çözücü adı alanında bir değer girin.
6. Açıklama alanına bir değer girin.
7. Bileşen alanında bir değer girin veya seçin.
    * Her alt bileşen bir bileşen tanımına başvurmalıdır. Bu tasarım, yeniden kullanılabilir bileşenleri destekler ve bir bileşenin bir kere tanımlandıktan sonra birçok ürün modelinde kullanılabilmesini sağlar.  
8. Kaydet'e tıklayın.
9. Ürün reçetesi satır ayrıntılarını tıklatın.
    * Ürün reçetesi satırı ayrıntıları, kullanıcının alt bileşen için gerekli özellikleri seçmesini sağlar. Her özellik sabit bir değer verebilir veya bir özniteliğine eşlenebilir. Bir özniteliği eşleştirme, ürün reçetesi satır özelliğinin yapılandırma seçimine bağlı olarak farklı değerler almasına neden olur.  
10. Madde numarası alanında bir değer girin veya seçin.
    * Her alt bileşen, kısıtlama tabanlı yapılandırma teknolojisine sahip yapılandırılabilir bir ana ürünü temsil eder. Referans, ürün numarası üzerinden verilir.  
11. Ayarla onay kutusunu işaretleyin.
12. Hesaplama alanında Evet'i seçin.
    * Hesaplama seçeneğinin ayarlanması, ürünün maliyet hesaplaması çalıştırıldığında ürünün dahil edilmesini sağlar.  
13. Kurulum sekmesine tıklayın.
14. Ayarla onay kutusunu işaretleyin.
15. Miktar alanına bir sayı girin.
    * Miktar alanı, bu ürünün ne kadarının yapılandırılan üründe tüketileceğini belirler.  
16. Ayarla onay kutusunu işaretleyin.
17. Seri başına alanında bir sayı girin.
18. Tamam'a tıklayın.

