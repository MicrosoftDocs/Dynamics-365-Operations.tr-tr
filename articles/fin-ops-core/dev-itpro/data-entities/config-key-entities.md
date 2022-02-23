---
title: Yapılandırma anahtarları ve veri varlıkları
description: Bu konu, yapılandırma anahtarları ve veri varlıkları arasındaki ilişkiyi açıklar.
author: Sunil-Garg
manager: AnnBe
ms.date: 05/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: e6145a2f6925932361851735df55374dda8ca03d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679393"
---
# <a name="configuration-keys-and-data-entities"></a>Yapılandırma anahtarları ve veri varlıkları

[!include [banner](../includes/banner.md)]

Verileri içe veya dışa aktarmak için veri varlıklarını kullanmadan önce öncelikle yapılandırma anahtarlarının kullanmayı planladığınız veri varlıkları üzerindeki etkisini belirlemenizi öneririz.

Yapılandırma anahtarları hakkında daha fazla bilgi için bkz. [Lisans kodları ve yapılandırma anahtarları raporu](../sysadmin/license-codes-configuration-keys-report.md).

### <a name="configuration-key-assignments"></a>Yapılandırma anahtarı atamaları
Yapılandırma anahtarları aşağıdaki yapılardan birine veya tümüne atanabilir.

- Veri varlıkları
- Veri kaynağı olarak kullanılan tablolar
- Tablo alanları
- Veri varlığı alanları

Aşağıdaki tablo, bir nesnenin temelini oluşturan farklı yapılardaki yapılandırma anahtarı değerlerinin nesnenin beklenen davranışını nasıl değiştirdiğini özetler.

| Veri varlığındaki yapılandırma anahtarı ayarı | Tablodaki yapılandırma anahtarı ayarı | Tablo alanındaki yapılandırma anahtarı ayarı | Veri varlığı alanındaki yapılandırma anahtarı | Beklenen davranış |
|-----------------------------------------|------------------------------------|------------------------------------------|----------------------------------------|------------------|
| Devre dışı                                | Değerlendirilmedi                      | Değerlendirilmedi                            | Değerlendirilmedi                          | Veri varlığının yapılandırma anahtarı devre dışı bırakılırsa, veri varlığı işlevlerini yerine getiremez. Temel alınan tablolardaki ve alanlardaki yapılandırma anahtarlarının etkin veya devre dışı olup olmadığı önemli değildir. |
| Etkin                                 | Devre dışı                           | Değerlendirilmedi                            | Değerlendirilmedi                          | Bir veri varlığı için yapılandırma anahtarı etkinleştirilmişse, veri yönetim çerçevesi temeldeki tabloların her birindeki yapılandırma anahtarını denetler. Bir tablo için yapılandırma anahtarı devre dışı bırakılırsa, bu tablo işlevsel kullanım için veri varlığında bulunmayacaktır. Bir tablonun yapılandırma anahtarı devre dışı bırakılırsa, tablo ve veri varlığı yapılandırma anahtarı ayarları değerlendirilmez. Varlıktaki birincil tablonun yapılandırma anahtarı devre dışı bırakılırsa sistem, varlığın yapılandırma anahtarı devre dışı bırakılmış gibi davranır. |
| Etkinleştirildi                                 | Etkinleştirildi                            | Devre dışı                                 | Değerlendirilmedi                          | Bir veri varlığı için yapılandırma anahtarı etkinleştirilirse ve temeldeki tabloların yapılandırma anahtarları etkinleştirilirse, veri yönetimi alt yapısı tablolardaki alanın yapılandırma anahtarını denetler. Bir alan için yapılandırma anahtarı devre dışı bırakılırsa, ilgili veri varlığı alanının yapılandırma anahtarı etkinleştirilmiş olsa bile bu alan işlevsel kullanım için veri varlığında kullanılmaz. |
| Etkin                                 | Etkin                            | Etkin                                  | Devre dışı                               | Yapılandırma anahtarı diğer tüm düzeylerde etkinleştirilmişse ancak varlık alanı yapılandırma anahtarı etkin değilse, alan veri varlığında kullanılmak üzere kullanılamaz. |

> [!NOTE]
> Bir varlık veri kaynağı olarak başka bir varlığa sahipse, yukarıdaki semantikler tekrarlı şekilde uygulanır.

### <a name="entity-list-refresh"></a>Varlık listesini yenileme
Varlık listesi yenilendiğinde, veri yönetimi alt yapısı çalışma zamanında kullanım için yapılandırma anahtarı meta verisini oluşturur. Bu meta veri yukarıda açıklanan mantık kullanılarak oluşturulur. Veri yönetimi çerçevesindeki işleri ve varlıkları kullanmadan önce varlık listesi yenileme işleminin tamamlanmasını beklemenizi önemle öneririz. Beklememeniz durumunda, yapılandırm anahtarı meta verisi güncel olmayabilir ve bu da beklenmeyen sonuçlara yol açabilir. Varlık listesi yenilenirken, varlık listesi sayfasında aşağıdaki ileti gösterilir.

