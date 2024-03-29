---
title: Servis siparişlerini otomatik oluşturma
description: Servis sözleşmesinin geçerli olduğu dönem için bir servis sözleşmesini temel alan servis siparişleri oluşturabilirsiniz.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41f48e2156ea5f57e600cc5dec09a78a91992d60
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675809"
---
# <a name="automatically-create-service-orders"></a>Servis siparişlerini otomatik oluşturma 

[!include [banner](../includes/banner.md)]


Servis sözleşmesinin geçerli olduğu dönem için bir servis sözleşmesini temel alan servis siparişleri oluşturabilirsiniz.

Bir servis sözleşmesinden oluşturduğunuz servis siparişleri servis sözleşmesine iliştirilir.

Servis siparişleri otomatik olarak aşağıdaki ayarlardan oluşturulur:

  - Servis sözleşmesi satırlarında ayarlanan servis sözleşmesi aralığı. Servis sözleşmesi aralığı servis siparişi satırlarının oluşturulma sıklığını gösterir. Daha fazla bilgi için bkz. [Servis aralıkları](service-intervals.md).

  - **Servis siparişleri oluştur** formundaki **Başlangıç tarihi** ve **Bitiş tarihi** alanlarındaki servis dönemini tanımlamak için belirttiğiniz dönem. Daha fazla bilgi için bkz. [Servis siparişlerini otomatik oluşturma](create-service-orders-automatically.md).

  - Servis sözleşmesi başlığındaki **Servis siparişlerini birleştir** seçeneği. Bu seçenek servis sözleşmesinden oluşturulan servis siparişi satırlarının servis siparişlerini personele, servis görevine, servis nesnesine veya servis sözleşmesine göre birleştirip birleştirmeyeceğini tanımlar. Daha fazla bilgi için bkz. [Servis siparişlerini birleştirme](combine-service-orders.md).

  - Servis sözleşmesi satırındaki **Zaman aralığı** seçeneği. Zaman aralığı bir servis siparişinin hesaplanan tarihi ile bağlantılı olarak ne kadar uzağa taşınabileceğini tanımlar. Daha fazla bilgi için bkz. [Zaman aralıkları](time-windows.md).


> [!NOTE]
> <P>Bir servis siparişi için belirtilen gün <STRONG>Servis yönetimi parametreleri</STRONG> formunda seçtiğiniz takvimde açık değilse, takvim uyumsuzluğu olduğunu belirten bir iletiyle karşılaşırsınız. Endişe etmeden iletiyi yok sayabilirsiniz; söz konusu gün takvimde kapalı olmasına karşın servis siparişi oluşturulur.</P>

## <a name="example-1"></a>Örnek 1

Servis sözleşmesi 1 Ocak 2012'den 31 Kasım 2012'ye kadar sürer. **Servis siparişleri oluştur** formunda belirttiğiniz servis dönemi 1 Kasım 2012 ile 1 Kasım 2013 arasındaysa, servis siparişleri 1 Kasım 2012'den 31 Aralık 2012'ye kadar oluşturulur.

## <a name="example-2"></a>Örnek 2

Servis sözleşmesi 1 Ocak 2012'den 31 Kasım 2012'ye kadar sürer. İki servis sözleşmesi satırı servis sözleşmesine iliştirilir. İlk servis sözleşmesi satırının başlangıç tarihi 2 Ocak 2012 ve bitiş tarihi 1 Mart 2012'dir. İkinci servis sözleşmesi satırının başlangıç tarihi 1 Nisan 2012 ve bitiş tarihi 31 Aralık 2012'dir. **Servis siparişleri oluştur** formunda 1 Ekim 2012 ile 31 Aralık 2012 arasında olan bir dönem belirtirsiniz. Dolayısıyla, birinci sözleşme satırının başlangıç tarihi ve bitiş tarihi servis siparişi için belirttiğiniz dönemden önce olduğundan servis siparişleri yalnızca ikinci sözleşme satırı için oluşturulur.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]