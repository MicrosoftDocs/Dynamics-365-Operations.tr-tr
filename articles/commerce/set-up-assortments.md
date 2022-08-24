---
title: Ürün sınıflarını ayarlama
description: Bu makalede, bir ürün çeşidinin ne olduğu ve Dynamics 365 Commerce'da ürün çeşitlerinin nasıl ayarlandığı açıklanmaktadır.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.industry: Retail
ms.search.form: RetailAssortmentDetails
ms.openlocfilehash: 26827a09962dbbb6be4e0a054e22424260592702
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271836"
---
# <a name="set-up-assortments"></a>Ürün çeşitleri ayarlama

[!include [banner](includes/banner.md)]

Bu makalede, bir ürün çeşidinin ne olduğu ve Dynamics 365 Commerce'da ürün çeşitlerinin nasıl ayarlandığı açıklanmaktadır.

Ürün çeşidi, fiziksel mağaza veya çevrimiçi mağaza gibi bir ticaret kanalına atadığınız bir ilgili ürünler topluluğudur. Ürün sınıflarını, her mağaza tarafından kullanılabilecek ürünleri tanımlamak üzere kullanabilirsiniz. Bir ürün sınıfı, ürün kategorileri içerebilir. Bu nedenle, belirli bir kategoriye atanan tüm ürünler ürün sınıfına dahil edilir. Bir ürün sınıfı belirli ürünleri ve belirli ürün varyantlarını da içerebilir. Bir ürün sınıfı ayarlayarak, kanallarınıza, mağazaların ihtiyacı olan herhangi bir kombinasyonda, aynı anda binlerce ürün atayabilirsiniz. İhtiyaç duyduğunuz kadar ürün sınıfı ayarlayabilirsiniz. Her ürün bir veya daha fazla ürün sınıfına dahil edilebilir ve her ürün sınıfı bir veya daha fazla kanalına atanabilir. Örneğin, temel ürün kümesi içeren bir ürün sınıfı belirleyebilirsiniz. Tüm mağazalar bu ürün sınıfını alır. Ardından, yalnızca geniş spor ekipmanlarını içeren başka bir ürün sınıfı tanımlayabilirsiniz. Bu ürün sınıfını yalnızca büyük mağazalarınız alır. Aşağıdaki şekilde ürünlerin ürün sınıflarına ve bu ürün sınıflarının kanallarına nasıl atanacağı gösterilmektedir.

![Ürün sınıfı ilişkileri.](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Önkoşullar

Bir ürün sınıfı ayarlamadan ve bunu bir ticaret kanalına atamadan önce aşağıdaki görevleri tamamlamanız gerekir.

| Görev                              | Tanım |
|-----------------------------------|-------------|
| Kanal ayarlayın.          | Kanalları fiziksel mağazayı, çevrimiçi mağazayı veya bir çevrimiçi marketi temsil eder. En az bir kanalı ayarlamanız ve mağaza için seçenekleri yapılandırmanız gerekir. Ürün sınıfları, belirli bir mağazanın alacağı ürünleri tanımlamak amacıyla mağazalara atanır. |
| Organizasyon hiyerarşisi oluşturun. | Kuruluşunuz için ticaret kanallarını ayarladıktan sonra, kanallarınızın organizasyon yapısını temsil eden bir organizasyon hiyerarşisi yapılandırmanız gerekir. Organizasyon hiyerarşisi ürün sınıfları, stok yenileme ve raporlama için kullanılabilir. Kanallarınızı bir organizasyon hiyerarşisine ekleyerek ürün sınıflarını mağaza gruplarına atayabilirsiniz. Ürün sınıfını her mağazaya ayrı ayrı atamak yerine, ürün sınıfını yüksek düzey organizasyon düğümüne atayın. Ardından, yüksek düzey organizasyon düğümüne yeni bir kanalı eklendiğinde, bu kanalı üst dzey organizasyon düğümüne atanmış olan ürün sınıflarını otomatik olarak devralır. Ürün sınıflarını yalnızca **Ticaret ürün sınıfı** amacıyla atanmış olan bir organizasyon hiyerarşisine dahil edilen perakende kanallarına atayabilirsiniz. |
| Ürünleri tanımlayın.                  | Ürünleri bir ürün çeşidine ekleyebilmek için önce Commerce'e eklemeniz gerekir. Ürünleri el ile ekleyebilir veya bir satıcıdan içer aktarabilirsiniz. Ürünleri ekledikten sonra, bunları bir tüzel kişilik için serbest bırakmanız gerekir. Yalnızca bir tüzel kişilik için serbest bırakılan ürünler kanallarınız tarafından kullanılabilir. Henüz bir tüzel kişilik için serbest bırakılmamış olan ürünler bir ürün sınıfına eklenebilir ve ürün sınıfı onaylanabilir. Ancak, ürünler bir tüzel kişilik için serbest bırakılana kadar kanalları için kullanılabilir olmayacaktır. |
| Kategori hiyerarşisi ayarlayın.      | Ticaret ürünlerinizi oluştururken, kategori hiyerarşisi özelliğini kullanarak ürünleri gruplayabilir ve kategorilere ayırabilirsiniz. Tüm kanallarınıza dağıttığınız tüm ürünleri gruplandırmak ve kategorize etmek için bir temel hiyerarşi oluşturabilirsiniz. Ayrıca, promosyon veya ürün sınıfları gibi belirli amaçlar için ürünleri gruplamak ve kategorize etmek üzere ayrı, ek kategori hiyerarşileri de oluşturabilirsiniz. Kategori hiyerarşilerini kullanarak, belirli bir kategorideki tüm ürünlerinizi bir ürün sınıfına atayabilirsiniz. Ürün sınıfına dahil edilen kategoriye eklenen tüm ürünler otomatik olarak ürün sınıfına dahil edilir. Ticaret ürün sınıfı planlayıcının bir sonraki çalışması sırasında, bu ürünler ürün sınıfının atandığı kanalları tarafından kullanılabilir. |

## <a name="setting-up-an-assortment"></a>Ürün sınıfı ayarlama

Önkoşulları tamamladıktan sonra, bir ürün sınıfı oluşturup kanallarınıza atayabilirsiniz. Bir ürün sınıfı ayarlamak için aşağıdaki görevleri tamamlamanız gerekir.

1. Yeni bir ürün sınıfı oluşturun veya mevcut bir ürün sınıfını kopyalayın.
2. Ürün sınıfının uygulanacağı kanallarını veya yüksek düzey kanalı gruplarını seçin.
3. Ürün sınıfına ürün kategorileri, bireysel ürünler veya ürün varyantları ekleyin. Tüm ürünleri belirli bir kategoriye ekleyebilir veya seçilen ürünleri ürün sınıfına dahil edilen bir kategoriden çıkarabilirsiniz.
4. Ürün sınıfını yayınlayın. Bir ürün sınıfını yayınladığınızda, ürün sınıfı planlayıcı otomatik olarak çalışır. Bu işlem, ürün listesini oluşturur. Bu işlem tamamlandığında, ürünler ürün sınıfının atandığı kanalları tarafından kullanılabilir duruma gelir. Yayınlanmış olan bir ürün sınıfında veya ürün sınıfının atandığı kanallarda değişiklikler yapılırsa, ürün sınıfının da güncelleştirilmesi gerekir. Değişiklikler yapıldığında ürün sınıfını güncelleştirmek için ürün sınıfı planlayıcıyı toplu iş olarak çalıştırabilirsiniz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
