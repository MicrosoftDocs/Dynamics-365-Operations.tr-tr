---
title: Kıymetler ve iş emirleri
description: Bu konuda Kıymet Yönetimi'ndeki kıymetler ve iş emirleri açıklanmaktadır.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2872dc84ec11ae7fad9fd5b225b9207f13280db334cc0d010a3d6749a591ee2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718119"
---
# <a name="assets-and-work-orders"></a>Kıymetler ve iş emirleri

[!include [banner](../../includes/banner.md)]

 

Bu konuda Kıymet Yönetimi'ndeki kıymetler ve iş emirleri açıklanmaktadır. Kıymetler ve iş emirleri Kıymet Yönetimi'nin merkezi parçalarıdır. Bir *kıymet* sürekli bakım ve hizmet gerektiren bir makine veya makine parçasıdır. Kıymetler hiyerarşik yapıda oluşturulabilir ve işlem yapılacak yerleşimle ilişkili olabilirler. Bakım işleri, kıymet yapısının tüm düzeyleriyle planlanabilir.

Ürün bilgileri ve kıymet belirtimi gibi çeşitli veriler ve gerekli bakım planları her kıymet için ayarlanmıştır. Aşağıdaki çizimde kıymet verilerine genel bakışla kıymetlerin iş türleriyle ilişkisi gösterilmektedir. Kırmızı metin devir ve bağımlılıkları gösteren örnekler için kullanılır.

![İş türleriyle ilgili varlık verilerini gösteren diyagram.](media/05-overview-image.png)

Her iş emrinin önleyici bakım, düzeltici bakım veya inceleme gibi bir iş emri türü vardır. İş emri bir veya daha fazla iş emri işi içerir. Her iş emri işi bir kıymet ve ilgili iş türü üzerinde gerçekleştirilmesi gereken bir işi tanımlar. İlgili iş türlerine 10.000 km, 50.000 km, 1 yıllık bakım ve güvenlik incelemesi örnek verilebilir. Bir iş emri birden çok kıymetle ilgili olabilir.

Aşağıdaki çizimde bir iş emrindeki anahtar verilere genel bakış gösterilmektedir.

![İş emrindeki anahtar verileri gösteren diyagram.](media/06-overview-image.png)

Bir iş emri başka bir iş emriyle ilgili olabilir ve iş türleri bir iş emri oluşturan izleyen işleri içerebilir. Genel olarak iş emirleri arasında bağımlılık yoktur. Bu nedenle, iş emri yaşam döngüsü durumunu değiştirebilirler ve birbirinden bağımsız olarak zamanlanabilirler.

İş emirleri düzeltici, önleyici veya reaktif bakımla ilgili çeşitli şekillerde oluşturulabilir. Ayrıca iş emirlerini el ile de oluşturabilirsiniz. Aşağıdaki çizimde iş emirlerini otomatik veya el ile oluşturma işlemine genel bakış gösterilmektedir.

![İş emirlerinin otomatik veya el ile oluşturulmasını gösteren diyagram.](media/07-overview-image.png)

Bir iş emri üzerinde bakım işi zamanlamak ve çalıştırmak istediğinizde birkaç adımın tamamlanması gerekir. Aşağıdaki çizimde bir iş emrinin işlenmesine genel bakış gösterilmektedir.

![İş emri işlemenin genel görünümünü gösteren diyagram.](media/08-overview-image.png)

> [!NOTE]
> Genel olarak, Dynamics 365 Supply Chain Management ve **Kıymet Yönetimi** modülünde çalışırken yeni kayıt oluşturmak için **Yeni**'yi, mevcut kaydı güncelleştirmek için **Düzenle**'yi ve yeni veya düzenlenmiş verileri kaydetmek için **Kaydet**'i seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]