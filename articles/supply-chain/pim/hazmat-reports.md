---
title: Tehlikeli malzeme sorguları ve raporları
description: Bu konuda, tehlikeli malzemelerle ilgili çeşitli raporlar üzerinde nasıl çalışılacağı açıklanmaktadır. Bu raporların çoğu, sevkiyat ve depolama sırasında çeşitli tehlikeli malzeme yönetmeliklerine uyumluluğunuzu korumanız için gereklidir.
author: dasani-madipalli
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 07f103680cacc1273b2b28f6e4e905d6dabb006a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820334"
---
# <a name="hazardous-materials-inquiries-and-reports"></a>Tehlikeli malzeme sorguları ve raporları

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management, tehlikeli malzemeler ile ilgili çeşitli raporlar sağlar. Bu raporların çoğu, sevkiyat ve depolama sırasında çeşitli tehlikeli malzeme yönetmeliklerine uyumluluğunuzu korumanız için gereklidir.

**Birden çok yöntemle taşınan tehlikeli mallar** raporu dışındaki tüm raporlarda, maddelerin sevkiyat metnini yazdırmak için kullanılması gereken yönetmeliği bulmak amacıyla sevkiyat için tanımlanan teslimat şekli kullanılır. Teslimat şekli, sevkiyat taşıyıcısı ve taşıyıcı hizmetiyle ilişkilidir. Bu nedenle, bir sevkiyat taşıyıcısı ve taşıyıcı hizmeti ayarlamanız ve bunları bir teslimat şekline bağlamanız gerekir. Teslimat şekli, tehlikeli malzeme yönetmeliğiyle ilgilidir.

Aşağıdaki resimde, sistem tehlikeli malzeme raporları oluştururken gerçekleşen faaliyet sırasını gösterilmektedir.

![Tehlikeli malzeme raporları için faaliyet sırası](media/hazmat-report-sequence.png "Tehlikeli malzeme raporları için faaliyet sırası")

## <a name="set-up-hazardous-materials-reporting"></a><a name="set-up"></a>Tehlikeli malzeme raporlarını ayarlama

