---
title: "Dynamics AX uygulama sürümü 7.0.1&quot;deki yenilikler ve değişiklikler (Mayıs 2016)"
description: "Bu makale, Microsoft Dynamics AX uygulamasının sürüm 7.0.1&quot;inde yeni olan veya değişen özellikleri açıklar. Bu sürüm Mayıs 2016 tarihinde yayımlanmıştır ve 7.0.1265.23014 yapım numarasına sahiptir."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8b58cb4f9de393b3f381dbe0aa4330d5ebd62795
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Dynamics AX uygulama sürümü 7.0.1'deki yenilikler ve değişiklikler (Mayıs 2016)

[!include[banner](../includes/banner.md)]


Bu makale, Microsoft Dynamics AX uygulamasının sürüm 7.0.1'inde yeni olan veya değişen özellikleri açıklar. Bu sürüm Mayıs 2016 tarihinde yayımlanmıştır ve 7.0.1265.23014 yapım numarasına sahiptir.

<a name="electronic-reporting-er"></a>Elektronik raporlama (ER)
-------------------------

|                                                                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ne yapabilirsiniz?**                                                                                                                                                                   | **Bu neden önemlidir?**                                                                                                                                                                                                                                                                                                                             |
| Kullanıcıların istedikleri finansal boyutları seçebilmeleri için Elektronik raporlama (ER) raporları tasarlarken bir çalışma zamanı iletişim kutusu yapılandırın.                                     | Çalışma zamanında, ER raporunu çalıştırma iletişim kutusunda kullanıcılar birden çok finansal boyut seçebilir. Seçili finansal boyutların ayrıntıları oluşturulan elektronik belgede görüntülenir.                                                                                                                              |
| ER raporunun tasarımı sırasında istenen veri kaynağına tek bir eşleme aracılığıyla birden çok finansal boyuta erişimi yapılandırın.                                                  | Aynı ER raporu yapılandırması kullanıcı tarafından seçilen veya geçerli tüzel kişiliği veya kurulumu için yapılandırılan mali boyutların sayısından bağımsız olarak, mali boyutların ayrıntılarıyla birlikte hareket verileri sunan elektronik belgeler oluşturmak için kullanılabilir.                                             |
| ER raporunu OPENXML çalışma sayfası biçiminde oluşturulan bir elektronik belgenin dinamik olarak oluşturulan sütunlarına veri girmek üzere yapılandırın.                                           | ER raporu oluşturulan bir OPENXML çalışma sayfasına yatay olarak yinelenen sütunlar aracılığıyla veri girebilir. Bu nedenle aynı ER raporu yapılandırması dinamik olarak oluşturulan sütun sayısı farklı olan elektronik belgeler oluşturmak için yeniden kullanılabilir.                                                                                 |
| ER hedeflerini Bir biçimin çıkış sonucunun dosya, e-posta veya arşiv (Microsoft SharePoint klasörü veya Microsoft Azure Depolama) gibi belirli bir hedefe yönlendirileceği şekilde yapılandırın. | Önceden bir ER yapılandırması çalıştırdığınızda dosyayı kaydetmek veya açmak için kullanıcı eylemi gerektiren bir ileti kutusu görüntüleniyordu. Artık her bir biçim yapılandırması ve her bir çıkış bileşeni (bir klasör veya bir dosya) için ayrı bir hedefi önceden yapılandırabilirsiniz. Uygun erişim haklarına sahip kullanıcılar çalışma zamanında hedef ayarlarını da değiştirebilir. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>POS - Microsoft Dynamics AX Perakende
|                                |                                                                                                                                                                                         |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ne yapabilirsiniz?**           | **Bu neden önemlidir?**                                                                                                                                                              |
| Google Chrome tarayıcısını kullanın. | Perakendeciler artık Chrome tarayıcısından Bulut POS uygulamasını başlatabilir ve Bulut POS'un Microsoft Edge ve Internet Explorer sürümlerinde bulunan tüm işlevleri kullanabilir. |

