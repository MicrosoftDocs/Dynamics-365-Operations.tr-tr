---
title: Servis siparişleri
description: Bir servis siparişi, bir servis teknisyeninin belirli bir tarihte müşteri tesisine yaptığı ziyareti gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64863b8c19c756cffab94adeaa9c38a0a3388d70
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215045"
---
# <a name="service-orders"></a>Servis siparişleri   

[!include [banner](../includes/banner.md)]


Bir servis siparişi, bir servis teknisyeninin belirli bir tarihte müşteri tesisine yaptığı ziyareti gösterir. Her servis siparişi bir veya daha fazla servis siparişi satırından oluşur. Servis siparişi satırları servis teknisyeninin gerçekleştirmesi gereken saat sayısını ve ilgili maddeleri, giderleri ve ücretleri gösterir.

Servis siparişi satırına görevleri ve nesneleri ekleyebilirsiniz. Servis siparişi satırlarını daha sonra göreve ya da nesneye göre gruplayabilirsiniz. Ayrıca, stokta listelenen maddeleri servis siparişi satırlarına iliştirebilirsiniz.

## <a name="create-service-orders"></a>Servis siparişleri oluştur

Servis siparişlerini servis sözleşmesini ve sözleşmede yer alan satırları temel alarak oluşturabilirsiniz. Ancak, bir servis sözleşmesiyle ilişkili olan servis siparişlerini yalnızca sözleşmede belirtilen dönemde oluşturabilirsiniz. Örneğin, bir servis sözleşmesi 2011 takvim yılı için geçerliyse, sözleşme için 1 Ocak 2011 ve 31 Aralık 2011 arasında servis siparişleri oluşturabilirsiniz.

Servis siparişlerini, sözleşmeyle ilişkilendirmeden tek tek de oluşturabilirsiniz. Bu servis siparişleri zamanlanmamış veya bir defalık servis ziyaretlerini işlemek için kullanılabilir. Örneğin, Mart ayında müşteriniz servis sözleşmesinde belirtilenlere ek olarak iki makineye servis yapılmasın ister. Bu görev için servis siparişlerini oluşturursunuz ancak bunları sözleşmeyle ilişkilendirmezsiniz.


> [!NOTE]
> <P>Bir servis sözleşmesiyle ilişkilendirilmemiş servis siparişleri oluşturmak için <STRONG>Servis yönetimi parametreleri</STRONG> formunda <STRONG>Servis sözleşmesi olmadan izin ver</STRONG> onay kutusunu işaretlemeniz gerekir.</P>

**Senaryo**

Aşağıdaki senaryo bir servis sözleşmesiyle ilişkili olmayan bir servis siparişi oluşturmanın yararlı olacağı başka bir durumu açıklar.

Şirket dağıtıcısı bir asansöre acil servis yapılmasını talep eden bir arama alır. Bir servis sözleşmesi ve servis için bir proje ayarlamak için zaman yoktur. Bu nedenle dağıtıcı bir servis siparişini doğrudan **servis siparişleri** formunda oluşturur, servis siparişini varolan bir projeye ekler ve servis siparişi satırları oluşturur. Dağıtıcı servis sözleşmesiyle ilişkili olmayan işleri kaydetmek üzere mevcut bir servis siparişi için bir görev veya nesne ilişkisi oluşturabilir. Daha fazla bilgi için bkz. [Servis siparişlerini el ile oluşturma](create-service-orders-manually.md) ve [Servis görevi ilişkileri oluşturma](create-service-task-relations.md).

## <a name="monitor-the-progress-of-service-orders"></a>Servis siparişlerinin ilerlemesini izleme

Farklı takımlar ve iş süreçleri üzerinden bir satış siparişi ilerlemesini izlemek için servis siparişleri aşamaları ve neden kodları için bir sistem ayarlayabilirsiniz. Her aşama için izin verilen eylemleri belirtebilirsiniz. Daha fazla bilgi için bkz. [Neden kodları oluşturma](create-reason-codes.md).

**Örnek**

Bir servis siparişi dağıtıcı tarafından onaylanır. Dağıtıcı servis siparişi aşamasını güncelleştirir ve servis siparişinin servis teknisyenine serbest bırakıldığını belirten bir neden kodu belirtir. Teknisyen müşteri tesisine gider ve servisi yerine getirir.

## <a name="specify-item-requirements-for-service-orders"></a>Servis siparişleri için madde gereksinimleri belirtme

Servis siparişleri için gerekli olan stok maddeleri belirtebilirsiniz. Bununla birlikte, servis siparişi bir proje ile ilişkili olmalıdır. Servis siparişleri için madde gereksinimleri bir proje aracılığıyla işlenir. 

**Örnek**

Servis sözleşmesinden oluşturulan servis siparişleri sevk memuru tarafından işlenir. Birinci servis siparişinde, dağıtıcı servis teknisyenin eldeki stokta bulunmayan önemli bir yedek parçaya gereksinimi olduğunu fark eder. Bu nedenle, dağıtıcı yedek parça için doğrudan servis siparişinden bir madde gereksinimi oluşturur.

## <a name="move-and-post-lines"></a>Satırları taşıma ve deftere nakletme

Servis teknisyeni servis ziyaretinden döner ve sonra değişikliklere göre servis siparişi satırlarını güncelleştirir. Servis ziyaretindeyken teknisyen bir sonraki servis ziyaretinde yapılması planlanan bir servis işini gerçekleştirmiştir. Bu nedenle, teknisyen sonraki servis ziyaretindeki satırları geçerli servis ziyaretine taşır. Teknisyen ardından servis siparişini deftere nakleder. Daha fazla bilgi için bkz. [Servis siparişi satırlarını taşıma](move-service-order-lines.md).

## <a name="cancel-service-orders"></a>Servis siparişlerini iptal et

Söz konusu işin iptal edilmesi nedeniyle, Ocak ayı için oluşturulan diğer servis siparişlerinden biri geçersiz hale gelmiştir. Bu nedenle, servis dağıtıcısı servis siparişini iptal eder. Daha fazla bilgi için bkz. [Servis siparişlerini iptal etme](cancel-service-orders.md).

## <a name="post-from-projects"></a>Projelerden deftere nakletme

Her haftanın sonunda, dağıtıcı belirli bir projeye iliştirilmiş tüm servis siparişlerini deftere nakletmek ister. Bu nedenle, dağıtıcı **Projeler** formunda ilgili projeyi bulur ve tamamlanan servis siparişlerini deftere nakleder. Daha fazla bilgi için bkz. [Servis siparişlerini deftere nakletme (sınıf formu)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).

## <a name="delete-service-orders"></a>Servis siparişlerini sil

Yılın ikinci yarısında müşteriniz servis ziyaretlerinin çok az sıklıkta gerçekleştiğine karar verir. Servis anlaşmasındaki geri kalan süre için yeni ve daha sık bir servis ziyaretleri dizisi oluşturmanız gerekmektedir. Bu nedenle, mevcut servis siparişlerini silmeniz ve yeni servis siparişleri oluşturmanız gerekir. Daha fazla bilgi için bkz. [Servis siparişlerini silme](delete-service-orders.md).

## <a name="see-also"></a>Ayrıca bkz.

[Servis siparişleri (form)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))

  


