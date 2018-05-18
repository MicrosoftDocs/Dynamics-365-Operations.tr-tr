---
title: "Servis sözleşmeleri"
description: "Servis sözleşmesi tipik bir servis ziyaretinde kullanılan kaynakları ve bu kaynakların müşteriye ne şekilde faturalandığını tanımlamanızı sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bf9df2a31c758ba6b63ac7952e00065df04552dc
ms.openlocfilehash: aaff0c1d71fcf2656d5d6e76a2bf4b7b3a699281
ms.contentlocale: tr-tr
ms.lasthandoff: 02/19/2018

---

# <a name="service-agreements"></a>Servis sözleşmeleri

[!include [banner](../includes/banner.md)]

Servis sözleşmesi tipik bir servis ziyaretinde kullanılan kaynakları ve bu kaynakların müşteriye ne şekilde faturalandığını tanımlamanızı sağlar.

Her servis sözleşmesi, hareketlerin deftere nakledildiği ve faturalandığı bir projeye iliştirilir. Ancak servis siparişi hareketlerini servis siparişini öncelikle bir servis sözleşmesine bağlamadan da doğrudan proje üzerinden faturalandırabilirsiniz. Servis siparişinin yalnızca bir defalık servis ziyareti olması ve servis hareketlerini hızlı bir şekilde işleme gereksiniminin belirli bir dönem boyunca müşteri hakkında ayrıntılı servis sözleşmesi bilgileri tutma gereksinimine ağır basması durumunda bunu yapmaya karar verebilirsiniz.

## <a name="service-agreement"></a>Servis sözleşmesi

Her servis sözleşmesinde, bir proje, bir servis sözleşmesi kodu ve bir servis sözleşmesi grubu belirtmeniz gerekir. Servis sözleşmesi grubu servis sözleşmelerini sıralamak ve düzenlemek için kullanılır.

Servis sözleşmesi başlığı, iliştirilmiş tüm sözleşme satırları için geçerli olan ayarları içerir:

-  Servis sözleşmesinin askıya alınıp alınmadığı. Servis sözleşmesi askıya alınmışsa, servis sözleşmesinden servis siparişleri oluşturamazsınız.
-  Servis sözleşmesinin süresi.
-  Servis sözleşmesi satırlarının servis siparişleriyle ne şekilde birleştirileceği.
-  Servis sözleşmesinin bir şablon olup olmadığı

Servis sözleşmesi başlığında sözleşmenin çeşitli satırlarına eklenecek belirli servis görevlerini veya servis nesnelerini girerek servis sözleşmesiyle birlikte kullanılabilecek tüm servis nesnelerini ve servis görevlerini de ayarlayabilirsiniz.

Ayrıca, servis sözleşmesi başlığından servis sözleşmesi satırlarını veya servis şablonu satırlarını alarak geçerli servis sözleşmesine kopyalayabilirsiniz.

Servis sözleşmelerini askıya alabilir ve servis sözleşmesi satırlarını ayrı ayrı durdurabilirsiniz.

Servis sözleşmesi satırında **Askıda** onay kutusunu seçerseniz şunları yapamazsınız:

-    Servis sözleşmesinden otomatik olarak veya el ile servis siparişleri oluşturamazsınız.

Servis sözleşmesi satırındaki **Durduruldu** onay kutusunu seçerseniz şunları yapamazsınız:

-    Servis sözleşmesi satırından otomatik olarak veya el ile servis siparişleri oluşturamazsınız.
-    Servis sözleşmesi satırını başka bir servis sözleşmesine veya servis siparişine kopyalayamazsınız.


> [!NOTE]
> Servis sözleşmesi askıdaysa tüm iliştirilmiş satırların durumu tek tek dikkate alınmadan durdurulur.

## <a name="service-agreement-lines"></a>Servis sözleşmesi satırları

Her servis sözleşmesi satırı ayrıntılı şekilde servis işinin içeriğini açıklar. Satırlar aşağıdaki ayarları içerir:

-  Hareket türü ve hareket türünin açıklaması.
-  Servis işini gerçekleştiren çalışan
-  Servis sözleşmesi için servisin uygulanması gereken nesneler.
-  İşin gerçekleştirilme sıklığı ve ilişkili madde, gider ve masraf hareketleri kaydedilir.
-  Servis siparişi satırlarının bir servis siparişi dahilinde gruplandırılabileceği zaman penceresi.
-  Sözleşme satırı kümelerini iş görevleri halinde gruplandırmak ve servis teknisyenleri ile müşterilere sağlanacak servis görevini özetlemek için kullanılan servis görevleri.
-  Bir satırın durdurulup durdurulmadığı. Bir satır durdurulmuşsa, siz konusu satır için servis siparişleri oluşturamazsınız.
-  Kategori ve satır özelliği gibi proje ayarları.

## <a name="related-topics"></a>İlgili konular

[Servis sözleşmeleri oluşturma](create-service-agreements.md)

