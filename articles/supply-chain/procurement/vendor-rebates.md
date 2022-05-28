---
title: Satıcı indirimleri
description: Bu konu, bir satıcı indirimi ile çalışırken gerçekleştirmek isteyebileceğiniz en yaygın görevlere bir genel bakış sağlar. Satıcı indirimleri, şirketlerin kendi tedarikçi indirim programlarını daha iyi yönetmelerine, kazanılan indirimleri elde etmelerine, yönetmelerine ve izlemelerinde gerek duyulan otomatik görevleri olanak sağlar.
author: GalynaFedorova
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMVendRebateAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 2012
ms.openlocfilehash: ed41fe18048050ecb80a93e929d66ebc3a2e2441
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672976"
---
# <a name="vendor-rebates"></a>Satıcı indirimleri

[!include [banner](../includes/banner.md)]

Satıcı indirimleri, şirketlerin kendi tedarikçi indirim programlarını daha iyi yönetmelerine, kazanılan indirimleri elde etmelerine, yönetmelerine ve izlemelerinde gerek duyulan otomatik görevleri olanak sağlar.

Bu konu, bir satıcı indirimi ile çalışırken gerçekleştirmek isteyebileceğiniz en yaygın görevlere bir genel bakış sağlar. Genel bakış aşağıdaki görevleri kapsar:

- Bir indirim sözleşmesinin ayrıntıları.
- İndirimlere hak kazanan siparişleri belirleme ve indirim taleplerini oluşturma.
- Talepleri gözden geçir ve onayla.

## <a name="audience-and-purpose"></a>Kitle ve amaç

Bu konudaki bilgi kurumsal şirketlerdeki, satınalma yöneticisi, mali işler müdürü (CFO) ve muhasebe müdürü gibi aşağıdaki sorumluluklara sahip işletme karar alıcıları içindir:

- Satıcı fiyatını, indirimini ve indirim sözleşmelerinin pazarlığını yapmak.
- İndirim taleplerini işleyen ve ödemeleri toplayan personeli yönetmek.
- Stoku mümkün olan en iyi fiyattan sipariş etmek.

Bu konumlardaki kişiler, çeşitli hedeflere ulaşmak için yollar arıyor. Burada bazı örnekler verilmiştir:

- Çeşitli türde satıcı promosyon programlarını ve indirim koşullarını esnek biçimde yönetin.
- Yönetim yükünü azaltın ve promosyon performansı ve işleme talepleri ile ilişkili hataları azaltın.
- Gelecekte alınacakları tahakkuk ederek nakit akışı tahminlerini iyileştirin.
- Satıcılar ile indirimler hakkında sürmekte olan ve gelecekteki pazarlıklar hakkında temele sahip olun.

## <a name="review-details-of-a-vendor-rebate-agreement"></a>Bir satıcı indirim sözleşmesinin ayrıntıları

Bir satıcı indirim sözleşmesi, bir satıcı ile şirketin önceden belirli bazı satınalma hedeflerine ulaşılması sonucunda şirketin parasal ödüle hak kazandığı şart ve koşulları belirleyen bir sözleşmedir. Satıcı indirim sözleşmeleri, **İndirim sözleşmeleri** sayfasında kaydedilir.

**Satıcı indirim sözleşmeleri** sayfasını açmak için **Satınalma ve kaynak** &gt; **Satıcı indirimleri** &gt; **İndirim sözleşmeleri**'ni seçin.

![Satınalma sözleşmesi.](media/purchase-agreement.PNG)

**Satıcı indirim sözleşmeleri** sayfasında, bir satıcı sözleşmesinin anlaşılmış koşullarının ayrıntılarını görüntüleyebilirsiniz.

Sözleşmenin başlığı, bir şirketin indirime hak kazandığı genel koşulları belirtir. Başka bir deyişle, başlık bilgisi, belirli bir ürün, belirli bir miktarda alındığında satıcının bir indirime hak kazandığını belirtir. Başlıkta, ölçü birimi indirim seçeneğini ve hesaplama veri türünü belirtebilirsiniz.

