---
title: Stok hareketi ayrıntıları
description: Bu konu, seçili bir stok hareketinin ayrıntılarını gösteren Hareket ayrıntıları sayfasına genel bakış sağlar.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventTrans, InventTransDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: fd1416f21ce15dc832dd41ea4110c93bf5bb41a2
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735924"
---
# <a name="inventory-transaction-details"></a>Stok hareketi ayrıntıları

Seçili herhangi bir stok hareketinin ayrıntılarını görüntülemek için **Hareket ayrıntıları** sayfasını kullanın.

## <a name="open-the-transaction-details-page"></a>Hareket ayrıntıları sayfasını açma

**Hareket ayrıntıları** sayfasını açmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Sorgular ve raporlar \>> Hareketler** öğesine gidin.
1. İncelemek istediğiniz hareketi seçin.
1. Eylem Bölmesinde, **Hareket ayrıntıları**'nı seçin.

## <a name="fasttabs-overview"></a>Hızlı sekmelere genel bakış

**Hareket ayrıntıları** sayfası çeşitli hızlı sekmelere bölünür. Aşağıdaki tabloda her bir hızlı sekmenin amacı açıklanmıştır.

| Hızlı sekme | Açıklama |
|---|---|
| Genel | Bu hızlı sekme, seçili stok hareketiyle ilgili temel bilgileri gösterir. **Stok hareketleri** sayfasında görülen alanlara ek olarak, bu konunun ilerleyen kısımlarında açıklanan ek alanları içerir. |
| Güncelleştirmeler | Bu hızlı sekme, seçili stok hareketinin fiziksel, mali ve kapatma yönleriyle ilgili bilgileri gösterir. Hareketin geçerli durumuna bağlı olarak, bazı alanlar boş olabilir. Ancak, hareketler deftere nakledilirken bu alanlar otomatik olarak ayarlanır. **Stok hareketleri** sayfasında görülen alanlara ek olarak bu hızlı sekme, bu konunun ilerleyen kısımlarında açıklanan ek alanları içerir. |
| Genel muhasebe nakilleri | Bu hızlı sekme, seçili stok hareketiyle ilişkili fiziksel güncelleştirme, mali güncelleştirme, fiziksel gelir, fiziksel giderler, mali gelir ve mali giderler için kullanılan deftere nakil türünü ve genel muhasebe hesabını gösterir. |
| Referanslar | Bu hızlı sekme, seçili stok hareketini oluşturan kaynak hareketle ilgili ek bilgileri gösterir. Örneğin, bu bilgiler satın alma siparişi veya satış siparişinin ayrıntılarını içerebilir. |
| İlgili bilgiler | Bu hızlı sekme, seçili stok hareketiyle ilgili ek bilgileri gösterir. Tedarik kategorileri veya projeler gibi bazı özellikleri kullanmıyorsanız, bu alanlar ayarlanmamış olabilir. |
| Mali boyutlar – fiziksel | Bu hızlı sekme, fiziksel güncelleştirme deftere nakledilirken kullanılan finansal boyut değerlerini gösterir. Fiziksel güncelleştirme deftere nakledilmemişse, alanlar boş kalır. |
| Mali boyutlar – mali | Bu hızlı sekme, mali güncelleştirme deftere nakledilirken kullanılan finansal boyut değerlerini gösterir. Mali güncelleştirme deftere nakledilmemişse, alanlar boş kalır. |
| Stok boyutları | Bu hızlı sekme, seçili stok hareketine atanan stok boyutu değerlerini gösterir. Bu değerler tesis, ambar, boyut, renk, yapılandırma, konum, parti numarası, seri numarası, envanter durumu, plaka ve sahip bilgilerini içerir. |

## <a name="fields-on-the-general-fasttab"></a>Genel hızlı sekmesindeki alanlar

Aşağıdaki tabloda, **Stok hareketleri** sayfasında da görünmeyen, **Genel** hızlı sekmesindeki alanlar açıklanmaktadır.

