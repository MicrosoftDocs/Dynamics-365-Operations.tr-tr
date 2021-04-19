---
title: Üretimdeki malzemeler için varsayılan rezervasyon ilkesini geçersiz kılma
description: Bu konuda, her madde modeli grubu için varsayılan bir rezervasyon ilkesinin nasıl ayarlanacağını açıklanmaktadır. Böylece farklı rezervasyon ilkeleri, üretim ürün reçetesi (BOM) veya toplu iş emri formülünün parçası olan her bir maddeye otomatik olarak uygulanabilir.
author: johanhoffmann
ms.date: 12/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a1b2dd204c9a507dba387b0295f3021253e02dc4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814814"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a>Üretimdeki malzemeler için varsayılan rezervasyon ilkesini geçersiz kılma

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

*Varsayılan üretim rezervasyonunu geçersiz kıl* özeliği, her madde modeli grubu için varsayılan rezervasyon ilkesini ayarlamanızı sağlar. Bu sayede, üretim ürün reçetesi (BOM) veya toplu iş siparişi formülünün parçası olan her maddeye farklı rezervasyon ilkeleri otomatik olarak uygulanabilir. Her madde modeli grubunun sipariş için ayarlanan varsayılan rezervasyon ilkesini geçersiz kılıp kılmayacağını ve bunun yerine hangi rezervasyon ilkesinin (*el ile*, *tahmin*, *zamanlama*, *serbest bırakma* veya *başlatma*) kullanılacağını seçebilirsiniz.

Yeni bir üretim emri veya toplu iş emri oluşturduğunuzda, söz konusu emire ve tüm ürün reçetesi satırlarına veya formül satırlarına uygulanacak rezervasyon ilkesini seçmeniz istenir. *Varsayılan üretim rezervasyonunu geçersiz kıl* özelliği kullanıldığında, ürün reçetesi veya formül satırlarının bir kısmı veya tümü bu rezervasyon ilkesini geçersiz kılabilir ve bunun yerine ilgili madde modeli grubu için ayarlanan rezervasyon ilkesini kullanabilir.

Örneğin, malzeme çekme işi gerektiren hammaddeleriniz veya maddeleriniz varsa, fiziksel rezervasyon ambar işinin oluşturulması için bir ön koşul olduğundan, bu ürünler için oluşturulan ürün reçetesi veya formül satırları fiziksel bir rezervasyon gerektirir. Normalde rezervasyonun otomatik olarak gerçekleşmesini istiyorsanız *tahmin*, *zamanlama*, *serbest bırakma* veya *başlatma* rezervasyon ilkelerinden birini seçersiniz. Diğer taraftan, malzeme çekme işi gerektirmeyen malzemelerinzi veya maddeleriniz varsa, bunlar doğrudan bir yerleşimden tüketildiklerinden genellikle *el ile* rezervasyon ilkesini seçersiniz; bu ilke fiziksel rezervasyon yapmaz veya malzeme çekme işi oluşturmaz.

## <a name="turn-on-the-feature"></a>Özelliği etkinleştirme

Özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Üretim denetimi*
- **Özellik adı:** *(Önizleme) Varsayılan üretim ayırmalarını geçersiz kıl*

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a>Madde modeli grubuna üretim rezervasyon ilkesi atama

1. **Maliyet Yönetimi \> Stok muhasebe ilkeleri kurulumu \> Madde modeli grupları**'na gidin.
1. Madde modeli grubu oluşturun veya seçin.
1. **Stok ilkeleri** hızlı sekmesinde, **Madde üretim rezervasyonunu geçersiz kıl** onay kutusunu seçin.
1. **Rezervasyon** alanında, seçili model grubuna ait maddeler için rezervasyon ilkesini seçin. (Bu maddeler, bir ürün reçetesi veya formül satırındaki maddeleri içerir.)

    - **El ile**: Model grubundaki maddeler üretim için otomatik olarak fiziksel olarak rezerve edilemez. Ancak, gerektikçe el ile ayrılabilirler.
    - **Tahmin**: Model grubundaki maddeler üretim emri tahmini sırasında fiziksel olarak rezerve edilir.
    - **Zamanlama**: Model grubundaki maddeler üretim emrinin zamanlaması sırasında fiziksel olarak rezerve edilir.
    - **Serbest bırakma**: Model grubundaki maddeler üretim emri serbest bırakıldığında fiziksel olarak rezerve edilir.
    - **Başlama**: Model grubundaki maddeler üretim emrinin başlangıcında fiziksel olarak rezerve edilir.

## <a name="example-using-reservation-principles-in-a-bulkpack-scenario"></a>Örnek: Toplu iş/paket senaryosunda rezervasyon ilkelerini kullanma

Toplu yağ malzemesi, 1.000 litrelik karıştırıcıda üretilir. Toplu malzeme hazırladıktan sonra, farklı boyutlardaki şişelerin doldurulduğu çeşitli doldurma istasyonlarına gönderilir. Doldurma tamamlandıktan sonra, şişeler kutular halinde paketlenir. Bu kutular daha sonra paletlere yüklenir.

Bu senaryoda, 1.000 litre toplu malzeme oluşturmak için bir toplu iş emri oluşturulur. (Bu emir toplu iş emridir). Bu toplu iş emri tamamlandığında, doldurma istasyonlarının malzeme giriş yerleşimine tamamlandı olarak rapor edilir. Daha sonra, her şişe boyutunu doldurmak ve paketlemek için bir toplu iş emri oluşturulur. (Bu emirler, paketleme emirleridir.) Paketleme emirleri toplu malzeme, boş şişe, bir etiket ve diğer paketleme malzemelerini içeren bir formüle sahiptir. Toplu malzeme, doğrudan karıştırıcı tanktan doldurma istasyonlarına aktarıldığından, bu malzemeyi çekmek için herhangi bir ambar işi gerekmez ve toplu malzeme doğrudan giriş yerleşiminden tüketilir. Bu nedenle, rezervasyon ilkesi *el ile* olarak ayarlanır. Diğer malzemeler çekme işiyle doldurma istasyonuna hazırlanır. Bu nedenle, bu satırlar için rezervasyon ilkesi *serbest bırakma* olarak ayarlanır. Böylece paket emri serbest bırakıldığında rezervasyon otomatik olarak gerçekleşir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]