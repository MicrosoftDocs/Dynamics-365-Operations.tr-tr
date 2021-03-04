---
title: Serileştirilen maddelerle çalışma
description: Bu konuda, satış işlemi sırasında sevk irsaliyeleri veya faturalar üzerine seri numaralarını nasıl kaydedeceğiniz açıklanmaktadır. Bu işlev, bir şirket servis veya garanti amaçlı olarak seri numaralarını tutmak istediğinde ancak seri numaralarını girişten çıkışa stokta tutması gerekmediğinde kullanışlıdır.
author: omulvad
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResTrackingDimensionGroup, InventTrackingRegisterTrans, SalesEditLines, SalesTable, InventSerial
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 28931
ms.assetid: 5d39630f-607e-492b-8c1e-790ca53effa0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 989dcca499f6d27ae9680f184978d5500397fa57
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439225"
---
# <a name="working-with-serialized-items"></a>Serileştirilen maddelerle çalışma

[!include [banner](../includes/banner.md)]

Bu konuda, satış işlemi sırasında sevk irsaliyeleri veya faturalar üzerine seri numaralarını nasıl kaydedeceğiniz açıklanmaktadır. Bu işlev, bir şirket servis veya garanti amaçlı olarak seri numaralarını tutmak istediğinde ancak seri numaralarını girişten çıkışa stokta tutması gerekmediğinde kullanışlıdır.

Birçok şirket servis ve garanti amacıyla seri numaraları tutmak ister ancak alımdan çıkışa kadar seri numaraları stokta koruması gerekmez. Bu gibi durumlarda, ürünler satıldığında seri numaralarını sevk irsaliyelerine veya faturalara kaydedebilirsiniz. Ürünler daha sonra iade edilirse, ürünü satıp satmadığınızı ve servis ya da garanti koşullarının geçerli olup olmadığını belirlemek için her ürünü faturadan izleyebilirsiniz.

**İzleme boyutu grupları** sayfasındaki **Satış işleminde etkinleştir** seçeneğini seçerek satış işlemi için seri numaraları etkinleştirmeniz gerekir. Bunun üzerine Supply Chain Management'ta aşağıdaki olaylar gerçekleşir:
-   **Seri numaraları** hızlı sekmesinde **Seri numarası denetimi** seçeneği işaretlidir. Bu seçenek seçildiğinde, sevk irsaliyesi veya faturadaki her madde için bir seri numarası kaydetmeniz gerekir.
-   **İzin verilen boş çıkış** seçeneği hariç seri numaralara ilişkin izleme boyutu grubundaki tüm seçimler kaldırılır. Seri numarası denetimini geçersiz kılmak ve ürünlerin seri numaralar kaydedilmeden paketlenip faturalanmasını sağlamak için **İzin verilen boş çıkış** seçeneğini seçebilirsiniz.

## <a name="when-do-i-register-serial-numbers-during-the-sales-process"></a>Satış işlemi sırasında seri numaraları ne zaman kaydetmem gerekir?
Seri numaraları bir satış siparişine ilişkin sevkiyat irsaliyesinde veya faturada kaydedebilirsiniz. Bir sevk irsaliyesiyle sevk edilen seri hale getirilmiş bir madde için fatura hazırlarken, sevk irsaliyesi üzerindeki hangi seri numaraların faturalanacağını seçebilirsiniz. Kaydedilen seri numaraların sayısı sevk edilen madde miktarını aşmamalıdır. Kısmi faturalama yapıyorsanız, sevk irsaliyesinde kayıtlı olandan daha az seri hale getirilmiş madde seçebilirsiniz. Sevk irsaliyesi veya fatura yazdırırken, kaydedilen seri numaralar da yazdırılır.

## <a name="can-i-enter-serial-numbers-by-scanning-them-or-do-i-have-to-type-them"></a>Seri numaraları tarayarak girebilir miyim yoksa hepsini yazmam mı gerekir?
Seri numaraları tarayabilir veya yazabilirsiniz. Bir tarayıcı kullandığınızda, tarama modu seri numaraların fatura veya sevk irsaliyesindeki seri numara listesine ekleneceğini mi yoksa kaldırılacağını mı belirler. Seri numaraları örneğin taşınabilir bir barkod tarayıcıyla taramak isterseniz, tarayıcıyı seri numarasından sonra bir ENTER veya TAB komutu gönderecek şekilde yapılandırın. Bu komut veri akışının sona erdirileceğini belirtir. Aksi halde, her seri numarayı taradıktan sonra klavyeden Enter veya TAB tuşuna basmanız gerekir.

## <a name="if-i-enable-serial-numbers-for-the-sales-process-do-i-have-to-register-all-serial-numbers-for-all-items"></a>Satış işlemi için seri numaraları etkinleştirirsem tüm maddelerin tüm seri numaralarını kaydetmem gerekir mi?
Ürüne atanan izleme boyutu grubu ayarı, bir sevk irsaliyesi veya faturadaki tüm maddeler için seri numaraların kaydedilip edilmeyeceğini belirler. Satış işlemi için seri numaraları etkinleştirdiğinizde, **Seri numarası denetimi** seçeneği otomatik olarak seçilir. Ardından, sevk irsaliyesi veya faturadaki her madde için bir seri numarası kaydetmeniz veya okunamayan numara için boş bir kayıt oluşturmanız gerekir. Her madde için seri numarası sorulmasını istemiyorsanız, maddete atanan izleme boyutu grubunda **İzin verilen boş çıkış** seçeneğini seçin. Sevk edilen madde miktarından daha az seri numarası kaydedebilirsiniz. Sevk edilen madde miktarından daha fazla seri numarası kaydederseniz, sevk irsaliyesi veya faturayı deftere nakledemezsiniz.