| Alan | Açıklama |
|---|---|
| Taraf | Seçili stok hareketi için ilgili tarafın adı. Örneğin, bir satın alma siparişi hareketi satın alma siparişindeki satıcı adını gösterir ve bir satış siparişi hareketi müşterinin adını gösterir. Bu alan tüm stok hareketi türleri için kullanılamaz. |
| Stok referansı | Seçili stok hareketiyle ilişkili başka bir stok hareketi varsa, bu hareketin türü. Örneğin, bir satın alma siparişi bir satış siparişine göre işaretlenirse, satın alma siparişi hareketinin **Stok referansı** alanı *Satış siparişi* olarak ayarlanır. Doğrudan teslim siparişleri ve şirketlerarası siparişler için otomatik olarak işaretleme yapılır. *Standart maliyet* ve *hareketli ortalama* dışındaki maliyet yöntemleriyle işaretlemeyi kullandığınızda sistem, işaretli hareketlerde kapatmalar ve düzeltmeler oluşturur. Bu şekilde, ilk giren ilk çıkar (FIFO), son giren ilk çıkar (LIFO) veya ağırlıklı ortalama mantığını geçersiz kılan "gerçek" maliyetlendirmeyi elde edebilirsiniz. |
| Stok numarası | Seçili stok hareketiyle ilişkili belirli bir hareket. Örneğin, bir satın alma siparişi bir satış siparişine göre işaretlenirse, satın alma siparişi hareketinin **Stok numarası** alanı satış sipariş numarası olarak ayarlanır. |
| Proje kodu | Seçili stok hareketi bir projeyle ilişkiliyse, bu alan proje numarası olarak ayarlanır. |
| Lot kodu | Sistemin seçili stok hareketine atadığı benzersiz lot kodu. |
| Referans lotu | Seçili stok hareketiyle ilişkili başka stok hareketleri varsa, bu hareketlerin lot kodu. Örneğin, bir satın alma siparişi bir satış siparişine göre işaretlenirse, satın alma siparişi hareketinin **Referansı lotu** alanı satış siparişi satırının stok hareketinin **Lot Kodu** değeri olur. |
| Boyut numarası | Seçili stok hareketine atanan tüm stok boyutu değerlerinin birleşimini temsil eden benzersiz bir kod. |
| Değer açık | Seçili stok hareketinin stok kapanış işlemi tarafından kapatılıp kapatılmadığını belirten bir değer. Bu alan *Evet* olarak ayarlanmışsa hareket kapatılmamıştır. |
| Beklenen tarih | Giriş hareketleri için, stok girişinin gerçekleşmesi beklenen tarih. Örneğin bu alan, bir stok durdurma emrindeki beklenen giriş tarihini veya bir satın alma siparişi satırındaki teslimat tarihini gösterebilir. |
| Stok tarihi | Bu alan, bir fiziksel giriş deftere nakledilmeden önce giriş siparişinde bir kayıt hareketi yapıldığında ayarlanır. |
| Finansal olmayan transfer | Seçili stok hareketinin mali olmayan bir transfer olup olmadığını belirten bir değer. Mali olmayan bir transfer, mali boyutlara ilişkin bir değişiklik **Madde modeli grubu** sayfasında finansal olarak izlenmediğinde oluşur. |
| Lot kodu transfer et | Seçili stok hareketi mali olmayan bir transfer ise bu alan, seçili hareketin karşılık olarak kapatıldığı diğer stok hareketinin **Lot Kodu** değerine ayarlanır. |

## <a name="fields-on-the-updates-fasttab"></a>Güncelleştirmeler hızlı sekmesindeki alanlar

Aşağıdaki tabloda, **Stok hareketleri** sayfasında da görünmeyen, **Güncelleştirmeler** hızlı sekmesindeki alanlar açıklanmaktadır.

| Alan | Açıklama |
|---|---|
| Fiziksel fiş | Seçili stok hareketi için fiziksel deftere naklin oluşturulduğu, genel muhasebedeki fiş numarası. |
| Rota | Seçili stok hareketiyle ilişkili rota. Bu alan yalnızca ürün reçetesi (BOM) veya formül satırının belirli bir maddeyle ilişkili olduğu üretim malzeme çekme listesi hareketleri için ayarlanır. |
| Sevk irsaliyesi | Bir satın alma siparişi ürün giriş hareketi için girilen sevk irsaliyesi numarası. |
| Fiziksel maliyet tutarı | Fiziksel güncelleştirme için genel muhasebeye nakledilen tutar. Standart maliyet ürünü için bu tutar standart maliyeti gösterir. Diğer maliyetlendirme yöntemleri için, deftere nakil sırasında ürünün ağırlıklı ortalamasını temsil eder. |
| Fiziksel gelirler | Fiziksel güncelleştirme için genel muhasebeye nakledilen ertelenen gelir tutarı. |
| Yük kodu | Geçerli hareket, taşıma yönetimindeki bir yük ile ilişkiliyse, bu alan maddeyi içeren yükün benzersiz numarasını gösterir. |
| Fiziksel olarak nakledildi | Seçili stok hareketinin fiziksel olarak deftere nakledilip nakledilmediğini gösteren bir değer. Geçerli hareket genel muhasebeye nakledildiyse, fiziksel bir fiş de olacaktır. |
| Mali olarak nakledildi | Seçili stok hareketinin mali olarak deftere nakledilip nakledilmediğini gösteren bir değer. Geçerli hareket genel muhasebeye nakledildiyse, mali bir fiş de olacaktır. |
| Nakledilen fiziksel masraf | Seçili stok hareketiyle ilişkili fiziksel giderlerin deftere nakledilip nakledilmediğini gösteren değer. |
| Nakledilen mali masraf | Seçili stok hareketiyle ilişkili mali giderlerin deftere nakledilip nakledilmediğini gösteren değer. |
| Mali fiş | Mali deftere naklin oluşturulduğu, genel muhasebedeki fiş numarası. |
| Fatura | Oluşturulan fatura numarası (örneğin, bir satın alma siparişi veya satış siparişi için). |
| Düzeltme | Stok kapanışı ve düzeltme işlemindeki seçili stok hareketinde düzeltilmiş tutar. |
| Kar ve zarar, deftere nakledilen tutar | Kar ve zarar raporuna nakledilen seçili stok hareketinin tutarı. |
| Deftere nakledilmemiş fatura | **Bekleyen satıcı faturası** sayfasında görünen ilgili satın alma siparişinin fatura numarası. |
| Mali olarak kapatıldı | Hareketin tamamen kapatıldığı tarih. |
| Karşılanan FA miktarı | Kapatma kapsamındaki fiili ağırlık miktarı. |
| Kapatılan miktar | Seçili stok hareketi için kapatılan miktar. |
| Kapatılan tutar | Seçili stok hareketi için kapatılan değer. |
