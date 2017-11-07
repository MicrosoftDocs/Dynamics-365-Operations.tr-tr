---
title: "Stok durumları"
description: "Bu makalede, stoğu kategorilendirmek ve izlemek için stok durumlarını nasıl kullanabileceğiniz açıklanmaktadır."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 70b084ac2eb8ffbd8832df2e562e8862e4ac8e57
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="inventory-statuses"></a>Stok durumları

[!include[banner](../includes/banner.md)]


Bu makalede, stoğu kategorilendirmek ve izlemek için stok durumlarını nasıl kullanabileceğiniz açıklanmaktadır.

Stok durumlarını stoku kategorilere ayırmak için kullanabilirsiniz. Arından stok yenileme veya yerine koyma gibi uygun eylemleri başlatabilirsiniz.

Burada stok durumlarını kullanabileceğiniz bazı yollara ilişkin örnekler verilmiştir:

-   Eldeki stok, gelen hareketler ve giden hareketler için stok durumları oluşturun.
-   Ambar hareketleri için varsayılan bir stok durumu belirleyin.
-   Teslim almadan, teslim alırken veya maddeler stok hareketi sırasında yerine konulurken maddelerin stok durumunu değiştirin.
-   İade edilen maddeleri fiyatlandırmak ve master planlama sırasında madde karşılama planlamak için stok durumunu kullanın.

Stok durumu, depolama boyutu grubundaki boyutlardan biridir. Stok durumları, kullanılabilir veya kullanılamaz diye kategorilere ayrılabilir ve kullanılmayan bir stok durumuna sahip olan maddeleri engellemek için **Stok engelleme** parametresini kullanabilirsiniz. Engellenen bir duruma sahip olan maddeler fiziksel stok olarak kabul edilir ve bir üretim emri, satış emri, transfer emir veya giden hareket üzerinde kullanılamaz.

Gelen iş için kullanılabilir veya kullanılamaz stok durumuna sahip ambar maddelerini kullanabilirsiniz. Örneğin, **Hazır** adında bir kullanılabilir durum, **Hasarlı** adında bir kullanılamayan durum ve **Engelli** adında bir engellenen durum oluşturuyorsunuz. Alınan veya iade edilen madeler için bir satın alma emri oluşturduğunuzda maddeler hasarlı veya arızalı ise bu maddelerin stok durumunu satın alma emri satırında **Hasarlı** olarak değiştirebilirsiniz. Bu maddeler teslim alındıktan sonra durum otomatik olarak **Engelli** olarak ayarlanır. Hasarlı maddeleri bir taşınabilir aygıt kullanarak tarıyorsanız Microsoft Dynamics 365 for Finance and Operations bu maddeleri yerine koyabileceğiniz uygun bir konum veya konumlar hakkında bilgi göstermek üzere konum direktiflerini ve iş şablonlarını kullanabilir. İade edilen maddeler için **Stok hareketleri** sayfasında **Rezervasyon** türü bir sorun oluşturulur.

Giden iş için kullanılabilen stok durumuna sahip maddeleri kullanın. **Arızalı** durumunda olan maddeler varsa ve master planlama bu maddeler üzerinde çalıştırılıyorsa maddelerin eksik olduğu kabul edilir ve stok otomatik olarak yenilenir.

Stok durumlarını oluşturduktan sonra bir saha, madde ve ambar için varsayılan stok durumunu ayarlayabilirsiniz. Ayrıca satışlar, transferler ve satın alma emirleri için de varsayılan bir durum ayarlayabilirsiniz. Satış emirleri ve giden transferler için varsayılan durumun **Stok engelleme** seçeneğini **Evet** olarak ayarlanamaz. Bir saha, ambar, madde, satın alma emri, transfer emri veya satış emri ile ilgili varsayılan ayarlardan gelen stok durumu taşınabilir aygıt kullanarak veya satın alma emir, satış emri veya transfer emri satırında değiştirilebilir.

Bir kullanılabilen stok durumuna sahip maddelerin karşılanmasını planlamak için **Depolama boyutu grupları** sayfasında bir depolama boyutu için **Boyuta göre karşılama planı** seçimini yapın. **Madde Karşılama** sihirbazını açtığınızda, bir kullanılabilir duruma sahip olan maddeler **Durum** sayfasında görüntülenmez. Bu maddeler için karşılama ayarları oluşturmak için kullanılabilen stok durumları için stok durumu kimliğini seçin. Karşılama ayarlarına bağlı olarak, madde gereksinimlerini hesaplayabilir ve master planlama sırasında kullanılabilir maddelerin arz ve taleplerini tahmin edebilirsiniz. Bir engelli stok durumuna sahip bir madde karşılama kurulumu oluşturamazsınız. Alternatif olarak, madde karşılama parametreleri oluşturmak veya bunları değiştirmek için **Madde karşılama** sayfasını kullanın.

