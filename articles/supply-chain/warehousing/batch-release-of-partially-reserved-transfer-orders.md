---
title: Kısmen rezerve edilen transfer emirleri için toplu iş serbest bırakma
description: Bu makale bir mobil cihazdan kısmi rezerve edilmiş transfer emirlerini toplu serbest bırakmanın nasıl ayarlanacağını ve uygulanacağını açıklamaktadır.
author: perlynne
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 741377a43e2bfe702b213647cc6460a3d6ad93fb
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218697"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Kısmen rezerve edilen transfer emirleri için toplu iş serbest bırakma

[!include [banner](../includes/banner.md)]

Kısmi rezerve edilmiş transfer emirlerini toplu serbest bırakma işlevi, bir transfer emrini bir ambara, bir toplu iş kullanarak kısmi serbest bırakmanıza olanak sağlar.
Kısmi bir miktarı serbest bırakma seçeneğine sahip olduğunuz için bir siparişi serbest bırakmadan önce tüm miktarın ambarda kullanılabilir olmasını beklemenize gerek yoktur.

Siparişlerin bir ambara serbest bırakılması, bir ambar yönetimi işlemleridir (WMS). Bu işlem çekme, paketleme, sevkiyat gibi bir ambar çalışanının bir mobil cihaz kullanarak gerçekleştirebileceği etkinlikleri içerir.

## <a name="where-it-applies"></a>Uygulandığı yerler

Bu işlev için, transfer emirleri bir ambara bir toplu iş kullanarak serbest bırakılır. Bu işlev, ambarda yeterli stoka sahip değilseniz ancak maddeleri yine de bir ambardan diğerine transfer etmek istiyorsanız yararlıdır.

## <a name="how-it-is-set-up"></a>Nasıl ayarlanır

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Transfer emirleri ve satış siparişleri için yerine getirilme ölçütleri belirtin

Bir sipariş kısmen bir ambara toplu bir işte serbest bırakılmadan önce, yerine ölçütünün karşılanması gerekir. Bu karşılanma kriterleri yerine getirme ilkesi tarafından belirlenir.

Transfer emirleri ve satış siparişleri için yerine getirme ilkeleri şirket düzeyinde belirtilir. Yerine getirme ilkesinin kurulumuna bağlı olarak, bir toplu işteki siparişlerin serbest bırakılması kabul veya reddedilir. Siparişler daha sonra uygun şekilde işlenir.

- Transfer emirleri ve satış siparişleri için yerine getirme ilkeleri oluşturmak için **Ambar yönetimi \> Kurulum \> Ambara serbest bırak \> Yerine getirme ilkeleri**'ne gidin ve bir ad ve açıklama girerek bir yerine getirme ilkesi oluşturun.
- Yerine getirme oranını, bir değer türünü ve yerine getirme ilkesi ihlal edilirse gösterilecek mesajı belirtmek için **Ambar yönetimi \> Kurulum \> Ambara serbest bırak \> Yerine getirme ilkeleri**'ne gidin ve sonra **Yerine getirme oranı**, **Değer türü** ve **Yerine getirme ihlal mesajı** alanlarını ayarlayın.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Transfer emirleri ve satış siparişleri için yerine getirilme ilkelerini ayarlayın

- Transfer emirleri için yerine getirme ilkelerini ayarlamak için **Stok yönetimi \> Kurulum \> Stok ve ambar yönetimi parametreleri**'ne gidin ve ardından **Transfer emirleri** sekmesindeki **Ambar yönetimi** bölümünde bir transfer emri yerine getirme ilkesi seçin.
- Satış siparişleri için yerine getirme ilkeleri ayarlamak için **Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**'ne gidin ve ardından **Ambar yönetimi** sekmesinde bir satış siparişi yerine getirme ilkesi seçin.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-released-in-a-batch"></a>Toplu iş içinde serbest bırakmaya izin verme ve bir toplu iş içinde serbest bırakılacak miktarı belirtme

Bir toplu iş, siparişleri bir ambara toplu olarak serbest bırakmakta kullanılır. Bir toplu işte çalışacak siparişleri ayırt eden parametreler, toplu işin kendisinde ayarlanır.

**Miktar** parametresi, fiziksel olarak rezerve edilmiş miktarı veya toplam miktarın mı toplu işte serbest bırakılacağını belirtir. **Kısmi serbest bırakılmış siparişlerin serbest bırakılmasına izin ver** parametresi, toplu işteki hangi siparişlerin, daha önce kısmen serbest bırakılmışlarsa kabul edileceğini veya reddedileceğini belirler.

- Transfer emirleri için **Miktar** ve **Kısmi serbest bırakılmış siparişlerin serbest bırakılmasına izin ver** parametrelerini ayarlamak için **Ambar yönetimi \> Ambara serbest bırak \> Transfer emirlerini otomatik olarak serbest bırak** seçeneğine gidin.
- Satış siparişleri için **Miktar** ve **Kısmi serbest bırakılmış siparişlerin serbest bırakılmasına izin ver** parametrelerini ayarlamak için **Ambar yönetimi \> Ambara serbest bırak \> Satış siparişlerini otomatik olarak serbest bırak** seçeneğine gidin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
