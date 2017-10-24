---
title: "PunchOut eProcurement için harici katalogları kullanma"
description: "Bu konu, istekler oluşturmak ve göndermek için harici katalogları nasıl kullanacağınızı açıklar."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 035c5d15e5508c78dd66a349defd534bfecc96bb
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a>PunchOut eProcurement için harici katalogları kullanma
PunchOut e-tedarik için harici katalogları kullanarak, satıcılarınızın ürünleriyle ilgili bilgileri kendi ana verileriniz içinde korumanız gerekmez. Bunun yerine, satıcının web sitesindeki alışveriş sepeti doğru ürün bilgisine sahip istek satırlarına dönüştürülür. 

Satıcınızın ürünlerinin açıklamalarını ve fiyatlarını kendi ana ürün verilerinizde tutmaktan kaçınmanız gerekir. Bunun yerine, PunchOut e-tedarik için harici katalogları kullanın. Ardından, çalışanlar taleplerini oluşturduğunda, satıcının harici katalog sitesine çıkış yapabilirler (diğer bir deyişle, sisteminizden ayrılıp satıcının sitesine giderler). Satıcının web sitesinde alışveriş sepetine eklenen ürünler daha sonra talep satırlarına dönüştürülebilir. Bu nedenle, doğru ürün bilgilerini alırsınız: ürün kimliği, adı, fiyat ve benzeri.

Harici katalogları kullanmak için çalışanın **Satınalma taleplerim** sayfasında bir talep oluşturması gerekir.

Talebi oluşturan çalışan talebin hazırlayıcısı olarak geçer. Hazırlayan kişi olarak aşağıdaki görevleri tamamlayabilirsiniz.

Belirli talep sahibi, satınalma tüzelkişiliği ve alıcı işlem birimi için kullanılabilir olan tüm harici katalogları içeren bir sayfayı açmak için **Harici kataloglar** satırı eylemini kullanın.

İzinlere bağlı olarak talep sahibini, satınalma tüzel kişiliğini ve alıcı işlem birimini değiştirin. Bu değerlerdeki bir değişiklik bir talep sahibi için kullanılabilir olan harici kataloglar listesini değiştirebilir. Kullanılabilir olan harici kataloglar, satınalma tüzel kişiliği veya alıcı işlem birimi için geçerli etkin satın alma ilkelerine bağlıdır. Bu ilkeler belirli tedarik kategorilerine erişime izin verebilir veya erişimi engelleyebilir. Bu nedenle, bu tedarik kategorileriyle eşlenen harici katalogların listesi etkilenebilir.

İlkelerle ilgili daha fazla bilgi için bkz. [Satınalma ilkeleri](../procurement/purchase-policies.md).

- Belirli tedarik kategorileri için harici katalogları bulmak üzere katalog arama alanına metin girin.
- Satıcının web sitesindeki harici kataloğundan ürünler eklemek için harici kataloğu tıklayın. Daha sonra ürünleri alışveriş sepetine ekleyin ve ödemeye geçin. Alışveriş sepeti satırları Microsoft Dynamics 365'e aktarılacaktır.

Tedarik kategorileri için birden fazla seçenek varsa, talebe satırları eklemeden önce doğru tedarik kategorisini seçin.
Talebe satırlar eklendikten sonra harici katalogları kullanmadan daha fazla satır ekleyebilirsiniz. Alternatif olarak, satır eklemek için harici katalogları kullanmaya devam edebilirsiniz.

Talep hazır olduğunda, onay için göndermek üzere **İş akışı** > **Gönder** eylemini kullanın.

