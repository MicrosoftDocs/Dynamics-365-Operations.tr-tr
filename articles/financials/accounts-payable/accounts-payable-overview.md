---
title: "Borç hesaplarını yapılandırın"
description: "Bu makale, Microsoft Dynamics 365 for Finance and Operations'ta Borç hesapları için temel ve isteğe bağlı işlevleri ayarlamada kullanacağınız sayfaları açıklar. Ayrıca, Borç hesaplarını ayarlamaya başlamadan önce tamamlamanız gereken kurulum adımları da açıklanmaktadır."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 60313da23fdbd5a06b71c7c91a236165f8f189de
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="configure-accounts-payable"></a>Borç hesaplarını yapılandırın

[!include [banner](../includes/banner.md)]

Bu makale, Microsoft Dynamics 365 for Finance and Operations'ta Borç hesapları için temel ve isteğe bağlı işlevleri ayarlamada kullanacağınız sayfaları açıklar. Ayrıca, Borç hesaplarını ayarlamaya başlamadan önce tamamlamanız gereken kurulum adımları da açıklanmaktadır.

<a name="prerequisites-for-accounts-payable-setup"></a>Borç hesapları kurulumu için ön gereksinimler
----------------------------------------

Borç hesaplarını ayarlamadan önce aşağıdaki kurulumu tamamlamanız gerekir:

-   Genel muhasebe hesabında:
    -   Ödeme Günlükleri'ni kullanmayı planlıyorsanız, ödeme günlükleri ayarlayın.
    -   Döviz kuru ayarlamalarını çalıştırmayı planlıyorsanız, Para birimleri sayfasında para birimi kodlarını, Döviz kurları türleri sayfasında döviz kuru türlerini ve Para birimi döviz kuru sayfasında, para birimi döviz kurlarını ayarlayın.
-   Nakit ve banka yönetimi bölümünde, ödeme yöntemleriyle kullanılacak banka hesaplarını ayarlayın.

## <a name="setup-pages-for-accounts-payable"></a>Borç hesapları için kurulum sayfaları

Her tüzel kişilik için temel Borç hesapları işlevlerini ayarlamak üzere aşağıdaki sayfaları kullanın. Sayfalar önerilen kurulum sırasıyla listelenmiştir. Kurulum işlemini kolaylaştırmak için, oluşturduğunuz ilk kayıtlardan şablonları oluşturabilirsiniz. Bir şablonda, değerler genellikle kuruluşun belirli bir satıcı tipi için uygulamak istediği özellikleri yansıtan değerleri içerir.
1.  Satış siparişlerine, satınalma siparişlerine, müşterilere ve satıcılara atadığınız ve fatura vade tarihlerini belirleyen ödeme koşullarını, Ödeme koşulları sayfasında tanımlayın. Daha fazla bilgi için bkz. [Satıcı ödeme ücretlerini tanımlama](tasks/define-vendor-payment-fees.md).
2.  Ödeme yöntemleri - Satıcılar sayfa üzerinde, kuruluşun satıcılarına nasıl ödeme yaptığı hakkındaki bilgileri oluşturun ve sürdürün.
3.  Deftere nakletme, kapatma ve ödeme, raporlama ve tahmin yürütme için önemli parametreleri paylaşan satıcı gruplarını, Satıcı grupları sayfasında oluşturun ve sürdürün.
4.  Satıcı deftere nakil profilleri sayfasında, satıcı hareketlerinin genel muhasebeye nasıl nakledildiğini tanımlayın.
5.  Daha özel bir ayar belirtilmediğinde uygulanacak varsayılan değerleri, çeşitli tiplerde işlevler için parametreleri ve Borç hesapları için çeşitli numara sıralarını Borç hesapları parametreleri sayfasında ayarlayın.
6.  Satıcılarla ilgili olan, satıcılardan gelen girişleri izlemek ve satıcılara ödeme akışları için nedenler girmek için kuruluşun kullandığı çeşitli belgelerin biçimini Form kurulumu sayfasında tanımlayın.
7.  Satıcılar sayfasında, satıcı hesapları ve ayrıca kuruluşunuzun satış vergilerini bildirdiği vergi dairelerini oluşturun ve sürüdün.

## <a name="optional-setup-pages-for-accounts-payable"></a>Borç hesapları için isteğe bağlı kurulum sayfaları
Temel işlevselliğe ek olarak, Borç hesapları ayarlayabileceğiniz başka işlevlere de sahiptir.

İşleve göre ek kurulum sayfaları düzenlenir.

**İlkeler**
-   Satıcı Fatura ilkesi sayfasında satıcı fatura ilkelerini ayarlayın.

**Fatura eşleştirme**

