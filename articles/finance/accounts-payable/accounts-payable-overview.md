---
title: Borç hesaplarını yapılandırmaya genel bakış
description: Bu makalede, Borç hesapları için temel ve isteğe bağlı işlevleri ayarlamada kullanacağınız sayfalar açıklanmaktadır. Ayrıca, Borç hesaplarını ayarlamaya başlamadan önce tamamlamanız gereken kurulum adımları da açıklanmaktadır.
author: abruer
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "24671"
- intro-internal
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bce5da0c9593bcfcfb9589f8fe7e09b8acd63726
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906546"
---
# <a name="configure-accounts-payable-overview"></a>Borç hesaplarını yapılandırmaya genel bakış

[!include [banner](../includes/banner.md)]

Bu makalede, Borç hesapları için temel ve isteğe bağlı işlevleri ayarlamada kullanacağınız sayfalar açıklanmaktadır. Ayrıca, Borç hesaplarını ayarlamaya başlamadan önce tamamlamanız gereken kurulum adımları da açıklanmaktadır.

## <a name="prerequisites-for-accounts-payable-setup"></a>Borç hesapları kurulumu için ön gereksinimler

Borç hesaplarını ayarlamadan önce aşağıdaki kurulumu tamamlamanız gerekir:

-   Genel muhasebede:
    -   Ödeme Günlükleri'ni kullanmayı planlıyorsanız, ödeme günlükleri ayarlayın.
    -   Döviz kuru ayarlamalarını çalıştırmayı planlıyorsanız, **Para birimleri** sayfasında para birimi kodlarını, **Döviz kuru türleri** sayfasında döviz kuru türlerini ve **Para birimi döviz kuru** sayfasında ara birimi döviz kurlarını ayarlayın.
-   Nakit ve banka yönetimi bölümünde, ödeme yöntemleriyle kullanılacak banka hesaplarını ayarlayın.

## <a name="setup-pages-for-accounts-payable"></a>Borç hesapları için kurulum sayfaları

Her tüzel kişilik için temel Borç hesapları işlevlerini ayarlamak üzere aşağıdaki sayfaları kullanın. Sayfalar önerilen kurulum sırasıyla listelenmiştir. Kurulum işlemini kolaylaştırmak için, oluşturduğunuz ilk kayıtlardan şablonları oluşturabilirsiniz. Bir şablonda, değerler genellikle kuruluşun belirli bir satıcı tipi için uygulamak istediği özellikleri yansıtan değerleri içerir.
1.  Satış siparişlerine, satınalma siparişlerine, müşterilere ve satıcılara atadığınız ve fatura vade tarihlerini belirleyen ödeme koşullarını, **Ödeme koşulları** sayfasında tanımlayın. Daha fazla bilgi için bkz. [Satıcı ödeme ücretlerini tanımlama](tasks/define-vendor-payment-fees.md).
2.  **Ödeme yöntemleri - Satıcılar** sayfasında, kuruluşun satıcılarına nasıl ödeme yaptığı hakkındaki bilgileri oluşturun ve sürdürün.
3.  Deftere nakletme, kapatma ve ödeme, raporlama ve tahmin yürütme için önemli parametreleri paylaşan satıcı gruplarını, **Satıcı grupları** sayfasında oluşturun ve sürdürün.
4.  **Satıcı deftere nakil profilleri** sayfasında, satıcı hareketlerinin genel muhasebeye nasıl nakledildiğini tanımlayın.
5.  Daha özel bir ayar belirtilmediğinde uygulanacak varsayılan değerleri, çeşitli tiplerde işlevler için parametreleri ve Borç hesapları için çeşitli numara sıralarını **Borç hesapları parametreleri** sayfasında ayarlayın.
6.  Satıcılarla ilgili olan, satıcılardan gelen girişleri izlemek ve satıcılara ödeme akışları için nedenler girmek için kuruluşun kullandığı çeşitli belgelerin biçimini **Form kurulumu** sayfasında tanımlayın.
7.  **Satıcılar** sayfasında, satıcı hesapları ve ayrıca kuruluşunuzun satış vergilerini bildirdiği vergi dairelerini oluşturun ve sürüdün.

## <a name="optional-setup-pages-for-accounts-payable"></a>Borç hesapları için isteğe bağlı kurulum sayfaları
Temel işlevselliğe ek olarak, Borç hesapları ayarlayabileceğiniz başka işlevlere de sahiptir.

İşleve göre ek kurulum sayfaları düzenlenir.

**İlkeler**
-   **Satıcı Fatura ilkesi** sayfasında satıcı fatura ilkelerini ayarlayın.

**Fatura eşleştirme**

-   **Fatura toplamları toleransları** sayfasında, fatura toplamları için toleransları ayarlayın.
-   **Eşleşme ilkesi** sayfasında iki yönlü ve üç yönlü eşleştirme ilkeleri ayarlayın.
-   **Fiyat toleransları** sayfasında birim fiyatları için toleransları ayarlayın.
-   **Madde fiyatı tolerans grupları** sayfasında madde fiyatları için tolerans grupları ayarlayın.
-   **Satıcı fiyat toleransı grupları** sayfasında satıcı fiyatları için tolerans grupları ayarlayın.
-   **Gider toleransları** sayfasında giderler için toleransları ayarlayın.