## <a name="financial-reporting"></a>Mali raporlama
|                                                                     |                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ne yapabilirsiniz?**                                                | **Bu neden önemlidir?**                                                                                                                                                                                                                                                                                         |
| Finansal raporlama veri reyonunu yeniden oluşturun.                          | Dynamics AX veritabanları ortamlar arasında taşıdığınızda veya ortama başka aykırı değişiklikler yaptığınızda Finansal raporlama veritabanının yeniden oluşturulması gerekebilir. Veritabanını sizin için yeniden oluşturmak amacıyla bir Windows PowerShell komut dosyası sağlandı.                                                                |
| Artık geçerli olmayan rapor tasarımcısı seçeneklerini belirleyemezsiniz. | Yönetim raporlayıcısının pazar içi sürümlerinde kullanılan pek çok rapor tasarımcısı seçeneği Dynamics AX'in bu sürümünde geçerli değildir. Bu seçenekler, finansal rapor tasarımıyla, çıktıyla ve bağlama ile ilgiliydi. Bu seçenekler, kullanıcı hataları önlemek için mali rapor tasarımcısından kaldırılmıştır. |

## <a name="financial-management"></a>Mali yönetim
|                                                            |                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------|
| **Ne yapabilirsiniz?**                                       | **Bu neden önemlidir?**                                       |
| Borç hesapları ödemeleri için pozitif ödeme dosyaları oluşturun. | Pozitif ödeme dosyaları çek sahteciliğini önlemeye yardımcı olmak için oluşturulabilir. |

## <a name="warehouse-and-production"></a>Ambar ve üretim
|                                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ne yapabilirsiniz?**                                                                                                                                                                                                                                                                                                                                                                    | **Bu neden önemlidir?**                                                                                                                                                                                                                                                                                                                                                                                                              |
| Belirli yerleşimlerde ürün kümeleri için iş oluşturma işlemini denetleyen bir ambar çalışma ilkesi tanımlayın.                                                                                                                                                                                                                                                                          | Ambar işlemler, her zaman iş içermez. Yeni ambar çalışma ilkesini kullanarak, hammadde çekme ve tamamlanmış malların yerine koyması işlerinin oluşturulmasını, çeşitli bir ürün dizisi veya belirtilen konumlar için engelleyebilirsiniz.                                                                                                                                                                                                     |
| Ürün çıkış konumunun plaka denetimli olmadığını belirtin.                                                                                                                                                                                                                                                                                                               | Artık bir ürün çıkış konumunun plaka denetimli olmadığını belirtebilirsiniz. Örneğin, bu özellik yukarı doğru bir üretim emri maddeleri aşağı doğru bir ürün emri için ürün giriş konumu görevi gören bir konuma doğrudan tamamlandı olarak bildirdiğinde yararlıdır.                                                                                                                                                     |
| Aynı maddenin farklı üretim boyutlarına sahip maddeleri içeren ürün reçetelerini destekleyin.                                                                                                                                                                                                                                                                                                     | Üretimde bir veya daha fazla üretim boyutu kullanırken, maddeyi aynı maddenin farklı seçeneklerine göre üretmek istediğiniz durumlar olabilir. Daha fazla bilgi için bkz. [bu blog](https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/).                                                                  |
| Ürün reçetelerinin birinci düzeyinde döngüsel yapıya sahip üretim emirleri malzeme kaynak planlamasında ürün reçetesi düzeyi hesaplamanın dışında bırakılır.                                                                                                                                                                                                                                     | Ürün reçetesi hiyerarşisinde döngüselliğe neden olan üretim emirlerinde seçenek üretmek için doğru ürün reçetesi düzeyleri atamak mümkün değildir.                                                                                                                                                                                                                                                                                                  |
| Malzeme kaynağı planlama ve maliyet hesaplaması için ayrı ürün reçetesi düzeylerini hesaplayın: • Malzeme kaynak planlaması için ürün reçetesi düzeyleri yeni **ReqItemLevel** tablosunda hesaplanır. Biten üretim emirleri hesaplamada dikkate alınmaz. • Üretim maliyeti hesaplamasında, ürün reçetesi düzeyleri **InventTable** üzerinde hesaplanır. Biten üretim emirleri hesaplamaya dahil edilir. | • Malzeme kaynak planlaması çalıştırırken, örneğin master planlama plan planlama ve açılım, yalnızca malzeme kaynak planlamasında kullanılan ürün reçetesi düzeylerinin hesaplanması gerekir. Diğer bir deyişle, üretim maliyeti hesaplamasında kullanılan ürün reçetesi düzeylerini hesaplamaya gerek yoktur. • Maliyet işlemleri çalıştırırken, örneğin stok kapatma, yalnızca üretim maliyeti hesaplamasında kullanılan ürün reçetesi düzeylerinin yeniden hesaplanması gerekir. |

 

<a name="see-also"></a>Ayrıca bkz.
--------

[Yeni veya değişenler nedir](whats-new-changed.md)

[Yeni veya güncelleştirilmiş kılavuzlar (Mayıs 2016)](new-updated-task-guides-available-may-2016.md)