-   Fatura toplamları farkları sayfasında, fatura toplamları için fakları ayarlayın.
-   Eşleşme ilkesi sayfasında iki yönlü ve üç yollu eşleştirme ilkeleri ayarlayın.
-   Fiyat farkları sayfasında birim fiyatları için farkları ayarlayın.
-   Madde fiyatı farkı grupları sayfasında madde fiyatları için fark grupları ayarlayın.
-   Satıcı fiyatı farkı grupları sayfasında satıcı fiyatları için fark grupları ayarlayın.
-   Gider farkları sayfasında giderler için farkları ayarlayın.

**İş Akışı**

-   Borç hesapları iş akışı sayfasında, Satınalma talepleri ve günlük onayları için iş akışı yapılandırmaları ayarlayın.

**Nedenler**

-   Satıcı nedenleri sayfasında neden kodlarını ayarlayın.

**Masraflar**

-   Gider kodu sayfasında kullanılan satınalma siparişlerindeki giderleri için kodlar ayarlayın.
-   Satıcı giderleri grubu üzerinde sayfa oluşturun ve satıcılar için masraf gruplarını güncelleştirin.
-   Madde giderini grupları sayfasında, maddeler için giderler grupları oluşturun ve sürdürün.
-   Otomatik masraflar sayfasında, siparişlere otomatik olarak atanan giderleri tanımlayın.

**Tamamlayıcı maddeler**

-   Tamamlayıcı madde grupları üzerinde- Satıcı sayfasında, satıcılar için tamamlayıcı madde grupları oluşturun ve sürdürün.
-   Tamamlayıcı madde grupları üzerinde-Stok sayfasında, maddeler için tamamlayıcı madde grupları oluşturun ve sürdürün.

**Dağıtım**

-   Teslimat koşulları sayfasında , satıcıdan müşteriye bir madde naklinin koşullarını oluşturun ve sürdürün.
-   Teslimat modları sayfasında, bir sipariş satıcıdan alıcıya teslim edildiğinde, kullanılacak taşıma yöntemlerini oluşturun ve yönetin.
-   Hedef kodları sayfasında, teslimat hedefleri için tanımlayıcılar ve tarifler oluşturun ve sürdürün.

**Formlar**

-   Form notlarısayfasında, çeşitli sayfalarda görüntülenecek standar metni oluşturun.
-   Form sıralaması parametreleri sayfasında, talepler, giriş listeleri, sevk irsaliyeleri ve faturalar için bir sıralama düzeni ayarlayın.
-   Yazdırma yönetimi kurulumu sayfasında, sayfaların orjinali ve kopyası için baskı yönetim bilgisini ayarlayın.

**Ödemeler**

-   Nakit iskontosu sayfasında, nakit iskontoları edinmek için şartları ayarlayın ve yönetin. Nakit iskonto kodları satıcılara bağlıdır ve satınalma siparişlerine uygulanır.
-   Ödeme planları sayfasında, satıcılara yapılacak taksit ödemelerini yönetmek için kullanılan ödeme planlarını ayarlayın.
-   Ödeme günleri sayfasında, vade tarihlerini belirlemede kullanılacak ödeme günlerini tanımlayın ve ayın veya haftanın bir günlerini ödeme günleri olarak belirleyin.
-   Ödeme masrafları sayfasında, satıcılar ile ilişkili ödeme masraflarını oluşturun ve sürdürün.
-   Ödeme talimatı sayfasında, ödeme talimatları oluşturun ve sürdürün.

**İstatistikler**

-   Yaşlandırma dönemi tanımları sayfasında, satıcı hesaplarının vade dağılımını analiz etmede kullanılacak, kullanıcı tarafından tanımlanan aralıkları ayarlayın.
-   İş kolu sayfasında, satıcılara atanan iş kolu (LOB) kodlarını oluşturun.

**Vergi 1099**

-   **1099 alanları** sayfasında, en güncel gereksinimlerine göre ABD İç Gelir Servisi'ne (IRS) bildirilecek minimum tutarları onaylayın ve güncelleyin.

## <a name="optional-setup-for-other-modules"></a>**Diğer modüller için isteğe bağlı kurulum**
**Kuruluş yönetimi**

-   Numara serileri sayfasında, fatura numaraları için numara serisi grupları ayarlayın.
-   Aşağıdaki sayfalarda adres bilgilerini ayarlayın:
    -   Adres kurulumu
    -   NAF kodları
    -   Posta kodlarını içe aktar

**Genel muhasebe**

-   Finansal boyutlar sayfasında, finansal boyutları ayarlayın.
-   Aşağıdaki sayfalarda, vergi bilgilerini ayarlayın:
    -   Satış vergisi kodları
    -   Satış vergisi grupları
    -   Madde satış vergisi grupları
    -   Hesap grubu
    -   Satış vergisi muafiyet kodları
    -   Satış vergi daireleri
    -   Satış vergisi makamları
    -   Satış vergisi kapatma dönemleri

**Nakit ve banka yönetimi**

-   Ödeme amaçları kodları sayfasında, Merkezi Banka amaç kodunu ayarlayın.