**İş Akışı**

-   **Borç hesapları iş akışları** sayfasında, satınalma talepleri ve günlük onayları için iş akışı yapılandırmaları ayarlayın.

**Nedenler**

-   **Satıcı nedenleri** sayfasında neden kodlarını ayarlayın.

**Masraflar**

-   **Gider kodu** sayfasında kullanılan satınalma siparişlerindeki giderler için kodlar ayarlayın.
-   **Satıcı gider grubu** sayfasında satıcılar için gider grupları oluşturun ve sürdürün.
-   **Madde gideri grupları** sayfasında, maddeler için gider grupları oluşturun ve sürdürün.
-   **Otomatik giderler** sayfasında, siparişlere otomatik olarak atanan giderleri tanımlayın.

**Tamamlayıcı maddeler**

-   **Tamamlayıcı madde grupları - Satıcı** sayfasında, satıcılar için tamamlayıcı madde grupları oluşturun ve sürdürün.
-   **Tamamlayıcı madde grupları -Stok** sayfasında, maddeler için tamamlayıcı madde grupları oluşturun ve sürdürün.

**Dağıtım**

-   **Teslimat koşulları** sayfasında , satıcıdan müşteriye bir madde naklinin koşullarını oluşturun ve sürdürün.
-   **Teslimat modları** sayfasında, bir sipariş satıcıdan alıcıya teslim edildiğinde, kullanılacak taşıma yöntemlerini oluşturun ve yönetin.
-   **Hedef kodları** sayfasında, teslimat hedefleri için tanımlayıcılar ve tarifler oluşturun ve sürdürün.

**Formlar**

-   **Form notları** sayfasında, çeşitli sayfalarda görüntülenecek standart metni oluşturun.
-   **Form sıralaması parametreleri** sayfasında, talepler, giriş listeleri, sevk irsaliyeleri ve faturalar için bir sıralama düzeni ayarlayın.
-   **Yazdırma yönetimi kurulumu** sayfasında, sayfaların orjinali ve kopyası için baskı yönetim bilgisini ayarlayın.

**Ödemeler**

-   **Nakit iskontosu** sayfasında, nakit iskontoları edinmek için şartları ayarlayın ve yönetin. Nakit iskonto kodları satıcılara bağlıdır ve satınalma siparişlerine uygulanır.
-   **Ödeme zamanlamarı** sayfasında, satıcılara yapılacak taksit ödemelerini yönetmek için kullanılan ödeme planlarını ayarlayın.
-   **Ödeme günleri** sayfasında, vade tarihlerini belirlemede kullanılacak ödeme günlerini tanımlayın ve ayın veya haftanın bir günlerini ödeme günleri olarak belirleyin.
-   **Ödeme masrafları** sayfasında, satıcılar ile ilişkili ödeme masraflarını oluşturun ve sürdürün.
-   **Ödeme talimatı** sayfasında, ödeme talimatları oluşturun ve sürdürün.

**İstatistikler**

-   **Yaşlandırma dönemi tanımları** sayfasında, satıcı hesaplarının vade dağılımını analiz etmede kullanılacak, kullanıcı tarafından tanımlanan aralıkları ayarlayın.
-   **İş kolu** sayfasında, satıcılara atanan iş kolu (LOB) kodlarını oluşturun.

**Vergi 1099**

-   **1099 alanları** sayfasında, en güncel gereksinimlerine göre ABD İç Gelir Servisi'ne (IRS) bildirilecek minimum tutarları onaylayın ve güncelleyin.

## <a name="optional-setup-for-other-modules"></a>**Diğer modüller için isteğe bağlı kurulum**
**Kuruluş yönetimi**

-   **Numara sıraları** sayfasında, fatura numaraları için numara serisi grupları ayarlayın.
-   Aşağıdaki sayfalarda adres bilgilerini ayarlayın:
    -   **Adres kurulumu**
    -   **NAF kodları**
    -   **Posta kodlarını içe aktar**

**Genel muhasebe**

-   **Mali boyutlar** sayfasında, finansal boyutları ayarlayın.
-   Aşağıdaki sayfalarda, vergi bilgilerini ayarlayın:
    -   **Satış vergisi kodları**
    -   **Satış vergisi grupları**
    -   **Madde satış vergisi grupları**
    -   **Hesap grubu**
    -   **Satış vergisi muafiyet kodları**
    -   **Satış vergi daireleri**
    -   **Satış vergisi makamları**
    -   **Satış vergisi kapatma dönemleri**

**Nakit ve banka yönetimi**

-   **Ödeme amacı kodları** sayfasında, **Merkezi Banka amaç kodunu** ayarlayın.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