- **Özet** sekmesinde, malzemeyi belirtmek için **Malzeme kodu**'nu *tablo* olarak ayarlanmış satırlar varsa, sözleşme belirli bir malzeme içindir. Malzemeleri belirtmek üzere **Malzeme kodu** *Grup* veya *Tümü* olarak ayarlanmış satırlar varsa, satıcı indirim sözleşmesi malzeme kodu için uygun olan malzeme koduna göre tek başına işlenir.

- **Genel** sekmesinde, **İndirim ölçü birimi seçeneği** alanında, bir ölçü biriminin satınalma siparişi satırı için, bir indirim talep etme konusunda koşul olup olmadığını belirtebilirsiniz.

    - **Dönüştürme** – Bir satınalma siparişi satırı için bir satıcı indirim indirim anlaşması başına niteler. Satırda uygulanan ölçü biriminden bağımsız olarak bir indirim alacaksınız.
    - **Tam eşleşme** – bir indirime hak kazanmak için bir satınalma satırının anlaşmada belirtilen ölçü birimi aynı olmalıdır.

- **Genel** sekmesi üzerinde, **Hesaplama veri türü** alanında, satınalmaların indirim sözleşmesinin geçerli olduğu dönemde gerçekleştiğini belirten tarihi seçin.

    - **Oluşturulan** – Satınalma siparişinin oluşturma tarihini kullan.
    - **Talep edilen teslim** – Talep edilen teslim tarihini kullan.

Sözleşme satırlarında, satıcı indirim sözleşmesini daha ayrıntılı belirtebilirsiniz.

- **Birikimli satınalma** alanında, indirim talebinin hesaplamasını ayarlayabilirsiniz. Tutar, bir döneme dayalı olacak şekilde ayarlanabilir (hafta, ay, yıl, süresiz veya özel dönem). **Fatura** değeri, bir indirim talebinin bir satınalma siparişi satırı her faturalandığında belirleneceğini belirtir.
- **Alınan** alanında, indirim hesaplama için tabanı belirtebilirsiniz.

    - **Brüt** – Temel madde üzerinde maddenin brüt fiyatından indirim hesaplanır.
    - **Net** – İndirim, maddenin net fiyatına dayanarak hesaplanır (yani, diğer indirimler uygulandıktan sonraki fiyat).

- **İndirim programı tahakkuk hesabı** ve **İndirim programı gider hesabı** alanları, tahakkuk edilen indirim tutarını onay ve işleme aşaması arasındaki arada alacak hesap numaralarını belirtir.
- **Onay gerekli** seçeneği **Evet** olarak ayarlandığında, indirim talebinin tahakkuk edilmeden veya ödenmeden önce onaylanması gerekir.
- **İndirim satır kırılma türü** alanı, indirimler için tabanı belirtir.

    - **Miktar** – İndirimler birime bağlıdır.
    - **Tutar** – İndirimler tutara bağlıdır.

- **Satırlar** hızlı sekmesinde, çeşitli tutar katmanlarının farklı indirimler vermek için nasıl ayarlanabileceğini görebilirsiniz. Örneğin, önceki şekilde **Geliş değeri** ve **Gidiş değeri** alanları, 10 ve 19 birim arasındaki bir ürün miktarının, ürün başına 15 USD indirime hak kazanacağını belirtir.

    > [!NOTE]
    > **Geliş değeri** değeri dahil ediciyken, **Gidiş değeri** değeri, hariç bırakır. Örneğin, **İndirim satır kırılma türü** alanı, **Miktar** olarak ayarlanmıştır ve **Geliş değeri** alanına **1** ve **Gidiş değeri** alanına **3** girdiniz. Bu durumda, bir veya iki maddeleri satın aldığınızda, ancak üç maddeleri satın aldığınız olmayan zaman indirim tutarı uygulanır.

- **İş akışı onay durumu** alanında **Onaylandı** değeri, anlaşmanın, anlaşma koşullarına uyan satınalma siparişlerine uygulanabileceğini belirtir.

