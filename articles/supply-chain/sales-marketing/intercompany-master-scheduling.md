---
title: Şirketlerarası master planlama
description: Bu konuda, şirketlerarası master planlama açıklanmaktadır
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4993f981b268127af7c9259aa0e73a8e4a75015a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851463"
---
# <a name="intercompany-master-scheduling"></a>Şirketlerarası master planlama

[!include [banner](../../includes/banner.md)]

Şirketlerarası master planlama, gereksinimleri hesaplamanıza ve birkaç dahili şirket arasında planlanmış şirketlerarası sipariş oluşturmanıza yardımcı olan bir yöntemdir. Şirketlerarası master planlama, belirlediğiniz tekrar sayısının üzerinden gerçekleştirilir. Microsoft Dynamics 365 Supply Chain Management uygulamasının master planlama gerçekleştirmesini sağlamak için şirketlerarası şirketlerinizin her birinde master planlama ayarlaması yapmanız gerekir. Bu, Microsoft Dynamics 365 Supply Chain Management uygulamasının otomatik olarak bir şirketlerarası satın alma siparişi oluşturduğu birkaç yineleme gerektirir; bu da şirketler arası bir satış siparişinin otomatik olarak oluşturulmasına yol açar ve bu da yine taleplerin oluşmasına yol açar.

Şirketlerarası master plan ve şirketlerarası planlama sırasını, şirketlerarası şirketlerin her birindeki **Master planlama** parametrelerinde ayarlayabilirsiniz.

Şirketlerarası zincirinde talebi çoğaltmak için planlanmış satın alma siparişlerinin otomatik olarak kesinleştirilmesini sağlayacak parametreleri ayarlamanız gerekir; başka bir deyişle, siparişler süre veya miktar bakımından değiştirilemez. Kapsam grubunda **Kesinleştirme zaman dilimi**'ni veya Master planda **Kesinleştirme zaman dilimi**'ni ayarlayın. Hiçbir **Kesinleştirme zaman dilimi** ayarlanmazsa otomatik olarak şirketlerarası satın alma siparişi oluşturulmaz. Master planlamanın yalnızca ilk yürütmesi planlı siparişlerle sonuçlanır. Ancak, şirketlerarası satın alma siparişi oluşturulmadığından şirketlerarası satış siparişi oluşturulmaz ve bu nedenle şirketlerarası satın alma siparişi de oluşturulmaz ve bu böyle devam eder.

Şirketlerarası master planlamayı başlattığınızda Microsoft Dynamics 365 Supply Chain Management önce şirketlerarası şirketlerin her birinde master planlama gerçekleştirir; ardından da şirketlerarası şirketlerin her birinde ikinci bir master planlama gerçekleştirir; belirtilen tekrar sayısına erişilene kadar da bu böyle devam eder. En çok 30 tekrar yapılabilir; ancak ne kadar çok tekrar seçerseniz planlama işlemi de o kadar uzun sürer.

Şirketlerdeki master planlama, şirketlerarası planlama sırası (programın tüm şirketlerarası şirketler arasındaki master planlamaları önceliklendirme sırası) tarafından denetlendiğinden şirketlerarası master planlamayı şirketlerarası şirketlerin herhangi birinden başlatabilirsiniz. Şirketlerarası planlama sırası, master planlamanın şirketlerdeki gerçekleştirilme sırasını belirlediğinden şirketlerarası master planlamaya nereden başlandığının önemi yoktur. Her tekrarda, geçerli şirket en sonuncuyu yürütür.

> [!NOTE]
> En iyi yöntem, şirketlerarası master planlamanın bir Microsoft Dynamics 365 Supply Chain Management şirketinden başlatılmasıdır.

**Şirketlerarası master planlama** sayfasında, bir master planlama sırası başlatabilirsiniz; bu, tüm şirketlerarası şirketlere yönelik olarak belirlenmiş birinci tekrar için seçtiğiniz gereksinim hesaplamasının güncelleştirilmesi ilkesiyle ilk master planlamayı yürütür. İzleyen tekrarlarda, sonraki tekrar için seçtiğiniz ikincil ilke kullanılır ve belirlediğiniz tekrar sayısına erişilene kadar bu ilke uygulanmaya devam eder.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
