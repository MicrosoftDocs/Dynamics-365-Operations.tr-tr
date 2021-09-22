---
title: Onaylanan bir satıcı için geçerlilik tarihi değiştirilemiyor
description: Ürün varlığına göre Onaylanan satıcı listesi, geçerlilik tarihinin değiştirilmesine izin vermiyor
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: cb6dbd134d63daa163261cabdbd7eceb978877ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477804"
---
# <a name="cant-change-the-effective-date-for-an-approved-vendor"></a>Onaylanan bir satıcı için geçerlilik tarihi değiştirilemiyor


## <a name="symptoms"></a>Belirtiler

Bir üründe, örneğin, geçerlilik tarihi 11 Ocak 2018 (*11.01.2018*) ve sona erme tarihi *Hiçbir zaman* olan onaylanmış bir satıcı vardır. Geçerlilik tarihini 10 Ocak 2018 (*10.01.2018*) veya 12 Ocak 2018 (*12.01.2018*) olarak değiştirmeye çalışırsanız aşağıdaki hatayı alırsınız:

> Onaylanan tedarikçi listesinde (PdsApproveVendorList) bir kayıt oluşturulamıyor. "Geçerlilik süresi" değeri "Geçerli" değerinden büyük veya eşit olmalıdır.

## <a name="resolution"></a>Çözüm

Yalnızca satıcı için onay verilen dönemi uzatabilirsiniz. Geçerli olan kurallar şunlardır:

- Geçerlilik tarihi, malzeme satıcısı için var olan kayıtlardan (dönemler) önce gelecek şekilde değiştirmek için, yeni dönemin sona erme tarihi var olan kayıtlardaki tüm sona erme tarihlerinden önce olmalıdır.
- Sona erme tarihini var olan herhangi bir dönemden daha geç olacak şekilde değiştirmek için, geçerli tarih var olan bir kayıttaki en son sona erme tarihinden sonra olmalıdır.
- Satıcının onaylandığı genel dönemi azaltmak için, var olan kayıtları silmeniz veya değiştirmeniz gerekir. Alternatif olarak, içe aktarma sırasında **kısaltma** anahtarını kullanabilirsiniz. Bu anahtar, tabloda onaylanan satıcılar için olan tüm kayıtları malzemeye göre siler.

Bir kaydın geçerlilik tarihi *11.01.2018* ve sona erme tarihi *Hiçbir zaman* olduğunda sorun açıklamasında açıklanan örnek senaryo için, geçerlilik tarihi *10.01.2018* ve sona erme tarihi *Hiçbir zaman* olan yeni bir kaydı içe aktarabilirsiniz. Ancak, geçerlilik tarihi veri yönetimi aracılığıyla *12.01.2018* olarak güncelleştirilecek şekilde dönemi azaltamazsınız. Bu değişikliği kullanıcı arayüzü aracılığıyla yapmalısınız.