## <a name="identify-orders-that-qualify-for-rebates-and-generate-rebate-claims"></a>İndirimlere hak kazanan siparişleri belirleme ve indirim taleplerini oluşturma

Satınalma siparişleri, şirketin bir indirim sözleşmesine sahip olduğu bir satıcı ile gerçekleştiğinde, program gelecekteki tüm kredi ödemelerini tanımlar. Satınalma siparişleri bir indirime hak kazanıyorsa, bir indirim talebi, satınalma siparişi faturasının nakledilir nakledilmez her bir sipariş satırı için oluşturulur. Bu işlem otomatiktir. Daha sonra, beklenen indirimleri gözden geçirebilir ve bu indirimlerin etkisini ürün maliyet ve kar marjı üzerinde görebilirsiniz.

### <a name="view-details-of-rebates-that-are-applied-to-a-purchase-order-line-per-the-vendor-rebate-agreement"></a>Satıcı indirim anlaşması başına bir satınalma siparişi satırına uygulanan indirimlerin ayrıntısını görüntüleme

1. **Satınalma siparişi** sayfasında bir sipariş satırını seçin ve sonra **Satınalma siparişi satırı** &gt; **Görüntüle** &gt; **Fiyat ayrıntıları**'nı seçin.
2. **Fiyat ayrıntıları** sayfasında, **İndirimler** hızlı sekmesini seçin.

İndirim bilgisi ayrıca **Fiyat ayrıntıları** sayfasının **Tahmini marj** bölümünde **Satıcı indirimleri** alanında gösterilir.

> [!NOTE]
> **Satınalma ve kaynak parametreleri** sayfasında, **Fiyatlar** sekmesinde, **Fiyat ayrıntılarını etkinleştir** seçeneğinin **Evet** olduğunu doğrulayın. Seçenek **Hayır** olarak ayarlanırsa, indirimleri göremeyebilirsiniz.

## <a name="review-and-approve-claims"></a>Talepleri gözden geçir ve onayla

Oluşturulan indirim talepleri, satıcıdan beklenen gelecekteki ödemeleri temsil eder. Satıcı için alacak dekontu verilmeden önce, sözleşme sahibi genellikle talepleri gözden geçirmek ve onaylamak ister. Ancak, bir talebin durumunun, talebin onay işlemine gitmeye hazır olup olmadığını belirlediğini unutmayın.

### <a name="the-status-of-claims-and-the-effect-on-the-approval-process"></a>Taleplerin durumu ve onay işlemine etkileri.

Bir talep oluşturulduğunda, talep toplam temelli olarak verildiyse durumu **Hesaplanacak**, fatura temelli verildiyse **Hesaplandı** olarak ayarlanır. Bir talebin durumu **Hesaplanacak** ise, talebin Toplam işlevi tarafından yönetilen bir hesaplama işleminden geçmesi gerekir. Yalnızca **Hesaplandı** durumuna sahip olan talepler onaylama işlemine dahil edilebilir.

> [!NOTE]
> Bir satıcı indirim sözleşmesindeki **Onay gerekli** seçeneği **Hayır** olarak ayarlanmışsa, oluşturulan tüm talepler **Onaylandı** duruma sahip olacaktır. Onay, toplama dayanarak verilecek tüm talepler için zorunludur.

### <a name="approve-claims-and-view-postings-and-invoice-details"></a>Talepleri onaylayın ve nakilleri ve fatura ayrıntıları görüntüleyin

Talepler onaylandığında, Borç hesapları (A/P) tarafından işlenebilirler. İndirim talebi tutarı için bir iade faturasını (satıcı faturası) otomatik olarak oluşturulur. Alacak daha sonra satıcının bakiyesine eklenebilir ve A/P ekibi, normal kapatma işlemine bunu dahil edebilir.

