---
title: Ürün yapılandırma modeli oluşturma
description: Bu yordam, bir ürün yapılandırma modelinin nasıl oluşturulacağını ve öznitelikler ve alt bileşenler gibi temel bilgilerin nasıl girileceğini gösterir.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca99c0346a3f982164076167c3429587aac18be6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568436"
---
# <a name="create-a-product-configuration-model"></a>Ürün yapılandırma modeli oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, bir ürün yapılandırma modelinin nasıl oluşturulacağını ve öznitelikler ve alt bileşenler gibi temel bilgilerin nasıl girileceğini gösterir. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-a-product-model"></a>Ürün modeli oluşturma

1. **Ürün bilgileri yönetimi \> Ürünler \> Ürün yapılandırma modelleri**'ne gidin.
1. **Yeni**'yi seçin.
1. **Ad** alanına bir değer yazın.
1. **Tanım** alanına bir değer girin.
1. **Çözüm stratejisi** alanında bir seçenek belirleyin.
    * Çözüm stratejisi, kısıtlama tabanlı bir ürün yapılandırması modelindeki kısıtlamaların nasıl işleme koyulacağını belirler. Bu seçimin ürün yapılandırma modelinin performansı üzerinde etkisi olabilir.  
1. **Ad** alanına bir değer yazın.
    * Kök bileşen, ürün yapılandırması modelini temsil eder ve diğer ürün modellerinde de kullanılabilir.  
1. **Tamam**'ı seçin.
1. **Yeniden kullanma yapılandırması** alanında bir seçenek belirleyin.
    * Yapılandırmaları yeniden kullanma parametresi Evet olarak ayarlanırsa, sistem her bir yapılandırma oturumunun ardından eşdeğer yapılandırmaları denetler ve tam bir eşleşme bulunursa onları yeniden kullanır.  

## <a name="add-attributes"></a>Öznitelikler ekle

1. **Öznitelikler** bölümünü genişletin.
2. **Ekle**'yi seçin.
3. Listede, seçili satırı işaretleyin.
4. **Ad** alanına bir değer yazın.
5. **Çözücü adı** alanında bir değer girin.
    * Çözücü adı, ürün yapılandırıcının çözücüsü tarafından kullanılır. Boşluk veya _ (alt çizgi) dışında özel karakterler içermemelidir.  
6. **Tanım** alanına bir değer girin.
    * Açıklama metni yapılandırma kullanıcısı tarafından görülür ve dolayısıyla doğru öznitelik değerinin seçilmesine yardımcı olabilir.  
7. **Öznitelik türü** alanında bir değer girin veya seçin.
    * Öznitelik türü, hangi değerlerin öznitelik için kullanılabilir olduğunu belirler.  
8. **Yeniden kullanıma dahil et** onay kutusunu işaretleyin.
    * Bu seçenek yalnızca Yapılandırmaları yeniden kullanma seçeneği belirlendiğinde kullanılabilir. Yeniden kullan onay kutusunda öznitelik eklenmesi, bu özniteliğin sistem tam bir eşleşme aradığında göz önüne alınacağı anlamına gelir.  

## <a name="add-subcomponents"></a>Alt bileşenler ekleme

1. **Alt bileşenler** bölümünü genişletin.
2. **Ekle**'yi seçin.
3. Listede, seçili satırı işaretleyin.
4. **Ad** alanına bir değer yazın.
5. **Çözücü adı** alanında bir değer girin.
6. **Tanım** alanına bir değer girin.
7. **Bileşen** alanında bir değer girin veya seçin.
    * Her alt bileşen bir bileşen tanımına başvurmalıdır. Bu tasarım, yeniden kullanılabilir bileşenleri destekler ve bir bileşenin bir kere tanımlandıktan sonra birçok ürün modelinde kullanılabilmesini sağlar.  
8. **Kaydet**'i seçin.
9. **Ürün reçetesi satırı ayrıntıları**'nı seçin.
    * Ürün reçetesi satırı ayrıntıları, kullanıcının alt bileşen için gerekli özellikleri seçmesini sağlar. Her özellik sabit bir değer verebilir veya bir özniteliğine eşlenebilir. Bir özniteliği eşleştirme, ürün reçetesi satır özelliğinin yapılandırma seçimine bağlı olarak farklı değerler almasına neden olur.  
10. **Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.
    * Her alt bileşen, kısıtlama tabanlı yapılandırma teknolojisine sahip yapılandırılabilir bir ana ürünü temsil eder. Referans, ürün numarası üzerinden verilir.  
11. **Ayarla** onay kutusunu işaretleyin.
12. **Hesaplama** alanında **Evet**'i seçin.
    * Hesaplama seçeneğinin ayarlanması, ürünün maliyet hesaplaması çalıştırıldığında ürünün dahil edilmesini sağlar.  
13. **Kurulum** sekmesini seçin.
14. **Ayarla** onay kutusunu işaretleyin.
15. **Miktar** alanına bir sayı girin.
    * Miktar alanı, bu ürünün ne kadarının yapılandırılan üründe tüketileceğini belirler.  
16. **Ayarla** onay kutusunu işaretleyin.
17. **Seri başına** alanında bir sayı girin.
18. **Tamam**'ı seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]