## <a name="can-i-register-serial-numbers-for-partial-invoices-and-partial-shipments"></a>Kısmi faturalar veya kısmi sevkiyatlar için seri numaraları kaydedebilir miyim ?
Satış siparişleri için kısmi faturalar veya sevk irsaliyeleri oluşturabilir ve yalnızca fatura veya sevk irsaliyelerinde yer alan maddeler için seri numarası kaydedebilirsiniz. Kısmi bir fatura oluşturmak istiyorsanız ve satış siparişi için birden fazla sevk irsaliyesi varsa, birden fazla sevk irsaliyesindeki seri numaralarını ekleyebilirsiniz. Ancak, tüm seri numaralarını içermeyen tek bir sevk irsaliyesi olabilir. Örneğin, üç sevk irsaliyeniz varsa ve her sevk irsaliyesi iki seri hale getirilmiş madde içeriyorsa, her sevk irsaliyesindeki tek bir madde için kısmi fatura oluşturamazsınız.

## <a name="what-do-i-do-when-a-serial-number-isnt-readable"></a>Bir seri numarası okunabilir değilse ne yapmam gerekir?
Bir seri numarası okunamıyor veya tarama yapılamıyorsa, **Seri numaraları** sayfasındaki **Okunabilir değil** öğesine tıklayarak madde için boş bir satır oluşturabilirsiniz. Seri numarası daha sonra kullanılabilir duruma gelirse, fatura veya sevk irsaliyesini güncelleştirebilirsiniz. Daha fazla bilgi için "Bir satış siparişi için kaydettiğin seri numaralarını düzeltebilir veya değiştirebilir miyim?" başlıklı sonraki bölüme bakın.

## <a name="can-i-correct-or-change-the-serial-numbers-that-i-have-registered-for-a-sales-order"></a>Bir satış siparişi için kaydettiğin seri numaralarını düzeltebilir veya değiştirebilir miyim?
Evet, aşağıdaki koşulların yerine getirilmesi durumunda seri numaraları düzeltebilirsiniz:
-   **Faturalar** – Henüz faturalandırmadığınız maddeler için seri numarasını değiştirebilirsiniz. Bu durumda sevk irsaliyesi de güncelleştirilir. Ancak, bir satış siparişi satırı negatif miktar kaydedilerek düzeltilmişse, satış siparişi satırı için seri numaraları değiştiremezsiniz.
-   **Sevk irsaliyeleri** – Seri hale getirilmiş maddeler içeren bir sevk irsaliyesi satırını kısmi olarak düzeltemezsiniz. Satır için tüm miktarı tersine çevirmeniz gerekir. Bir sevk irsaliyesi iptal edilir veya düzeltilirse, aynı seri hale getirilmiş maddeler için yeni bir sevk irsaliyesi oluştururken tersine çevrilen seri numaralarını yeniden kaydetmeniz gerekmez. Daha önce kaydedilmiş olan numaralar kullanılır.

## <a name="can-i-view-the-serial-numbers-that-were-shipped-together-with-a-specific-packing-slip-or-that-were-included-on-an-invoice"></a>Belirli bir sevk irsaliyesiyle birlikte sevk edilen veya bir faturaya eklenmiş olan seri numaralarını görebilir miyim?
Evet. Belgeye eklenmiş olan tüm seri numaralarının listesini görüntülemek için sevk irsaliyesi günlük satırında veya fatura günlüğü satırında bir sorgu çalıştırabilirsiniz.

## <a name="can-i-view-the-serialized-items-that-i-have-on-hand"></a>Elimde bulunan seri hale getirilmiş maddeleri görüntüleyebilir miyim?
Hayır. Seri numaraları maddeler satılana kadar kaydedilmediğinden elinizde bulunan seri hale getirilmiş maddeleri göremezsiniz.

## <a name="can-i-register-serial-numbers-for-catchweight-items"></a>Fiili ağırlık maddeleri için seri numaralar kaydedebilir miyim?
Hayır. Satış işlemi sırasında fiili ağırlık maddeleri için seri numaralar kaydedemezsiniz. Ayrıca, bir ürünün fiili ağırlık maddesi olarak ayarlanması durumunda, ürünü yalnızca satış işlemi sırasında seri numaralar kullanmak üzere ayarlanan bir izleme boyutu grubuna atayamazsınız.

## <a name="can-i-register-serial-numbers-at-the-retail-pos"></a>Retail POS'ta seri numaraları kaydedebilir miyim?

Evet. Kullanıcı yalnızca satış işlemi sırasında seri numaraları kullanmak üzere ayarlanan bir boyut izleme grubuna atanmış bir madde sattığında, Perakende satış noktası (POS) kullanıcıdan bir seri numarası girmesini ister.

## <a name="what-security-roles-are-required-in-order-to-register-serial-numbers-during-the-sales-process"></a>Satış işlemi sırasında seri numaraları kaydetmek için gerekli olan güvenlik rolleri nelerdir?
Bu işlev, satış sevk irsaliyelerini ve satış faturalarını takip edebilen tüm roller tarafından kullanılabilir. Aşağıdaki görevler çalışanların seri numaraları düzeltmesine ve okunamayan ya da taranamayan seri numaralar için boş girişler kaydetmesine olanak tanır:
-   Seri numarası düzeltmelerini korumak
-   Okunamayan seri numaralarının kaydını korumak







[!INCLUDE[footer-include](../../includes/footer-banner.md)]