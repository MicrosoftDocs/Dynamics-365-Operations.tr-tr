---
title: Stok durdurma
description: Bu makalede, Microsoft Dynamics 365 for Finance and Operations'ın kalite denetim sürecinin parçası olan stok engellemeye genel bakış sunulmuştur. Stok engellemeyi kullanarak maddelerin işlenmesini veya tüketilmesini engelleyebilirsiniz.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb6291e2f012f148b247b747f84155b96cf09677
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "352057"
---
# <a name="inventory-blocking"></a>Stok durdurma

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 for Finance and Operations'ın kalite denetim sürecinin parçası olan stok engellemeye genel bakış sunulmuştur. Stok engellemeyi kullanarak maddelerin işlenmesini veya tüketilmesini engelleyebilirsiniz.

Stok maddelerini aşağıdaki şekillerde durdurabilirsiniz:
-   El ile
-   Kalite emri oluşturma
-   Kalite emri oluşturan bir işlemi kullanma
-   Stok durumu durdurmayı kullanma

## <a name="blocking-items-manually"></a>Maddeleri el ile durdurma
**Stok durdurma** sayfasında bir hareket oluşturarak bir miktar maddeyi durdurabilirsiniz. Yalnızca eldeki stok olarak mevcut olan maddeler el ile durdurulabilir. El ile engellenen miktarlar için, planlama etkinliklerinin beklenen girişlerin beklenen eldeki miktar olarak eklenip eklenmeyeceğine karar vermeniz gerekir. Beklenen girişler, inceleme tamamlandıktan sonra eldeki stok olarak kullanılabilir olması beklenen durdurulmuş maddelerdir. Beklenen tarihi koruyabilirsiniz. Varsayılan olarak, **Beklenen girişler** seçeneği, bir kalite emri aracılığıyla durdurulan maddeler için seçilir. **Stok durdurma** sayfasındaki hareketi silerek miktara uygulanan el ile durdurmayı iptal edebilirsiniz.

## <a name="blocking-items-by-creating-a-quality-order"></a>Bir kalite emri oluşturarak maddeleri durdurma
**Kalite emirleri** sayfasında bir kalite meri oluşturarak incelenmesi gereken maddeleri belirtebilirsiniz. Bir kalite emri oluşturduğunuzda, bir madde için belirttiğiniz miktar durdurulur. Bir kalite emriyle ilişkili olan örnekleme planı yalnızca incelenmesi gereken maddelerin miktarını denetler; durdurulan miktar kontrol edilmez. Kalite emrine girilen, miktar durdurulan miktardır; örnekleme planında belirtilene bakılmaksızın inceleme için gönderilmesi gerekir.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Kalite meri oluşturan bir işlem kullanarak maddeleri durdurma
Kalite işlemi bir maddenin incelenmesi gerektiğini belirtirse, bir miktar madde otomatik olarak durdurulur. Bu nedenle, bir kalite emri otomatik olarak oluşturulduğunda, kalite emriyle ilişkili olan madde örnekleme planı hem durdurulan madde miktarını hem de incelenmesi gereken miktarı denetler. **Madde örnekleme** sayfasında **Tam durdurma** seçilirse, örneğin bir satınalma siparişi satırındaki tüm miktar, madde örnekleme adedine bakılmaksızın inceleme sırasında durdurulur.
### <a name="example"></a>Örnek

Aşağıdaki örnekte, bir satınalma siparişi sevk irsaliyesi deftere nakledildiğinde bir kalite emri oluşturulur. **Kalite ilişkilendirmeleri** sayfasında, satınalma siparişi sevk irsaliyesi naklinin kalite emrini etkinleştiren işlem olduğunu belirtirsiniz.

|Ayar                                                                     |Kullanıcı eylemi                 |Sonuç             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| Kalite ilişkilendirme, kalite emrinin satınalma siparişi sevk irsaliyesi deftere nakledildiğinde oluşturulması gerektiğini belirtir. Kalite emrinin madde örnekleme ayarı, satınalam siparişi satırındaki miktarın yüzde 10'unun incelenmesi gerektiğini belirtir. Ayrıca, madde örnekleme ayarında **Tam durdurma** seçili olduğundan, satınalma sipariş satırındaki tüm miktarın, incelenmeye gönderilen miktara bakılmaksızın, inceleme sırasında durdurulması gerekir. | Sevk irsaliyesi deftere nakledilir. | Kalite emri oluşturulur. Satınalma siparişi miktarının yüzde onu incelemeye gönderilir.  Satınalma sipariş satırındaki tüm miktar durdurulur. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Stok durumu durdurmayı kullanarak maddeleri durdurma
**Stok durumları** sayfasındaki **Stok durdurma** parametresini kullanarak hangi stok durumlarının durdurulacağını belirtebilirsiniz. Üretim emirleri, satış siparişleri, transfer emirleri, giden hareketler veya proje tümleştirmeleri için stok durumlarını durdurma durumları olarak kullanamazsınız. Giden iş için kullanılabilen stok durumuna sahip maddeleri kullanın. Maddelerin durumu **Arızalı** olduğunda ve bu maddeler üzerinde master planlama çalıştırıldığında, maddeler eksik olarak kabul edilir ve stok otomatik olarak yenilenir.



<a name="additional-resources"></a>Ek kaynaklar
--------

[Stok durdurma oluştur ve sürdür](tasks/create-maintain-inventory-blocking.md)

[Kalite yönetimi işlemleri](quality-management-processes.md)

[Malların kalitesini denetleme (Görev kılavuzu)](tasks/inspect-quality-goods.md)
