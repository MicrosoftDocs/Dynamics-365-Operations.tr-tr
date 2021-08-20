---
title: Servis sözleşmeleri geliştirme ve oluşturmaya genel bakış
description: Servis sözleşmesi tipik bir servis ziyaretinde kullanılan kaynakları ve bu kaynakların müşteriye ne şekilde faturalandığını tanımlamanızı sağlar.
author: ShylaThompson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e90161e7fa599fc76013277d3c80919fc144b77d3477e5d0318bdb5ef6da422c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771263"
---
# <a name="develop-and-establish-service-agreements-overview"></a>Servis sözleşmeleri geliştirme ve oluşturmaya genel bakış

[!include [banner](../includes/banner.md)]

Servis sözleşmesi tipik bir servis ziyaretinde kullanılan kaynakları ve bu kaynakların müşteriye ne şekilde faturalandığını tanımlamanızı sağlar.

Her servis sözleşmesi, hareketlerin deftere nakledildiği ve faturalandığı bir projeye iliştirilir. Ancak servis siparişi hareketlerini servis siparişini öncelikle bir servis sözleşmesine bağlamadan da doğrudan proje üzerinden faturalandırabilirsiniz. Servis siparişinin yalnızca bir defalık servis ziyareti olması ve servis hareketlerini hızlı bir şekilde işleme gereksiniminin belirli bir dönem boyunca müşteri hakkında ayrıntılı servis sözleşmesi bilgileri tutma gereksinimine ağır basması durumunda bunu yapmaya karar verebilirsiniz.

## <a name="service-agreement"></a>Servis anlaşması

Her servis sözleşmesinde, bir proje, bir servis sözleşmesi kodu ve bir servis sözleşmesi grubu belirtmeniz gerekir. Servis sözleşmesi grubu servis sözleşmelerini sıralamak ve düzenlemek için kullanılır.

Servis sözleşmesi başlığı, iliştirilmiş tüm sözleşme satırları için geçerli olan ayarları içerir:

-  Servis anlaşmasının askıya alınıp alınmadığı. Servis anlaşması askıya alınmışsa, servis anlaşmasından servis siparişleri oluşturamazsınız.
-  Servis anlaşmasının süresi.
-  Servis anlaşması satırlarının servis siparişleriyle ne şekilde birleştirileceği.
-  Servis sözleşmesinin bir şablon olup olmadığı

Servis sözleşmesi başlığında sözleşmenin çeşitli satırlarına eklenecek belirli servis görevlerini veya servis nesnelerini girerek servis sözleşmesiyle birlikte kullanılabilecek tüm servis nesnelerini ve servis görevlerini de ayarlayabilirsiniz.

Ayrıca, servis sözleşmesi başlığından servis sözleşmesi satırlarını veya servis şablonu satırlarını alarak geçerli servis sözleşmesine kopyalayabilirsiniz.

Servis sözleşmelerini askıya alabilir ve servis sözleşmesi satırlarını ayrı ayrı durdurabilirsiniz.

Servis sözleşmesi satırında **Askıda** onay kutusunu seçerseniz şunları yapamazsınız:

-    Servis sözleşmesinden otomatik olarak veya el ile servis siparişleri oluşturamazsınız.

Servis sözleşmesi satırındaki **Durduruldu** onay kutusunu seçerseniz şunları yapamazsınız:

-    Servis sözleşmesi satırından otomatik olarak veya el ile servis siparişleri oluşturamazsınız.
-    Servis anlaşması satırını başka bir servis anlaşmasına veya servis siparişine kopyalayamazsınız.


> [!NOTE]
> Servis sözleşmesi askıdaysa tüm iliştirilmiş satırların durumu tek tek dikkate alınmadan durdurulur.

## <a name="service-agreement-lines"></a>Servis sözleşmesi satırları

Her servis sözleşmesi satırı ayrıntılı şekilde servis işinin içeriğini açıklar. Satırlar aşağıdaki ayarları içerir:

-  Hareket tipi ve hareket tipinin açıklaması.
-  Servis işini gerçekleştiren çalışan
-  Servis anlaşması için servisin uygulanması gereken nesneler.
-  İşin gerçekleştirilme sıklığı ve ilişkili madde, gider ve masraf hareketleri kaydedilir.
-  Servis siparişi satırlarının bir servis siparişi dahilinde gruplandırılabileceği zaman penceresi.
-  Sözleşme satırı kümelerini iş görevleri halinde gruplandırmak ve servis teknisyenleri ile müşterilere sağlanacak servis görevini özetlemek için kullanılan servis görevleri.
-  Bir satırın durdurulup durdurulmadığı. Bir satır durdurulmuşsa, siz konusu satır için servis siparişleri oluşturamazsınız.
-  Kategori ve satır özelliği gibi proje ayarları.

## <a name="related-topics"></a>İlgili konular

[Servis sözleşmeleri oluşturma](create-service-agreements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]