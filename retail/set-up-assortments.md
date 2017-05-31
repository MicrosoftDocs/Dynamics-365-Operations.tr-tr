---
title: "Ürün sınıflarını ayarlama"
description: "Bu makalede, bir ürün çeşidinin ne olduğu ve Microsoft Dynamics 365 for Operations - Perakende&quot;de ürün çeşitlerinin nasıl ayarlandığı açıklanmaktadır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ffa60ad4890a783c05bbde09aa00189fb30bd706
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-assortments"></a>Ürün sınıflarını ayarlama

[!include[banner](includes/banner.md)]


Bu makalede, bir ürün çeşidinin ne olduğu ve Microsoft Dynamics 365 for Operations - Perakende'de ürün çeşitlerinin nasıl ayarlandığı açıklanmaktadır.

Ürün çeşidi, fiziksel mağaza veya çevrimiçi mağaza gibi bir perakende kanalına atadığınız bir ilgili ürünler topluluğudur. Ürün sınıflarını, her mağaza tarafından kullanılabilecek ürünleri tanımlamak üzere kullanabilirsiniz. Bir ürün sınıfı, ürün kategorileri içerebilir. Bu nedenle, belirli bir kategoriye atanan tüm ürünler ürün sınıfına dahil edilir. Bir ürün sınıfı belirli ürünleri ve belirli ürün varyantlarını da içerebilir. Bir ürün sınıfı ayarlayarak, perakende kanallarınıza, mağazaların ihtiyacı olan herhangi bir kombinasyonda, aynı anda binlerce ürün atayabilirsiniz. İhtiyaç duyduğunuz kadar ürün sınıfı ayarlayabilirsiniz. Her ürün bir veya daha fazla ürün sınıfına dahil edilebilir ve her ürün sınıfı bir veya daha fazla perakende kanalına atanabilir. Örneğin, temel ürün kümesi içeren bir ürün sınıfı belirleyebilirsiniz. Tüm mağazalar bu ürün sınıfını alır. Ardından, yalnızca geniş spor ekipmanlarını içeren başka bir ürün sınıfı tanımlayabilirsiniz. Bu ürün sınıfını yalnızca büyük mağazalarınız alır. Aşağıdaki şekilde ürünlerin ürün sınıflarına ve bu ürün sınıflarının perakende kanallarına nasıl atanacağı gösterilmektedir. ![Ürün sınıfı ilişkileri](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Önkoşullar
Bir ürün sınıfı ayarlamadan ve bunu bir perakende kanalına atamadan önce aşağıdaki görevleri tamamlamanız gerekir.

| Görev                              | Açıklama                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bir perakende kanalı ayarlayın.          | Perakende kanalları fiziksel mağazayı, çevrimiçi mağazayı veya bir çevrimiçi marketi temsil eder. En az bir perakende kanalı ayarlamanız ve mağaza için seçenekleri yapılandırmanız gerekir. Ürün sınıfları, belirli bir mağazanın alacağı ürünleri tanımlamak amacıyla mağazalara atanır.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Organizasyon hiyerarşisi oluşturun. | Kuruluşunuz için perakende kanallarını ayarladıktan sonra, perakende kanallarınızın organizasyon yapısını temsil eden bir perakende organizasyon hiyerarşisi yapılandırmanız gerekir. Organizasyon hiyerarşisi ürün sınıfları, stok yenileme ve raporlama için kullanılabilir. Perakende kanallarınızı bir organizasyon hiyerarşisine ekleyerek ürün sınıflarını mağaza gruplarına atayabilirsiniz. Ürün sınıfını her mağazaya ayrı ayrı atamak yerine, ürün sınıfını yüksek düzey organizasyon düğümüne atayın. Ardından, yüksek düzey organizasyon düğümüne yeni bir perakende kanalı eklendiğinde, bu perakende kanalı üst dzey organizasyon düğümüne atanmış olan ürün sınıflarını otomatik olarak devralır. Ürün sınıflarını yalnızca **Perakende ürün sınıfı** amacıyla atanmış olan bir organizasyon hiyerarşisine dahil edilen perakende kanallarına atayabilirsiniz. |
| Ürünleri tanımlayın.                  | Ürünleri ürün sınıfına ekleyebilmek için ürünleri önce Microsoft Dynamics AX'e eklemeniz gerekir. Ürünleri el ile ekleyebilir veya bir satıcıdan içer aktarabilirsiniz. Ürünleri ekledikten sonra, bunları bir tüzel kişilik için serbest bırakmanız gerekir. Yalnızca bir tüzel kişilik için serbest bırakılan ürünler perakende kanallarınız tarafından kullanılabilir. Henüz bir tüzel kişilik için serbest bırakılmamış olan ürünler bir ürün sınıfına eklenebilir ve ürün sınıfı onaylanabilir. Ancak, ürünler bir tüzel kişilik için serbest bırakılana kadar perakende kanalları için kullanılabilir olmayacaktır.                                                                                                                                                                                                                                                                                     |
| Kategori hiyerarşisi ayarlayın.      | Perakende ürünlerinizi oluştururken, Dynamics 365 for Operations'taki kategori hiyerarşisi özelliğini kullanarak ürünleri gruplayabilir ve kategorilere ayırabilirsiniz. Tüm perakende kanallarınıza dağıttığınız tüm ürünleri gruplandırmak ve kategorize etmek için bir temel hiyerarşi oluşturabilirsiniz. Ayrıca, promosyon veya ürün sınıfları gibi belirli amaçlar için ürünleri gruplamak ve kategorize etmek üzere ayrı, ek kategori hiyerarşileri de oluşturabilirsiniz. Kategori hiyerarşilerini kullanarak, belirli bir kategorideki tüm ürünlerinizi bir ürün sınıfına atayabilirsiniz. Ürün sınıfına dahil edilen kategoriye eklenen tüm ürünler otomatik olarak ürün sınıfına dahil edilir. Perakende ürün sınıfı planlayıcının bir sonraki çalışması sırasında, bu ürünler ürün sınıfının atandığı perakende kanalları tarafından kullanılabilir.                                            |

## <a name="setting-up-an-assortment"></a>Ürün sınıfı ayarlama
Önkoşulları tamamladıktan sonra, bir ürün sınıfı oluşturup perakende kanallarınıza atayabilirsiniz. Bir ürün sınıfı ayarlamak için aşağıdaki görevleri tamamlamanız gerekir.

1.  Yeni bir ürün sınıfı oluşturun veya mevcut bir ürün sınıfını kopyalayın.
2.  Ürün sınıfının uygulanacağı perakende kanallarını veya yüksek düzey perakende kanalı gruplarını seçin.
3.  Ürün sınıfına ürün kategorileri, bireysel ürünler veya ürün varyantları ekleyin. Tüm ürünleri belirli bir kategoriye ekleyebilir veya seçilen ürünleri ürün sınıfına dahil edilen bir kategoriden çıkarabilirsiniz.
4.  Ürün sınıfını yayınlayın. Bir ürün sınıfını yayınladığınızda, perakende ürün sınıfı planlayıcı otomatik olarak çalışır. Bu işlem, ürün listesini oluşturur. Bu işlem tamamlandığında, ürünler ürün sınıfının atandığı perakende kanalları tarafından kullanılabilir duruma gelir. Yayınlanmış olan bir ürün sınıfında veya ürün sınıfının atandığı perakende kanallarda değişiklikler yapılırsa, ürün sınıfının da güncelleştirilmesi gerekir. Değişiklikler yapıldığında ürün sınıfını güncelleştirmek için perakende ürün sınıfı planlayıcıyı toplu iş olarak çalıştırabilirsiniz.