Genellikle, tehlikeli malzeme içeren maddeleri sevk ederken güvenliği korumak ve tehlikeli malzeme yönetmeliklerine uyum sağlamak için belirli raporlar oluşturmanız gerekir. Raporlarınızı ayarlamak için aşağıdaki adımları takip edin.

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.
2. **Raporlar** sekmesini açın. **Tehlikeli malzeme raporu parametresi** hızlı sekmesinde, aşağıdaki alanları ayarlayın.

    | Bölüm | Alan | Tanım |
    |---|---|---|
    | Birden Çok Yöntemle Taşınan Tehlikeli Mallar | Düzenleme kodu | **Birden çok yöntemle taşınan tehlikeli mallar** raporu oluşturulurken kullanılması gereken yönetmeliği seçin. |
    | Tehlikeli Malzeme stok limitleri | Düzenleme kodu | Stok limitleri değerlendirilirken kullanılması gereken yönetmeliği belirleyin. |
    | Kara yoluyla mal taşıma | CMR grubu ürünü | CMR, "kanserojen, mutajenik ve reprotoksik maddeler" anlamına gelir. Sistemi, bu maddelerin işlenmesine ilişkin belirli uyarlar ve mesajlar yazdıracak şekilde yapılandırmak için bu seçeneği **Evet** olarak ayarlayın. |
    | Kara yoluyla mal taşıma | Tehlikeli madde grubu açıklaması | CMR ve kara yoluyla mal taşıma ile ilgili belirli uyarıların metnini girin. Bu metin, rapora dahil edilecektir. |
    | Sevkiyatçı beyannamesi | Uyarı | Sevkiyatçı beyanname formuna yazdırılacak uyarı mesajının metnini girin (ör. "Uyarı: Tehlikeli Mallar, Yanıcı). |
    | Sevkiyatçı beyannamesi | Alt bilgi bildirimi | Sevkiyat beyanname belgesinin sonuna yazdırılması gereken mesaj metnini girin. |
    | Tehlikeli mallar raporunun dili | Tehlikeli mallar yerel raporunun dili | Yurt içi sevkiyatlarla ilişkili tehlikeli malzeme raporları için varsayılan dili seçin. |
    | Tehlikeli mallar raporunun dili | Tehlikeli mallar ihracat raporunun dili | Uluslararası sevkiyatlarla ilişkili tehlikeli malzeme raporları için varsayılan dili seçin. |

## <a name="hazardous-materials-report"></a>Tehlikeli malzeme raporu

**Tehlikeli malzeme** raporu, tehlikeli mal bilgileri içerecek şekilde ayarlanmış ve tanımlanmış tüm maddelerin listesini gösterir. Bu raporu, korumanız gereken bilgileri izlemek ve incelemek için kullanabilirsiniz. Rapor sayfası, tehlikeli malzeme ayarından sınırlı sayıda alanı gösterir. Ancak bunu, gereksinim duyduğunuz şekilde ek alanlar ekleyerek kişiselleştirebilirsiniz.

Bu raporu görüntülemek için **Ürün bilgileri yönetimi \> Sorgular ve raporlar \> Tehlikeli malzeme sevkiyatı belgeleri \> Tehlikeli malzeme**'ye gidin.

## <a name="hazardous-material-stock-limit-report"></a><a name="stock-limit-report"></a>Tehlikeli malzeme stok limiti raporu

**Tehlikeli malzeme stok limiti** raporu, depolarınızdaki tehlikeli malzeme stok düzeylerinin belirlenen güvenli limitlerin altında kalması için bu düzeyleri izlemenize olanak sağlar. Bu limitler, serbest bırakılan her bir ürün için tanımlanan limitlerden alınır.

Bu raporu görüntülemek için **Ürün bilgileri yönetimi \> Sorgular ve raporlar \> Tehlikeli malzeme sevkiyatı belgeleri \> Tehlikeli malzeme stok limitleri**'ne gidin.

Serbest bırakılan bir ürünle ilgili stok limitlerinin nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [Tehlikeli ürünler için stok limitleri ayarlama](hazmat-items.md#stock-limits).

Stok limitleri için kullanılan yönetmelik, **Ambar yönetimi parametreleri** sayfasında tanımlanmıştır. **Ambar yönetimi \> Ayar \> Ambar yönetim parametreleri**'ne gidin, ardından **Raporlar** sekmesindeki **Tehlikeli malzeme stok limiti**'nde yönetmelik kodunu belirtin. Daha fazla bilgi için bu konuda daha önce ele alınan [Tehlikeli malzeme raporlarını ayarlama](#set-up) bölümüne bakın.

## <a name="verified-gross-mass-report"></a>Doğrulanan brüt kütle raporu

**Doğrulanan brüt kütle** raporu, sevkiyatın ağırlığıyla ilgili bilgileri yazdırmanıza olanak tanır.

Bu raporu oluşturmak ve yazdırmak için **Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidip ilgili sevkiyatı açın. Ardından Eylemler Bölmesindeki **Sevkiyatlar** sekmesinde, **Tehlikeli malzeme belgesi** grubunda **Doğrulanan brüt kütle**'yi seçin.

## <a name="multimodal-dangerous-goods-report"></a>Birden çok yöntemle taşınan tehlikeli mallar raporu

**Birden çok yöntemle taşınan tehlikeli mallar** raporu, taşıma yöntemlerinin bir arada kullanılmasını gerektiren sevkiyatlar için sağlanır. Genellikle, sevkiyatın önce kara sonra deniz yoluyla taşınması durumunda kullanılır.

Bu raporu oluşturmak ve yazdırmak için **Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidip ilgili sevkiyatı açın. Ardından Eylemler Bölmesindeki **Sevkiyatlar** sekmesinde, **Tehlikeli malzeme belgesi** grubunda **Birden çok yöntemle taşınan tehlikeli mallar**'ı seçin.

Bu raporu oluşturduğunuzda gerekirse raporu düzenleyebilmeniz ve/veya yeniden yazdırabilmeniz için bilgiler kaydedilir. Oluşturulan raporu düzenlemek için **Ambar yönetimi \> Sorgular ve raporlar \> Tehlikeli malzeme sevkiyatı belgeleri \> Birden çok yöntemle taşınan tehlikeli mallar**'a gidip listede ilgili raporu bulun. İçeriği gereken şekilde düzenledikten sonra raporu yazdırmak için Eylem Bölmesinde **Yazdır**'ı seçin.

## <a name="shippers-declaration-report"></a>Sevkiyatçı beyannamesi raporu

**Sevkiyatçı beyannamesi** raporu, sevkiyata dahil edilen malzemelerin beyannamesiyle ilgili bilgileri yazdırmanıza olanak sağlar.

Bu raporu oluşturmak ve yazdırmak için **Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidip ilgili sevkiyatı açın. Ardından Eylemler Bölmesindeki **Sevkiyatlar** sekmesinde, **Tehlikeli malzeme belgesi** grubunda **Sevkiyatçı beyannamesi**'ni seçin.

## <a name="carriage-of-merchandise-by-road-report"></a>Kara yoluyla mal taşıma raporu

**Kara yoluyla mal taşıma** raporu, konşimentoya benzer ancak Tehlikeli Malların Kara Yolu ile Uluslararası Taşımacılığına İlişkin Anlaşma yönetmelikleri kapsamında Avrupa'da kara yoluyla taşıma için kullanılır. **Ambar yönetimi parametreleri** sayfasında **Tehlikeli malzeme grubu açıklaması** alanını ayarlamadığınız sürece bu raporda madde için sevkiyat yazılı metni kullanılır.

Bu raporu oluşturmak ve yazdırmak için **Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidip ilgili sevkiyatı açın. Ardından Eylemler Bölmesindeki **Sevkiyatlar** sekmesinde, **Tehlikeli malzeme belgesi** grubunda **Kara yoluyla mal taşıma**'yı seçin.

Bu raporu oluşturduğunuzda gerekirse raporu düzenleyebilmeniz ve/veya yeniden yazdırabilmeniz için bilgiler kaydedilir. Oluşturulan raporu düzenlemek için **Ambar yönetimi \> Sorgular ve raporlar \> Tehlikeli malzeme sevkiyatı belgeleri \> Kara yoluyla mal taşıma**'ya gidip listede ilgili raporu bulun. İçeriği gereken şekilde düzenledikten sonra raporu yazdırmak için Eylem Bölmesinde **Yazdır**'ı seçin.

## <a name="shipment-summary-report"></a>Sevkiyat özeti raporu

**Sevkiyat özeti** raporu, serbest bırakılmış maddelerle ilişkili taşıma kategorisi tarafından özetlenen bilgiler sağlar.

Bu raporu oluşturmak ve yazdırmak için **Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidip ilgili sevkiyatı açın. Ardından Eylemler Bölmesindeki **Sevkiyatlar** sekmesinde, **Tehlikeli malzeme belgesi** grubunda **Sevkiyat özeti**'ni seçin.

## <a name="bill-of-lading-report"></a>konşimento raporu

Sisteminizde tehlikeli malzemeler özelliği açıksa **konşimento** raporunda, bir yükün tehlikeli malzeme içerip içermediğini belirten **Tehlikeli malzemeler** sütunu bulunur. Bu rapor, her zamanki gibi **Tüm yükler** sayfasında bulunabilir.

## <a name="packing-list-report"></a>Ambalaj listesi raporu

Sisteminizdeki tehlikeli malzemeler özelliği açık olduğunda, ambalaj listelerinde maddenin sevkiyat yazdırma metniyle ilgili ek bilgiler bulunur. Bu rapor, her zamanki gibi **Tüm yükler** sayfasında bulunabilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]