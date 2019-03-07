---
title: Servis nesne grupları
description: Nesne grupları, raporlara ve istatistiklere yönelik nesneler hakkındaki verilerin sıralaması ve filtrelenmesi açısından yararlıdır.
author: ShylaThompson
manager: AnnBe
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc5b1bf93deaf60a3c6384671ad575c73871eb35
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "312244"
---
# <a name="service-object-groups"></a>Servis nesne grupları 

[!include [banner](../includes/banner.md)]

Nesne grupları, raporlara ve istatistiklere yönelik nesneler hakkındaki verilerin sıralaması ve filtrelenmesi açısından yararlıdır. Örneğin, nesneleri coğrafi konuma veya türe göre gruplandırabilirsiniz.

## <a name="group-by-geographical-location"></a>Coğrafi konuma göre gruplandırma

Şirket hizmetlerinizin bulunduğu farklı nesnelerin yerini göstermek üzere bu gruplandırma yöntemini kullanabilirsiniz. Nesneleri coğrafi konuma göre gruplandırmak aynı zamanda örneğin, belirli bir ülkede/bölgede şirketinizin zaten hizmet verdiği nesneleri tanımlamanız gereken durumlarda da yararlı olabilir.

## <a name="example"></a>Örnek

Belçika'da bulunan bir müşteri servis merkezinizi arayarak ABC adlı bir nesne için bir servis sözleşmesi oluşturmak ister. Belçika'da servis yapılan tüm nesnelere Belçika adında bir coğrafi konum nesne grubu iliştirirsiniz. Bu grubu bir filtre olarak kullanarak, ABC'nin programınızda bir kayıt olarak bulunup bulunmadığını veya yeni bir nesne oluşturmanız gerekip gerekmediğini görmek üzere hızlı bir arama yapabilirsiniz. 

## <a name="group-by-type"></a>Tipe göre gruplandırma

Bu gruplandırma yöntemini, şirketinizin servis verdiği nesne türlerine göstermek üzere kullanabilirsiniz. Ayrıca, nesneleri türe göre gruplandırmak programdaki benzer mevcut nesneleri temel alan yeni bir nesne oluşturmak istediğiniz durumlarda da yararlı olabilir.

## <a name="example"></a>Örnek

Müşteri sizi arayarak HIJ adındaki bir klima cihazı için sizinle bir servis sözleşmesi yapmak ister. Bu cihaz için henüz bir kaydınız yoktur. Ancak, Klima adlı bir nesne grubu oluşturur ve bu grubu tüm klima nesnelerine iliştirirsiniz. Bu nedenle, diğer tüm klima cihazlarını çabuk şekilde arayıp tanımlayabilir ve HIJ'ye ait servis sözleşmesi satırlarını oluşturmak için bu nesnelerden alınmış şablon bilgilerini kullanabilirsiniz. Nesne gruplarını bu şekilde kullanarak hızlı bir şekilde yeni nesneler oluşturabilir ve bunlar üzerinde gerçekleştirilecek servis görevlerini belirleyebilirsiniz. 

## <a name="create-service-object-groups"></a>Servis nesnesi grupları oluşturma

Servis nesneleri atayabileceğiniz gruplar oluşturun. Servis nesneleri, servislerin gerçekleştirilmesinde kullanılan stok maddeleri ve diğer ürünlerdir. Servis nesnelerini gruplandırarak benzer ve ilgili servis nesneleriyle ilgili raporlar oluşturabilirsiniz. Örneğin, bir servis nesne grubu iki servis nesnesi içerebilir: Bir servis nesnesi bir set ve diğer servis setin takılması için gerçekleştirilen hizmettir.

Servis nesne grupları oluşturmak için şu adımları izleyin:

1. **Servis yönetimi > Kurulum > Servis nesneleri > Servis nesnesi grupları**'na tıklayın.

2. Yeni servis nesnesi grubu oluşturmak için **Yeni**'ye tıklayın.

3. Servis nesnesi grubu için benzersiz bir ad ve isteğe bağlı olarak açıklama girin.

Servis nesnelerini **Servis nesneleri** formunu kullanarak gruba atayabilirsiniz. 

## <a name="see-also"></a>Ayrıca bkz.

[Servis nesneleri oluşturma](create-service-objects.md)