![Varlık listesi yenileme](./media/Entity_refresh_list.png)

### <a name="data-entity-list-page"></a>Veri varlığı listesi sayfası
Veri yönetimi çalışma sayfasındaki veri varlığı liste sayfası varlıklara ilişkin yapılandırma anahtarı ayarlarını gösterir. Yapılandırma anahtarlarının veri varlığı üzerindeki etkisini anlamak için bu sayfadan başlayın.

Bu bilgi, varlık yenileme sırasında oluşturulan meta veri kullanılarak gösterilir. Yapılandırm anahtarı sütunu, veri varlığıyla ilişkili olan yapılandırm anahtarının adını gösterir. Bu sütun boş olması veri varlığıyla ilişkilendirilmiş yapılandırma anahtarı olmadığını gösterir. Yapılandırma anahtarı durum sütunu yapılandırma anahtarının durumunu gösterir. Onay işareti varsa, bu anahtarın etkin olduğu anlamına gelir. Boş ise, bu anahtarın devre dışı olduğu ya da ilişkili anahtar bulunmadığı anlamına gelir.

![Varlık listesi sayfası](./media/Data_entity_list_page.png)

### <a name="target-fields"></a>Hedef alanları
Sonraki adım, yapılandırma anahtarlarının tablolar ve alanlar üzerindeki etkisini görmek üzere veri varlığını ayrıntılı incelemek olacaktır. Bir veri varlığındaki hedef alanlar yapılandırma anahtarını ve veri varlığındaki ilişkili tablolar ve alanlarla ilgili anahtar durumu bilgilerini gösterir. Veri varlığının kendi yapılandırma anahtarı devre dışı bırakılmışsa, bu varlık için hedef alanlar formundaki tabloların ve alanları yapılandırma anahtarının durumu ne olursa olsun tamamen kullanılamaz olacağını bildiren bir uyarı iletisi görüntülenir.

![Hedef alanları](./media/Target_fields_1.png)

### <a name="child-entities"></a>Alt varlıklar 
Bazı varlıklar veri kaynağı olarak başka varlıklara sahiptir veya bileşik veri varlıklarıdır: bu varlıklar için yapılandırma anahtarı bilgisi Alt varlıklar formunda gösterilir. Bu formu, yukarıda açıklanan varlıklar liste sayfasına benzer şekilde kullanın. Alt varlık için hedef alanlar formu da yukarıda açıklandığı şekilde davranır.

![Hedef alanları](./media/Target_fields_2.png)

### <a name="using-data-entities"></a>Veri varlıklarını kullanma
Yapılandırma anahtarlarının kullanmak istediğiniz veri varlıkları üzerindeki tam etkisini (varsa) anladıktan sonra, veri varlıklarını veri projelerine ekleyerek kullanma aşamasına geçebilirsiniz. 

### <a name="run-time-validations-for-configuration-keys"></a>Yapılandırma anahtarları için çalışma zamanı doğrulamaları
Çalışma zamanı doğrulamaları, varlık yenileme listesi sırasında oluşturulan yapılandırma anahtarı meta verisini kullanarak aşağıdaki kullanım örneklerinde gerçekleştirilir.

- Bir işe bir veri varlığı eklendiğinde
- Kullanıcı varlık listesinde 'doğrula'ya tıkladığında
- Kullanıcı veri projesine bir veri paketi yüklediğinde
- Kullanıcı veri projesine bir şablon yüklediğinde
- Mevcut bir veri projesi yüklendiğinde
- Veri projesine bir şablon yüklendiğinde
- Dışa aktarma/içe aktarma işi yürütülmeden önce (toplu iş, toplu iş olmayan, tekrarlayan, OData)
- Kullanıcı eşleme oluşturduğunda
- Kullanıcı eşleme kullanıcı arabiriminde alanları eşlediğinde
- Kullanıcı yalnızca 'içe aktarılabilir alanlar' eklediğinde

### <a name="managing-configuration-key-changes"></a>Yapılandırma anahtarı değişikliklerini yönetme
Yapılandırma anahtarlarını varlık, tablo veya alan düzeyinde her güncelleştirdiğinizde, varlık yönetimi altyapısındaki varlık listesinin yenilenmesi gerekir. Bu işlem altyapının en son yapılandırma anahtarı ayarlarını almasını sağlar. Varlık listesi yenilenene kadar aşağıdaki ileti varlık listesi sayfasında gösterilir. Güncelleştirilen yapılandırma anahtarı değişiklikleri varlık listesi yenilendikten hemen sonra etkinleşir. Yapılandırma anahtarı değişikleri etkin olduktan sonra beklenen şekilde çalıştığından emin olmak üzere mevcut veri projelerini ve işlerini değerlendirmenizi öneririz.

![Hedef alanları](./media/Target_fields_3.png)
