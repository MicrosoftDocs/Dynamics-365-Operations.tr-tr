---
title: Ambar toplu işi ve seri rezervasyon hiyerarşileriyle ilgili sorunları giderme
description: Bu konuda, toplu veya seri boyutlar kullanan rezervasyon hiyerarşileri ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: a2b6f76aba22c24c07a2727b2eb8752f6ce763654403d47e34932a21a776dccb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748655"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a>Ambar toplu işi ve seri rezervasyon hiyerarşileriyle ilgili sorunları giderme

[!include [banner](../includes/banner.md)]

Bu konuda, toplu veya seri boyutlar kullanan rezervasyon hiyerarşileri ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.

Daha fazla bilgi için bkz. [Esnek ambar düzeyi boyut rezervasyonu ilkesi](flexible-warehouse-level-dimension-reservation.md).

Bir maddenin rezervasyon hiyerarşisi, talep siparişine yerleşim atamak için yerine getirilmesi gereken depolama boyutlarının gereksinimini belirler. Bu boyutlar , bir yerleşim atanmadan önce karşılanması gereken tüm boyutlar için *konum üzerindeki boyutlar* ve talep emrine bir yerleşim atandıktan sonra tahsis edilebilecek boyutlar için de *konum altındaki boyutlar* olarak açıklanabilir. Bu ayırma hiyerarşileri Ayrıca *toplu iş-üstü* ve *toplu iş altı* ayırma hiyerarşileri ya da *seri üstü* ve *seri altı* ayırma hiyerarşileri olarak da bilinir.

Yalnızca konum üstü boyutta yer yoksa, stok başarıyla tahsis edilebilir. Örneğin, *toplu iş üstü* rezervasyon hiyerarşisinde, **tesis**, **Ambar** ve **toplu iş numarası** boyutlarının talep siparişinde belirtilecek şekilde olmasını beklersiniz. Bu boyutlardan herhangi biri eksikse, tahsisat işlemi başarısız olur. Bunun aksine, *toplu iş altı* veya *seri altı* rezervasyon hiyerarşisinde, bir toplu iş veya seri numara talep siparişinde belirtilebilir, ancak tahsisat süreci bunu gerektirmez.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Şu hata iletisini alıyorum: "Dalgaya atanması için yük satırlarının konum üzerindeki boyutları belirtmelidir. Bu boyutları atamak için yük satırını ayırın ve yeniden oluşturun."

### <a name="issue-description"></a>Sorun açıklaması

*Toplu iş üstü* rezervasyon hiyerarşisine sahip bir madde kullandığınızda Kısmi bir miktar için Yük serbest bırakmaya çalışıyorsanız **Yük planlama çalışma ekranı** sayfasındaki **Ambara serbest bırak** komutu çalışmaz. Bu hata iletisini alırsınız ve kısmi miktar için hiçbir iş oluşturulmaz.

Ancak, *toplu iş altı* ayırma hiyerarşisine sahip bir madde kullandığınızda **Yük planlama çalışma ekranı sayfasından** kısmi bir miktar için bir yükü serbest bırakabilirsiniz.

### <a name="issue-cause"></a>Sorun nedeni

Boyut, Ayırma hiyerarşisindeki **Konum** boyutunun üzerinde olduğunda ambara serbest bırakma işlemi öncesinde belirtilmelidir. **Konum** üzerinde bir veya daha fazla boyut belirtilmemişse kısmi miktarlar serbest bırakılamaz.

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a>Kullanılabilir stok olmasına rağmen, bir toplu iş numarası için otomatik rezervasyon istemi tetiklenir.

### <a name="issue-description"></a>Sorun açıklaması

Ambar işlemlerini etkinleştirilmemiş bir ambarda *toplu iş üstü* rezervasyon hiyerarşisine sahip bir madde kullandığınızda ve otomatik rezervasyon etkinleştirildiğinde, malzeme çekme için yalnızca bir toplu iş olsa bile bir toplu iş numarası için otomatik rezervasyon istemi görüntülenir.

Ancak, ambar işlemlerinin etkinleştirildiği bir ambarda aynı maddeyi kullandığınızda, otomatik rezervasyon istemi gösterilmez.

### <a name="issue-cause"></a>Sorun nedeni

Rezervasyon hiyerarşisi *toplu iş üstü* veya *seri üstü* olarak tanımlanmışsa, referansta bulunulan boyut (**toplu iş numarası** veya **seri numarası**) her zaman talep siparişlerinde belirtilmelidir. Tek bir toplu iş veya seri numarası varsa, ambar işlemleri bu bilgileri tamamlayabilirler. Ancak Ambar, ambar işlemleri için etkinleştirilmediğinden, kullanıcının her zaman **konumun** üzerindeki tüm boyutları belirtmesi gerekir.

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a>Eldeki miktarı dikkate al ölçütüne sahip yerleştirme şablonları, toplu iş etkinleştirilmiş maddeler için geçerli eldeki stok envanterini dikkate almaz.

Daha fazla bilgi için bkz. [Ambar yerleştirme](warehouse-slotting.md).

### <a name="issue-description"></a>Sorun açıklaması

*Eldeki miktarı dikkate al* ölçütüne sahip yerleştirme şablonları, *toplu iş üstü* maddeler için geçerli eldeki stok envanterini dikkate almaz. Bunlar yalnızca, toplu iş numarası satış siparişi satırında belirtilmişse bunu dikkate alır.

Ancak, *toplu iş altı* maddeleri kullandığınızda, geçerli eldeki stok beklendiği gibi kabul edilir.

### <a name="issue-cause"></a>Sorun nedeni

Yerleştirme şablon başlığı *sipariş edilen*, *rezerve edilen* veya *serbest bırakılan* talep stratejisi için tanımlanabilir. *Sipariş edilen* talep stratejisi için, rezervasyon veya ambara serbest bırakma işlemlerine uygulanan aynı rezervasyon hiyerarşisi gereksinimleri geçerlidir. Bu nedenle, *toplu iş üstü* ve *Seri üstü* ayırma hiyerarşileri bulunan maddeler için, toplu iş veya seri numarasının talep emrinde (satış veya transfer) belirtilmesi gerekir. Alternatif olarak, Ambar yerleştirme talebi oluşturulmadan önce toplu iş veya seri numarasını seçmek için *Rezerve edilen* talep stratejisi kullanılabilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