1. **Satınalma ve kaynak** &gt; **Satıcı İndirimleri** &gt; **İndirim talepleri**'ni bir indirim talebini açmak için seçin.
2. İndirim talebini kapatın.
3. Talebi işaretleyin ve sonra Eylem Panosunda, **Onayla**'yı seçin.
4. Talep sayfasında **Satıcı** alanında, indirim almaya yetkiniz olan satıcıyı seçin ve **Tamam**'ı işaretleyin.

    Bir indirim tahakkuk günlüğü indirim talebi için nakledilir. Bu nakil, Tahakkuk Satıcı İndirimleri Alacak hesabını beklenen satıcı kredileri için borçlandırır ve ara Tahakkuk Satıcı İndirim Alınan hesabını beklenen kazanç için alacaklandırır.

    ![İleti.](media/message.png)

5. İndirim listesinde, satırı seçin ve sonra Eylem Panosu'nda **İndirim hareketleri**'ni görmek için seçin ve bu indirim tahakkuk nakli için günlük toplu iş numarasına gidin.

    Talepleri normal A/P işleminden taşımak için A/P memurunun şimdi indirim talebini, İşlem işlevini çalıştırarak tamamlaması gerekir.

6. Eylem Panosunda, **İşlem**'i ve sonra **Filtre**'yi seçin. **Satıcı hesabı** alanı için **Ölçüt** alanında, indirim taleplerinin işleneceği satıcıyı ve diğer ilgili filtreleri seçin ve sonra **Tamam**'ı seçin.

    Mesaj çubukları ve durumun **Tamamlandı** olarak değişmesi, aşağıdaki olayların gerçekleştiğini belirtir:

    - Bir İndirim tahakkuk günlüğü nakli, tahakkuk alacak ve gider hesaplarındaki önceki ara tutarı tersine çevirdi.
    - İndirim tutarı için bir satıcı faturası (borç dekontu) oluşturuldu.

        > [!NOTE]
        > **Satınalma ve kaynak parametreleri** sayfasındaki **İndirim program** sekmesindeki **El ile fatura nakletme** seçeneği, bir talep işlemenin parçası olarak bir satıcı faturasının el ile mi otomatik mi nakledileceğini belirler.

    - Satıcı faturası otomatik veya el ile deftere nakledildiğinde, satıcının Borç hesabı borçlandırılır ve İskontolar ve Hakedişler Alacak hesabı alacaklandırılır.

        > [!NOTE] 
        > İndirim ve Hakediş Alacak hesap numarası, indirim için satınalma faturası satırında kullanılan satınalma kategorisi için belirtilir. Öte yandan, Satınalma kategorisi **Satınalma ve kaynak parametreleri** sayfasının **İndirim program** sekmesinde ayarlanır.

7. İndirim listesinde, satırı seçin ve sonra Eylem Panosu'nda **İndirim hareketleri**'ni görmek için seçin ve bu indirim tahakkuk nakli ve ayrıca satıcı fatura numarası için günlük toplu iş numarasına gidin.
8. Satıcı fatura hareketi için satırı seçin ve sonra Eylem Panosunda **Satıcı faturası**'nı seçin. Satıcı faturası deftere nakledilmişse, Fatura günlüğünü görürsünüz. Aksi takdirde, satıcı faturası el ile deftere nakil gereken bekleyen satıcı fatura olarak bağlantısını görebilirsiniz.

    Fatura satırı, **Komisyonlar ve İndirimler** satınalma kategorisi için satıcı faturasının ayrıntılarını belirtir.

9. **Tüm satıcılar** sayfasında, indirimi alacağınız satıcıyı seçin ve sonra Eylem Panosunda, **Hareketler**'i seçin. Fatura için satırı bulun. İndirim tutarı şimdi satıcı bakiyesine eklendi.

## <a name="summary"></a>Özet

Satıcı indirimlerini ele alma işlemi genellikle çok sayıda el ile izleme görevi içerir ve zahmetlidir. Bu görevleri otomatikleştirerek satıcı indirim yönetimi özelliği aşağıdaki işlemleri takip etmenizi kolaylaştırabilir:

- Doğru indirim talepleri oluşturma
- Genel muhasebede beklenen alacak ve ara kazancı tahakkuk etmek
- Satıcı bakiyesini ve gelir tablosunu, doğru hakediş ile güncelleştirmek


[!INCLUDE[footer-include](../../includes/footer-banner.md)]